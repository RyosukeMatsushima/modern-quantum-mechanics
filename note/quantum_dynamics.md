# 2 Quantum Dynamics

So far we have not discussed how physical systems change with time. This chapter is devoted exclusively to the dynamic development of state kets and/or observables. In other words, we are concerned here with the quantum-mechanical analogue of Newton's (or Lagrange's or Hamilton's) equations of motion.

## 2.1 Time Evolution and the Schrödinger Equation

The first important point we should keep in mind is that time is just a parameter in quantum mechanics, not an operator. In particular, time is not an observable in the language of the previous chapter. It is nonsensical to talk about the time operator in the same sense as we talk about the position operator. 

Ironically, in the historical development of wave mechanics both L. de Broglie and E. Schrödinger were guided by a kind of covariant analogy between energy and time on the one hand and momentum and position (spatial coordinate) on the other. Yet when we now look at quantum mechanics in its finished form, there is no trace of a symmetrical treatment between time and space. The relativistic quantum theory of fields does treat the time and space coordinates on the same footing, but it does so only at the expense of demoting position from the status of being an observable to that of being just a parameter.

### 2.1.1 Time-Evolution Operator

Our basic concern in this section is: How does a state ket change with time? Suppose we have a physical system whose state ket at $t_0$ is represented by $|\alpha\rangle$. At later times, we do not, in general, expect the system to remain in the same state $|\alpha\rangle$. Let us denote the ket corresponding to the state at some later time by

$$|\alpha, t_0; t\rangle \quad (t > t_0)$$

where we have written $\alpha, t_0$ to remind ourselves that the system used to be in state $|\alpha\rangle$ at some earlier reference time $t_0$. Because time is assumed to be a continuous parameter, we expect

$$\lim_{t \to t_0} |\alpha, t_0; t\rangle = |\alpha\rangle$$

and we may as well use a shorthand notation,

$$|\alpha, t_0; t_0\rangle = |\alpha, t_0\rangle$$

Our basic task is to study the time evolution of a state ket:

$$|\alpha, t_0\rangle \xrightarrow{\text{time evolution}} |\alpha, t_0; t\rangle$$

Put in another way, we are interested in asking how the state ket changes under a time displacement $t_0 \to t$.

As in the case of translation, the two kets are related by an operator which we call the time-evolution operator $U(t, t_0)$:

$$|\alpha, t_0; t\rangle = U(t, t_0) |\alpha, t_0\rangle$$

#### Properties of the Time-Evolution Operator

**Unitarity (Probability Conservation):**

Suppose that at $t_0$ the state ket is expanded in terms of the eigenkets of some observable $A$:

$$|\alpha, t_0\rangle = \sum_a c_a(t_0) |a\rangle$$

Likewise, at some later time,

$$|\alpha, t_0; t\rangle = \sum_a c_a(t) |a\rangle$$

In general, we do not expect the modulus of the individual expansion coefficient to remain the same:

$$|c_a(t)| \neq |c_a(t_0)|$$

For instance, consider a spin $\frac{1}{2}$ system with its spin magnetic moment subjected to a uniform magnetic field in the z-direction. To be specific, suppose that at $t_0$ the spin is in the positive x-direction; that is, the system is prepared in an eigenstate of $S_x$ with eigenvalue $\hbar/2$. As time goes on, the spin precesses in the xy-plane, as will be quantitatively demonstrated later in this section. This means that the probability for observing $S_x +$ is no longer unity at $t > t_0$; there is a finite probability for observing $S_x -$ as well. Yet the sum of the probabilities for $S_x +$ and $S_x -$ remains unity at all times. Generally, we must have

$$\sum_a |c_a(t_0)|^2 = \sum_a |c_a(t)|^2$$

despite the individual expansion coefficients changing. Stated another way, if the state ket is initially normalized to unity, it must remain normalized to unity at all later times:

$$\langle \alpha, t_0 | \alpha, t_0 \rangle = 1 \implies \langle \alpha, t_0; t | \alpha, t_0; t \rangle = 1$$

This property is guaranteed if the time-evolution operator is taken to be unitary:

$$U^\dagger(t, t_0) U(t, t_0) = 1$$

**Composition Property:**

$$U(t_2, t_0) = U(t_2, t_1) U(t_1, t_0) \quad (t_2 > t_1 > t_0)$$

