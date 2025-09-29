<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
|[<b>Home</b>](https://hxuhack.github.io/) | [<b>Publications</b>](../publication/list) | [<b>Artisan-Lab</b>](../lab/page) | [<b>Pictures</b>](../photo/page) | [<b>Misc</b>](../misc/list) |
# Rationale on the Soundness of Tracing based Verification Methodology
(This article justifies the soundness of our verification approach used in [RAPx](https://artisan-lab.github.io/RAPx-Book/6.4-unsafe.html).)

To verify the soundness of Rust APIs, we employ a tracing-based method.
Informally, our approach assumes that all undefined behaviors originate from unsafe code, 
and that the risks of undefined behavior are determined solely by the safety properties (_i.e.,_ a set of constraints that must be satisfied to avoid undefined behavior) of that unsafe code.
By tracing all possible execution paths and showing that these safety properties are always satisfied, we can formally verify the soundness of the API.

In the following paragraphs, we will attempt to prove that the assumption holds.
To simplify our discussion, the proof considers only a subset of Rust with static functions.
However, it can also be extended to more advanced constructs with dynamic methods.

## To Prove

We aim to prove the following theorem. 

**Theorem (Origin of Undefined Behavior)**
Undefined behavior originates exclusively from unsafe code and is solely determined by the safety constraints of that unsafe code.

## Proof

**Definition ([Safety Promise of Rust](https://rust-lang.github.io/unsafe-code-guidelines/glossary.html#soundness-of-code--of-a-library))**  
Only programs that use unsafe code may exhibit undefined behavior.

Based on the definition, two propositions can be derived.

**Proposition 1 (Compiler Soundness)**  
Rust compiler is sound iff 

$$
  \forall P_s, P_s \nRightarrow UB
$$

, where $$P_s$$ denotes any Rust program that does not use unsafe code..

**Proposition 2 (Safe API Soundness)**  
A safe public API $$f_s$$ provided by a module is sound iff 

$$
  \forall P_{f_s},\ P_{f_s} \nRightarrow UB
$$

, where $$P_{f_s}$$ denotes any program of another module that uses $$f_s$$ and contains no unsafe code.

The proof of the two propositions is straightforward: assuming the existence of a $$P_s$$ or $$P_{f_s}$$ that leads to undefined behavior would contradict the Safety Promise of Rust.

Next, we extend the discussion to the soundness of unsafe Rust using inductive reasoning.

**Observation 1 (Pervasiveness of Safety Constraints)**  
Each unsafe API has a set of safety constraints (a sufficient condition) that must be satisfied to avoid undefined behavior.

**Observation 2 (Uniformity of Safety Constraints)**  
The safety constraints of each API are uniform across all call sites.

Based on the two observations, we can derive the following proposition.

**Proposition 3 (Unsafe API Soundness)**  
An unsafe API $$f_u$$ with safety constraint $$SC_{f_u}$$ is sound iff

$$
  \forall P_{f_u}\ \text{s.t.}\ P_{f_u} \vdash SC_{f_u},\ P_{f_u} \nRightarrow UB
$$

where $$P_{f_u}$$ denotes any program of another module that uses $$f_u$$ and contains no other unsafe code.

Now the theorem can be proved:
- Assume that the Rust compiler is sound (Proposition 1) and all safe APIs are sound (Proposition 2), only unsafe Rust can introduce undefined behaviors.
- Assuming an unsafe API is sound (Proposition 3), any undefined behavior observed when using the API​ must result from a violation of its safety constraint, which completes the proof of the theorem.


## Application in Verification

From the theorem, we derive the following two corollaries, which can be applied in verification.

**Corollary 1 (Encapsulation Soundness of Safe API)**  
A safe API $$f_s$$ is sound iff it contains no unsafe code, or,
if it contains unsafe code, all safety constraints of the internal unsafe code are satisfied by the API itself.

**Corollary 2 (Encapsulation Soundness of Unsafe API)**  
An unsafe API $$f_u$$ with one or more internal unsafe call sites is sound iff 
all residual safety constraints from the internal unsafe call sites that cannot be enforced internally are reflected as the safety constraints of the API itself.



