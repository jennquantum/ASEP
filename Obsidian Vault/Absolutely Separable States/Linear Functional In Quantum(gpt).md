
In quantum computing, **linear functionals** are essential for various operations, particularly in the context of measurement, optimization, and the analysis of quantum states. Here are some common examples of linear functionals used in quantum computing:

### 1. **Expectation Value of an Observable**

One of the most common linear functionals in quantum mechanics and quantum computing is the **expectation value** of an observable. Given a quantum state \( \rho \) (which could be a pure state or a mixed state) and a Hermitian operator \( A \) representing an observable, the expectation value is given by:

$$
\[
\langle A \rangle_\rho = \text{Tr}(A \rho)
\]
$$

This is a linear functional because the trace operation is linear, and \( A \) is a fixed Hermitian operator. The expectation value provides a measurement outcome in a quantum system, and it plays a key role in understanding the behavior of quantum states.

#### Example:
- In the case of a Pauli matrix, say \( \sigma_z \), for a qubit state \( \rho \), the expectation value is:
$$
  \[
  \langle \sigma_z \rangle_\rho = \text{Tr}(\sigma_z \rho)
  \]
$$
  where $\( \sigma_z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} \)$, and \( \rho \) is the density matrix of the qubit.

### 2. **Fidelity Functional**

Fidelity is a measure of how close two quantum states are to each other. Given two density matrices \( \rho \) and \( \sigma \), the fidelity \( F(\rho, \sigma) \) is defined as:

$$
\[
F(\rho, \sigma) = \left( \text{Tr} \sqrt{ \sqrt{\rho} \sigma \sqrt{\rho} } \right)^2
\]
$$

In the case where one of the states is a pure state, say \( |\psi\rangle \), the fidelity simplifies to the linear functional:

$$
\[
F(\rho, |\psi\rangle) = \langle \psi | \rho | \psi \rangle
\]
$$

This expression is linear in \( \rho \), meaning that the fidelity functional for a pure state is a linear functional on the space of density matrices.

#### Example:
- For a pure state \( |\psi\rangle = |0\rangle \) and a mixed state \( \rho \), the fidelity is given by:
$$
  \[
  F(\rho, |0\rangle) = \langle 0 | \rho | 0 \rangle
  \]
$$
  This is just the projection of \( \rho \) onto the state \( |0\rangle \), which is a linear functional in \( \rho \).

### 3. **Quantum Measurement Functional**

In quantum computing, a **quantum measurement** is described by a set of positive semidefinite operators \( \{M_i\} \) known as **POVM (Positive Operator-Valued Measure) elements**. The probability of obtaining the measurement outcome corresponding to \( M_i \) when measuring a state \( \rho \) is given by the linear functional:

$$
\[
p_i = \text{Tr}(M_i \rho)
\]
$$

Each \( p_i \) is the probability of outcome \( i \) and is linear in \( \rho \). The measurement process defines a set of linear functionals, one for each possible measurement outcome.

#### Example:
- For a projective measurement with the projection operator \( P_0 = |0\rangle \langle 0| \), the probability of measuring \( |0\rangle \) in a state \( \rho \) is:
$$
  \[
  p_0 = \text{Tr}(P_0 \rho) = \langle 0 | \rho | 0 \rangle
  \]

$$
### 4. **Purity Functional**

The **purity** of a quantum state \( \rho \) is a measure of how mixed or pure the state is. It is defined as:

$$
\[
\text{Purity}(\rho) = \text{Tr}(\rho^2)
\]
$$

This functional is **quadratic**, but if we fix one of the states in a convex combination, we get a **linear functional**.

For instance, if we want to measure the purity change in a convex combination \( \rho = \lambda \rho_1 + (1 - \lambda) \rho_2 \), the purity of \( \rho \) can be expanded, and the purity contribution of \( \rho_1 \) or \( \rho_2 \) individually is linear in their respective coefficients.

#### Example:
- For a pure state \( |\psi\rangle \), the purity is:
$$
  \[
  \text{Purity}(|\psi\rangle) = \langle \psi | \psi \rangle = 1
  \]
$$
  whereas for a mixed state \( \rho \), the functional will give:
$$
  \[
  \text{Purity}(\rho) = \text{Tr}(\rho^2)
  \]

$$
### 5. **Entanglement Witness Functional**