This equation says that if we are interested in obtaining time evolution from $t_0$ to $t_2$, then we can obtain the same result by first considering time evolution from $t_0$ to $t_1$, then from $t_1$ to $t_2$, a reasonable requirement. Note that we read this equation from right to left!

**Infinitesimal Time-Evolution Operator:**

It also turns out to be advantageous to consider an infinitesimal time-evolution operator $U(t_0 + dt, t_0)$:

$$|\alpha, t_0; t_0 + dt\rangle = U(t_0 + dt, t_0)|\alpha, t_0\rangle$$

Because of continuity, the infinitesimal time-evolution operator must reduce to the identity operator as $dt$ goes to zero,

$$\lim_{dt \to 0} U(t_0 + dt, t_0) = 1$$

and as in the translation case, we expect the difference between $U(t_0 + dt, t_0)$ and $1$ to be of first order in $dt$.

We assert that all these requirements are satisfied by

$$U(t_0 + dt, t_0) = 1 - i\Omega dt$$

where $\Omega$ is a Hermitian operator:

$$\Omega^\dagger = \Omega$$

With this form, the infinitesimal time-displacement operator satisfies the composition property:

$$U(t_0 + dt_1 + dt_2, t_0) = U(t_0 + dt_1 + dt_2, t_0 + dt_1)U(t_0 + dt_1, t_0)$$

it differs from the identity operator by a term of order $dt$. The unitarity property can also be checked as follows:

$$U^\dagger(t_0 + dt, t_0)U(t_0 + dt, t_0) = (1 + i\Omega^\dagger dt)(1 - i\Omega dt) \approx 1$$

to the extent that terms of order $(dt)^2$ or higher can be ignored.


The operator $\Omega$ has the dimension of frequency (inverse time). Is there any familiar observable with the dimension of frequency? Recall that in the old quantum theory, angular frequency $\omega$ is postulated to be related to energy by the Planck–Einstein relation $E = \hbar \omega$. If the $\Omega$ operator depends explicitly on time, it must be evaluated at $t_0$.

Borrowing from classical mechanics, where the Hamiltonian is the generator of time evolution, it is natural to relate $\Omega$ to the Hamiltonian operator $H$:

$$\Omega = \frac{H}{\hbar}$$

Thus, the infinitesimal time-evolution operator is

$$U(t_0 + dt, t_0) = 1 - \frac{iH dt}{\hbar}$$

where $H$, the Hamiltonian operator, is assumed to be Hermitian. The $\hbar$ introduced here is the same as that which appears in the translation operator. This can be confirmed by comparing the quantum-mechanical equation of motion derived later with its classical counterpart. In fact, unless the two $\hbar$ are taken to be the same, the classical limit of the quantum-mechanical relation does not yield the familiar equation

$$\frac{dx}{dt} = \frac{p}{m}$$

as expected.

From the corresponding quantum-mechanical relation:

$$U(t_0 + dt, t_0) = 1 - \frac{iH dt}{\hbar}$$

### 2.1.2 The Schrödinger Equation

We are now in a position to derive the fundamental differential equation for the time-evolution operator $U(t, t_0)$. We exploit the composition property of the time-evolution operator by letting $t_1 \to t$, $t_2 \to t + dt$ in the composition property:

$$U(t + dt, t_0) = U(t + dt, t)U(t, t_0) = \left(1 - \frac{iH dt}{\hbar}\right)U(t, t_0)$$

where the time difference $t - t_0$ need not be infinitesimal. We have

$$U(t + dt, t_0) - U(t, t_0) = -i\frac{H}{\hbar} dt \cdot U(t, t_0)$$

which can be written in differential equation form:

$$i\hbar \frac{\partial}{\partial t} U(t, t_0) = HU(t, t_0)$$

This is the **Schrödinger equation for the time-evolution operator**. Everything that has to do with time development follows from this fundamental equation.

Equation (2.25) immediately leads to the Schrödinger equation for a state ket. Multiplying both sides by $|\alpha, t_0\rangle$ on the right, we obtain

$$i\hbar \frac{\partial}{\partial t} U(t, t_0)|\alpha, t_0\rangle = HU(t, t_0)|\alpha, t_0\rangle$$

