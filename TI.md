TI

---

Entropy (Physics): measure of the disorde in a system; the lower the order the thigher the entropy
Entropy (CS): measure of information in terms of uncertainty; the higher the uncertainty the higher the entropy.

easy definitions:
entropy: measure of uncertainty before the flip (of a coin)
Information: knowledge you have to gain after flip

Information Theory was founded by Claude Shannon in 1948, with the paper *The mathematical theory of communication*
It studies the fundamental limits in communications: transmission, storage, ecc..

<img src="/home/ludo/.config/Typora/typora-user-images/image-20210310140342670.png" alt="image-20210310140342670" style="zoom: 50%;" />

The message sent could be different from the received one.

**Key concepts**

- Information is *uncertainty*, modeled as random variables
- Information is *digital*, 1 or 0, without reference to what they represent

**Two fundamental theorems**

- Source coding theorem
  - fundamental limit in data compression, there's always a minimal size in which a file can be compressed in
- Channel coding theorem
  - fundamental limit for reliable communication through a noisy channel; no matter how smart the communication is designed for reliable communication exists a maximum rate to communicate information through the channel, *channel capacity*
  - when we store info on HDD and retrieve the info later we're communicating from past to present/future

Fundamental problem in Information Theory is: *Reliable communication over an unreliable channel*
Examples of channels: 

voice -- air --> ear
eye -- chemicals -->brain
DNA -- cose vaire --> replicazione DNA
antenna -- vacuum --> Mars rover --> earth
phone -- copper wire --> phone
disk drive -- magneized film --> yourself

common property: the recevied signal is not identical to the sent signal, due to noise

Recevied signal $\simeq$ transmitted signal
We'd like to have communications system where the received message = transmitted message

We're trying to achieve this goal.

Solutions:

- physical solutions, more copper on wire, more insulation, change physics to reduce noise
- system solutions: we accept the channel how it is, decode and encode

![image-20210310152158898](/home/ludo/.config/Typora/typora-user-images/image-20210310152158898.png)

Encoder adds redundancy
Decoder try to infers *n* and *s*.

Toy problem: binary symmetric channel

It's got an input, a binary input, 0 or 1, every time you use it. 
<img src="/home/ludo/.config/Typora/typora-user-images/image-20210310152716704.png" alt="image-20210310152716704" style="zoom:50%;" />

$P(y=0 | x=0) = 1-f = 0.9$
$P(y=1 | x=0) = f = 0.1$

Model for a disk drive:
*?Q1. A file of 10.000 bits is stored on this disk drive that flips 10% of the bits, assuming the bits are independent, how many bits are flipped?*
Using a binomial distribution:
variance: it's the square root of standard deviation
variance = $Npq = 900$ = $\sigma^2$, but we want $\sigma = \sqrt{900} = 30$
mean: $Np = N\cdot f = 10000 \cdot 0.1 = 1000$
So the answer is $1000 \pm30$

*?Q2. To have a saleable 1 GB disk dive how small does f​ need to be?*
Assuming using it for 5 years, rate of 1 GB per day, the number of bits that will be sent on channel is $8\cdot10^9 \cdot5\cdot365 \simeq10^{13} $
If we want an 1%chance of disappointment then we have to have $f=10^{-15}$
If we want 1000 happy customers the f must be $f=10^{-18}$, and that's a real number aimed for in industry.

We're assuming $f=10^{-15}$. 
*?How can we add redundancy?*
Example encoder: 

- parity coding: 01011101 | 1(bit parità)
- repetion code,  (3 times)

example with 3 repetions:

s = 01101

t = 000 111 111 000 111

n = 000 100 000 101 000 (noise)

r = 000 011 111 101 111

r = t + n mod 2

*?How should we decode this?*

- best of N (three), moda
- majority vote decoder, mean

It works a bit, but it doesn't garantee

Why is the majority vote decoder the correct decoder?
We use *inference*
Inverse probability, needs rules of probability:

1. $Product rule, P(s,r) = P(s)P(r|s) = P(r)P(s|r)$
2. Sum rule, $P(r) = \sum_{s}P(s,r) = P(s=0|r) + P(s=1|r)$

P(s|r) = poster of probability.
$= \frac{P(r|s)P(s)}{P(r)}$ 



<img src="/home/ludo/.config/Typora/typora-user-images/image-20210315121155424.png" alt="image-20210315121155424" style="zoom:33%;" />