An **entanglement witness** is a Hermitian operator \( W \) designed to detect entanglement in a quantum state. If \( \rho \) is a separable state, the functional \( \text{Tr}(W \rho) \geq 0 \), and if \( \rho \) is entangled, \( \text{Tr}(W \rho) < 0 \). The entanglement witness defines a linear functional:

$$
\[
\langle W \rangle_\rho = \text{Tr}(W \rho)
\]
$$

This functional can be used to distinguish between separable and entangled states.

#### Example:
- For a specific witness operator \( W \), say, designed to detect entanglement in a Bell state, the value of \( \text{Tr}(W \rho) \) will be negative if \( \rho \) is an entangled state, showing that it’s useful for detecting quantum correlations.

### 6. **Von Neumann Entropy Functional (for small perturbations)**

Although the **von Neumann entropy**:
$$
\[
S(\rho) = - \text{Tr}(\rho \log \rho)
\]
$$
is nonlinear in general, in certain contexts (such as small perturbations around a fixed state), it can be treated as a linear functional. For small variations in the state \( \rho \), the change in entropy behaves linearly in the perturbation. This approximation is often used in thermodynamic and quantum information contexts when considering slight deviations from equilibrium or known states.

---

### Summary:

In quantum computing, linear functionals often appear as traces of density matrices with fixed Hermitian operators. Examples include:
- **Expectation values** of observables, such as $\( \text{Tr}(A \rho)$ \).
- **Measurement probabilities**, such as $\( p_i = \text{Tr}(M_i \rho)$ \) in POVM measurements.
- **Fidelity** functionals, like \( $F(\rho, |\psi\rangle) = \langle \psi | \rho | \psi \rangle \)$.
- **Entanglement witnesses**, where $\( \text{Tr}(W \rho) \)$ reveals entanglement properties.

These linear functionals are crucial tools in understanding and manipulating quantum states, especially in measurement, optimization, and entanglement detection.






To express \( \text{Tr}(A \rho) \) in terms of the eigenvalues of \( \rho \), let’s break it down step by step.

### 1. **Eigenvalue Decomposition of \( \rho \)**

Given that \( \rho \) is a density matrix, we can diagonalize \( \rho \) in terms of its eigenvalues and eigenvectors. Let:
$$
\[
\rho = \sum_i \lambda_i | \psi_i \rangle \langle \psi_i |
\]
$$
where \( \lambda_i \) are the eigenvalues of \( \rho \), and \( |\psi_i\rangle \) are the corresponding eigenvectors. Since \( \rho \) is a density matrix, the eigenvalues \( \lambda_i \) are non-negative and sum to 1:
$$
\[
\sum_i \lambda_i = 1.
\]
$$

### 2. **Expression of \( \text{Tr}(A \rho) \)**

Now, we want to calculate \( \text{Tr}(A \rho) \), where \( A \) is a Hermitian operator (such as an observable). Using the eigenvalue decomposition of \( \rho \), we substitute \( \rho = \sum_i \lambda_i |\psi_i \rangle \langle \psi_i| \) into the trace expression:

$$
\[
\text{Tr}(A \rho) = \text{Tr}\left(A \sum_i \lambda_i |\psi_i \rangle \langle \psi_i| \right)
\]
$$

Since the trace is linear, we can pull the sum and the eigenvalues \( \lambda_i \) outside:

$$
\[
\text{Tr}(A \rho) = \sum_i \lambda_i \text{Tr}(A |\psi_i \rangle \langle \psi_i|)
\]
$$

### 3. **Simplifying the Trace**

Next, we use the fact that the trace of an outer product \( |\psi_i \rangle \langle \psi_i| \) with an operator \( A \) is given by:
$$
\[
\text{Tr}(A |\psi_i \rangle \langle \psi_i|) = \langle \psi_i | A | \psi_i \rangle.
\]
$$

Thus, we have:

$$
\[
\text{Tr}(A \rho) = \sum_i \lambda_i \langle \psi_i | A | \psi_i \rangle.
\]
$$

### Final Expression

The trace of \( A \rho \) in terms of the eigenvalues \( \lambda_i \) of \( \rho \) is:

$$
\[
\text{Tr}(A \rho) = \sum_i \lambda_i \langle \psi_i | A | \psi_i \rangle.
\]
$$

This expression shows that \$( \text{Tr}(A \rho) \)$ is a weighted sum of the expectation values \$$( \langle \psi_i | A | \psi_i \rangle \)$$, with the eigenvalues $\( \lambda_i \)$ serving as the weights.