But $|\alpha, t_0\rangle$ does not depend on $t$, so this is the same as

$$i\hbar \frac{\partial}{\partial t} |\alpha, t_0; t\rangle = H|\alpha, t_0; t\rangle$$

where we have used $|\alpha, t_0; t\rangle = U(t, t_0)|\alpha, t_0\rangle$.

If we are given $U(t, t_0)$ and, in addition, know how $U(t, t_0)$ acts on the initial state ket $|\alpha, t_0\rangle$, it is not necessary to bother with the Schrödinger equation for the state ket. All we have to do is apply $U(t, t_0)$ to $|\alpha, t_0\rangle$; in this manner we can obtain a state ket at any $t$. Our first task is therefore to derive formal solutions to the Schrödinger equation for the time-evolution operator. There are three cases to be treated separately.

#### Case 1: Time-Independent Hamiltonian

The Hamiltonian operator is independent of time. By this we mean that even when the parameter $t$ is changed, the $H$ operator remains unchanged. The Hamiltonian for a spin-magnetic moment interacting with a time-independent magnetic field is an example of this. The solution in such a case is given by

$$U(t, t_0) = \exp\left(-\frac{iH(t - t_0)}{\hbar}\right)$$

To prove this let us expand the exponential as follows:

$$\exp\left(-\frac{iH(t - t_0)}{\hbar}\right) = 1 + \left(-\frac{iH(t - t_0)}{\hbar}\right) + \frac{(-i)^2 H^2(t - t_0)^2}{\hbar^2 \cdot 2!} + \cdots$$

Because the time derivative of this expansion is given by

$$\frac{\partial}{\partial t} \exp\left(-\frac{iH(t - t_0)}{\hbar}\right) = \left(-\frac{iH}{\hbar}\right) + \frac{(-i)^2}{\hbar^2} \frac{H^2(t - t_0)}{1!} + \cdots$$

the exponential expression obviously satisfies the differential equation. The boundary condition is also satisfied because as $t \to t_0$, the expression reduces to the identity operator. An alternative way to obtain this result is to compound successively infinitesimal time-evolution operators just as we did for finite translation:

$$\lim_{N \to \infty} \left(1 - \frac{iH(t - t_0)}{\hbar N}\right)^N = \exp\left(-\frac{iH(t - t_0)}{\hbar}\right)$$

#### Case 2: Time-Dependent Hamiltonian with Commuting H at Different Times

The Hamiltonian operator $H$ is time dependent but the $H$ at different times commute, i.e., $[H(t_1), H(t_2)] = 0$. As an example, let us consider the spin-magnetic moment subjected to a magnetic field whose strength varies with time but whose direction is always unchanged. The formal solution in this case is

$$U(t, t_0) = \exp\left(-\frac{i}{\hbar} \int_{t_0}^{t} dt' H(t')\right)$$

This can be proved in a similar way. We simply replace $H(t - t_0)$ in the expansion by $\int_{t_0}^{t} dt' H(t')$.

#### Case 3: Non-Commuting H at Different Times (Dyson Series)

The $H$ at different times do not commute. Continuing with the example involving spin-magnetic moment, we suppose, this time, that the magnetic field direction also changes with time: at $t = t_1$ in the x-direction, at $t = t_2$ in the y-direction, and so forth. Because $S_x$ and $S_y$ do not commute, $H(t_1)$ and $H(t_2)$, which go like $\mathbf{S} \cdot \mathbf{B}$, do not commute either. The formal solution in such a situation is given by

$$U(t, t_0) = 1 + \sum_{n=1}^{\infty} \left(-\frac{i}{\hbar}\right)^n \int_{t_0}^{t} dt_1 \int_{t_0}^{t_1} dt_2 \cdots \int_{t_0}^{t_{n-1}} dt_n H(t_1)H(t_2) \cdots H(t_n)$$

which is sometimes known as the **Dyson series**, after F. J. Dyson, who developed a perturbation expansion of this form in quantum field theory. We do not prove this expression now because the proof is very similar to the one presented in Chapter 5 for the time-evolution operator in the interaction picture.

In elementary applications, only Case 1 is of practical interest. In the remaining part of this chapter we assume that the $H$ operator is time independent. We will encounter time-dependent Hamiltonians in Chapter 5.

