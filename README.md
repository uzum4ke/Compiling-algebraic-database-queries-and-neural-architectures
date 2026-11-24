# Reading neural representations as logical queries

*Compilation, readback and operational grounding over algebraic databases*  
Conor Sheridan

What would justify saying that a group of neurons represents a particular fact? A probe can learn to predict that fact from the neurons’ activations. A stronger explanation would give us a symbolic rule, tell us exactly where it agrees with the network, and show us how to test the same fact in the environment. This manuscript develops the mathematics for asking those questions at a chosen group of registers, called a **port**.

## An example to start with

In Example 5.11, a network with two hidden units learns to decide whether two integer readings differ by at least two. Rounding its parameters to the nearest quarter preserves all 49 decisions on the task grid. On that grid the value of the second rounded unit alone tells us the decision. Now hold that value at 2 and change the first unit from 0 to 1. The output score moves from −4 to 1.25 and the decision reverses. Reading the second unit answers a question about ordinary execution. Varying the first unit independently tells us which changes to the hidden state can alter the output.

## How the paper works

**Translate a computation into a query.** A keyed program stores numbers at database rows. A foreign key tells a register where to read, and a sum specifies which rows contribute to its output. Given the register list, structural readback recovers the wiring and shared parameter addresses. If only exact evaluations are available, Theorem 3.1 gives another route for the rational sum–product language on a finite entity category. With bounds on polynomial degree and witness size, evaluations over finitely many database shapes recover a unique sum of pattern queries. A pattern may include a row simply because its presence changes how many assignments are counted. The recovered queries compose when one program feeds another.

**Give a symbol an environmental test.** From a reached history $x$, record the neural port $h(x)$. Independently, let $q(x)$ record what an environmental sensor would report after each possible sequence of actions. A property is grounded at the port when a test of $h(x)$ and a test of $q(x)$ agree on every reached history. Section 6 constructs the common quotient that collects all such properties, then determines which ones remain readable after any specified continuation. On a finite deterministic transition table it gives paired formulas in port tests and sensor experiments. In Example 6.9, the port can tell whether the device is at phase zero now, yet cannot always tell whether the next advance will take it there. Of 16 common predicates, four remain readable under every continuation.

**Recover the architectures behind the queries.** The categorical construction starts with a database table of operations and the input positions each operation reads. These tables give polynomial functors. Their free monads describe the trees obtained by composing the operations, and evaluation explains how the same parameter is used at several occurrences. Weighted lookups give attention by normalizing the eligible weights and averaging their values. The same row and parameter keys also say where contributions to a gradient must be added.

## Reading paths

| If you are interested in… | Start with |
| --- | --- |
| Exact symbolic recovery from program evaluations | §§2–3, especially Theorem 3.1 and the limits of finite probing in §3.2 |
| Interpretability and symbol grounding | §§5–6, especially Examples 5.11 and 6.9 and Theorems 6.4 and 6.7 |
| Algebraic databases, polynomial functors and architecture composition | §§8–10 |
| Derivatives, attention and learning | §14 for feedback, §§15–17 for normalized and structured attention, and §§21–22 for learner dynamics |

