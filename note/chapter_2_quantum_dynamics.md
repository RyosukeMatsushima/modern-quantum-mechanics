# Chapter 2 Quantum Dynamics

is reduced to ﬁnding an
observable that commutes with Hand evaluating its eigenvalues. Once that is done, we
expand the initial ket in terms of the eigenkets of that observable and just apply the time-evolution operator. This last step merely amounts to changing the phase of each expansioncoefﬁcient, as indicated by ( 2.39).
Even though we worked out the case where there is just one observable Athat commutes
with H, our considerations can easily be generalized when there are several mutually
compatible observables all also commuting with H:
[A,B]=[ B,C]=[ A,C]=··· =0,
[A,H]=[ B,H]=[ C,H]=··· =0.(2.42)
Using the collective index notation of Section 1.4 [see (1.130)], we have
exp⎧parenleftbigg−iHt
¯h⎧parenrightbigg
=∑
K/prime|K/prime/angbracketrightexp⎧parenleftbigg−iEK/primet
¯h⎧parenrightbigg
/angbracketleftK/prime|, (2.43)
where EK/primeis uniquely speciﬁed once a/prime,b/prime,c/prime,...are speciﬁed. It is therefore of fundamental
importance to ﬁnd a complete set of mutually compatible observables that also commute
with H. Once such a set is found, we express the initial ket as a superposition of thesimultaneous eigenkets of A,B,C,...and H. The ﬁnal step is just to apply the time-
evolution operator, written as ( 2.43). In this manner we can solve the most general initial-
value problem with a time-independent H.
2.1.4 TimeDependenceofExpectationValues
It is instructive to study how the expectation value of an observable changes as a functionof time. Suppose that at t=0 the initial state is one of the eigenstates of an observable A
that commutes with H,a si n( 2.40). We now look at the expectation value of some other
observable B, which need not commute with Anor with H. Because at a later time we have
|a
/prime,t0=0;t/angbracketright=U(t,0)|a/prime/angbracketright (2.44)
for the state ket, /angbracketleftB/angbracketrightis given by
/angbracketleftB/angbracketright=(/angbracketlefta/prime|U†(t,0))·B·(U(t,0)|a/prime/angbracketright)
=/angbracketlefta/prime|exp⎧parenleftbiggiEa/primet
¯h⎧parenrightbigg
Bexp⎧parenleftbigg−iEa/primet
¯h⎧parenrightbigg
|a/prime/angbracketright
=/angbracketlefta/prime|B|a/prime/angbracketright, (2.45)
69 2.1 TimeEvolutionandtheSchrödingerEquation
which is independent of t. So the expectation value of an observable taken with respect
to an energy eigenstate does not change with time. For this reason an energy eigenstate is
often referred to as a stationary state .
The situation is more interesting when the expectation value is taken with respect to
asuperposition of energy eigenstates, or a nonstationary state . Suppose that initially
we have
|α,t0=0/angbracketright=∑
a/primeca/prime|a/prime/angbracketright. (2.46)
We easily compute the expectation value of Bto be
/angbracketleftB/angbracketright=⎧bracketleftBigg
∑
a/primec∗
a/prime/angbracketlefta/prime|exp⎧parenleftbiggiEa/primet
¯h⎧parenrightbigg⎧bracketrightBigg
·B·⎧bracketleftBigg
∑
a/prime/primeca/prime/primeexp⎧parenleftbigg−iEa/prime/primet
¯h⎧parenrightbigg
|a/prime/prime/angbracketright⎧bracketrightBigg
=∑
a/prime∑
a/prime/primec∗a/primeca/prime/prime/angbracketlefta/prime|B|a/prime/prime/angbracketrightexp⎧bracketleftbigg−i(Ea/prime/prime−Ea/prime)t
¯h⎧bracketrightbigg
. (2.47)
So this time the expectation value consists of oscillating terms whose angular frequencies
are determined by N. Bohr’s frequency condition
ωa/prime/primea/prime=(Ea/prime/prime−Ea/prime)
¯h. (2.48)
2.1.5 SpinPrecession
It is appropriate to treat an example here. We consider an extremely simple system which,however, illustrates the basic formalism we have developed.
We start with a Hamiltonian of a spin
1
2system with magnetic moment e¯h/2m ecsubjected
to an external magnetic ﬁeld B:
H=−⎧parenleftbigge
mec⎧parenrightbigg
S·B (2.49)
(e<0 for the electron). Furthermore, we take Bto be a static, uniform magnetic ﬁeld in
thez-direction. We can then write Has
H=−⎧parenleftbiggeB
mec⎧parenrightbigg
Sz. (2.50)
Because Szand Hdiffer just by a multiplicative constant, they obviously commute. The Sz
eigenstates are also energy eigenstates, and the corresponding energy eigenvalues are
E±=∓e¯hB
2m ec,f o r Sz±. (2.51)
It is convenient to deﬁne ωin such a way that the difference in the two energy eigenvalues
is¯hω:
ω≡|e|B
mec. (2.52)
70 QuantumDynamics
We can then rewrite the Hoperator simply as
H=ωSz. (2.53)
All the information on time development is contained in the time-evolution operator
U(t,0)=exp⎧parenleftbigg−iωSzt
¯h⎧parenrightbigg
. (2.54)
We apply this to the initial state. The base kets we must use in expanding the initial ket are
obviously the Szeigenkets, |+/angbracketrightand|−/angbracketright, which are also energy eigenkets. Suppose that at
t=0 the system is characterized by
|α/angbracketright=c+|+/angbracketright+c−|−/angbracketright. (2.55)
Upon applying (2.54), we see that the state ket at some later time is
|α,t0=0;t/angbracketright=c+exp⎧parenleftbigg−iωt
2⎧parenrightbigg
|+/angbracketright+c−exp⎧parenleftbigg+iωt
2⎧parenrightbigg
|−/angbracketright, (2.56)
w h e r ew eh a v eu s e d
H|±/angbracketright =⎧parenleftbigg±¯hω
2⎧parenrightbigg
|±/angbracketright. (2.57)
Speciﬁcally, let us suppose that the initial ket |α/angbracketrightrepresents the spin-up (or, more
precisely, Sz+) state|+/angbracketright, which means that
c+=1, c−=0. (2.58)
At a later time, ( 2.56) tells us that it is still in the spin-up state, which is no surprise because
this is a stationary state.
Next, let us suppose that initially the system is in the Sx+state. Comparing ( 1.110a )
with ( 2.55), we see that
c+=c−=1√
2. (2.59)
It is straightforward to work out the probabilities for the system to be found in the Sx±
state at some later time t:
|/angbracketleftS x;±|α,t0=0;t/angbracketright|2=⎧vextendsingle⎧vextendsingle⎧vextendsingle⎧vextendsingle⎧bracketleftbigg⎧parenleftbigg1
√
2⎧parenrightbigg
/angbracketleft+|±⎧parenleftbigg1√
2⎧parenrightbigg
/angbracketleft−|⎧bracketrightbigg
·⎧bracketleftbigg⎧parenleftbigg1√
2⎧parenrightbigg
exp⎧parenleftbigg−iωt
2⎧parenrightbigg
|+/angbracketright
+⎧parenleftbigg1√
2⎧parenrightbigg
exp⎧parenleftbigg+iωt
2⎧parenrightbigg
|−/angbracketright⎧bracketrightbigg⎧vextendsingle⎧vextendsingle⎧vextendsingle⎧vextendsingle2
=⎧vextendsingle⎧vextendsingle⎧vextendsingle⎧vextendsingle1
2exp⎧parenleftbigg−iωt
2⎧parenrightbigg
±1
2exp⎧parenleftbigg+iωt
2⎧parenrightbigg⎧vextendsingle⎧vextendsingle⎧vextendsingle⎧vextendsingle2
=cos2ωt
2for Sx+, (2.60a)
=sin2ωt
2for Sx−. (2.60b)
Even though the spin is initially in the positive x-direction, the magnetic ﬁeld in the
z-direction causes it to rotate; as a result, we obtain a ﬁnite probability for ﬁnding
71 2.1 TimeEvolutionandtheSchrödingerEquation
Sx−at some later time. The sum of the two probabilities is seen to be unity at all times, in
agreement with the unitarity property of the time-evolution operator.
Using (1.99), we can write the expectation value of Sxas
/angbracketleftSx/angbracketright=⎧parenleftbigg¯h
2⎧parenrightbigg
cos2⎧parenleftBigωt
2⎧parenrightBig
+⎧parenleftbigg−¯h
2⎧parenrightbigg
sin2⎧parenleftBigωt
2⎧parenrightBig
=⎧parenleftbigg¯h
2⎧parenrightbigg
cosωt, (2.61)
so this quantity oscillates with an angular frequency corresponding to the difference of
the two energy eigenvalues divided by ¯h, in agreement with our general formula ( 2.47).
Similar exercises with Syand Szshow that
/angbracketleftSy/angbracketright=⎧parenleftbigg¯h
2⎧parenrightbigg
sinωt (2.62a)
and
/angbracketleftSz/angbracketright=0. (2.62b)
Physically this means that the spin precesses in the xy-plane. We will comment further on
spin precession when we discuss rotation operators in