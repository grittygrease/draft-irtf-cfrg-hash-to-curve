---
title: Hashing to Elliptic Curves
abbrev: hash-to-curve
docname: draft-irtf-cfrg-hash-to-curve-latest
date:
category: info

ipr: trust200902
keyword: Internet-Draft

stand_alone: yes
pi: [toc, sortrefs, symrefs]

author:
 -
    ins: S. Scott
    name: Sam Scott
    org: Cornell Tech
    street: 2 West Loop Rd
    city: New York, New York 10044
    country: United States of America
    email: sam.scott@cornell.edu
 -
    ins: N. Sullivan
    name: Nick Sullivan
    org: Cloudflare
    street: 101 Townsend St
    city: San Francisco
    country: United States of America
    email: nick@cloudflare.com
 -
    ins: C. A. Wood
    name: Christopher A. Wood
    org: Apple Inc.
    street: One Apple Park Way
    city: Cupertino, California 95014
    country: United States of America
    email: cawood@apple.com

normative:
  RFC2119:
  RFC5114:
  RFC5869:
  RFC6234:
  RFC7748:
  RFC8017:
  RFC8032:
  SECG1:
    title: SEC 1 -- Elliptic Curve Cryptography
    target: http://www.secg.org/sec1-v2.pdf
    authors:
      -
        ins: Standards for Efficient Cryptography Group (SECG)
        org:
  Icart09:
    title: How to Hash into Elliptic Curves
    target: https://eprint.iacr.org/2009/226.pdf
    authors:
      -
        ins: T. Icart
        org: Sagem Securite and Universite du Luxembourg
  BF01:
    title: Identity-based encryption from the Weil pairing
    authors:
      -
        ins: Dan Boneh
        org: Stanford University
      -
        ins: Matthew Franklin
        org: UC Davis
  BLS01:
    title: Short signatures from the Weil pairing
    target: https://iacr.org/archive/asiacrypt2001/22480516.pdf
    authors:
      -
        ins: Dan Boneh
        org: Stanford University
      -
        ins: Ben Lynn
        org: Stanford University
      -
        ins: Hovav Shacham
        org: Stanford University
  BMP00:
    title: Provably secure password-authenticated key exchange using diffie-hellman
    venue: EUROCRYPT, pages 156–171, 2000.
    authors:
      -
        ins: Victor Boyko
        org: MIT Laboratory for Computer Science
      -
        ins: Philip D. MacKenzie
        org: Bell Laboratories, Lucent Technologies
      -
        ins: Sarvar Patel
        org: Bell Laboratories, Lucent Technologies
  DSS:
       title: "Digital Signature Standard, version 4"
       date: 2013
       author:
         org: National Institute of Standards and Technology, U.S. Department of Commerce
       seriesinfo:
         NIST: FIPS PUB 186-4
  Jablon96:
    title: Strong password-only authenticated key exchange
    venue: SIGCOMM Comput. Commun. Rev., 26(5), 5–26, 1996.
    authors:
      -
        ins: David P. Jablon
        org: Integrity Sciences, Inc. Westboro, MA.
  hacspec:
    title: hacspec
    target: https://github.com/HACS-workshop/hacspec
  ElligatorAGL:
    title: Implementing Elligator for Curve25519
    target: https://www.imperialviolet.org/2013/12/25/elligator.html
    authors:
      -
        ins: Adam Langley
  ECOPRF:
    title: EC-OPRF - Oblivious Pseudorandom Functions using Elliptic Curves
    authors:
      -
        ins: Jonathan Burns
        org: Ionic Research
      -
        ins: Daniel Moore
        org: Ionic Research
      -
        ins: Katrina Ray
        org: Ionic Research
      -
        ins: Ryan Speers
        org: Ionic Research
      -
        ins: Brian Vohaska
        org: Ionic Research
  Elligator2:
    title: Elligator -- Elliptic-curve points indistinguishable from uniform random strings
    venue: Proceedings of the 2013 ACM SIGSAC conference on Computer & communications security. ACM, 2013.
    target: https://dl.acm.org/ft_gateway.cfm?id=2516734&type=pdf
    authors:
      -
        ins: Daniel J. Bernstein
        org: Department of Computer Science, University of Illinois at Chicago, USA
      -
        ins: Mike Hamburg
        org: Cryptography Research, a division of Rambus, USA
      -
        ins: Anna Krasnova
        org: Privacy & Identity lab, Institute for Computing and Information Sciences, Radboud University Nijmegen, The Netherlands
      -
        ins: Tanja Lange
        org: Department of Mathematics and Computer Science, Technische Universiteit Eindhoven, The Netherlands
  SW06:
    title: Construction of rational points on elliptic curves over finite fields
    venue: ANTS, volume 4076 of Lecture Notes in Computer Science, pages 510–524. Springer, 2006.
    authors:
      -
        ins: Andrew Shallue
      -
        ins: Christiaan van de Woestijne
  SWU07:
    title: Rational points on certain hyperelliptic curves over finite fields
    target: https://arxiv.org/pdf/0706.1448
    authors:
      -
        ins: Maciej Ulas
        org:
  SimpleSWU:
    title: Efficient Indifferentiable Hashing into Ordinary Elliptic Curves
    venue: Annual Cryptology Conference (pp. 237-254). Springer, Berlin, Heidelberg.
    target: https://eprint.iacr.org/2009/340.pdf
    authors:
      -
        ins: Eric Brier
        org: Ingenico
      -
        ins: Jean-Sebastien Coron
        org: Universite du Luxembourg
      -
        ins: Thomas Icart
        org: Universite du Luxembourg
      -
        ins: David Madore
        org: TELECOM-ParisTech
      -
        ins: Hugues Randriam
        org: TELECOM-ParisTech
      -
        ins: Mehdi Tibouchi
        org: Universite du Luxembourg, Ecole normale superieure
  FFSTV13:
    title: Indifferentiable deterministic hashing to elliptic and hyperelliptic curves
    authors:
      -
        ins: Reza R. Farashahi
        org: Macquarie Universit
      -
        ins: Pierre-Alain Fouque
        org: Ecole normale superieure
      -
        ins: gor E. Shparlinski
        org: Macquarie Universit
      -
        ins: Mehdi Tibouch
        org: Ecole normale superieure
      -
        ins:  J. Felipe Voloch
        org: University of Texas
  BL07:
    title: Faster addition and doubling on elliptic curves
    venue: Proceedings of the Advances in Crypotology 13th international conference on Theory and application of cryptology and information security (ASIACRYPT'07), Kaoru Kurosawa (Ed.). Springer-Verlag, Berlin, Heidelberg, 29-50.
    target: https://eprint.iacr.org/2007/286.pdf
    authors:
      -
        ins: Daniel J. Bernstein
        org: Department of Computer Science, University of Illinois at Chicago, USA
      -
        ins: Tanja Lange
        org: Department of Mathematics and Computer Science, Technische Universiteit Eindhoven, The Netherlands

  BL17:
    title: Montgomery curves and the Montgomery ladder
    target: https://eprint.iacr.org/2017/293.pdf
    authors:
      -
        ins: Daniel J. Bernstein
        org: Department of Computer Science, University of Illinois at Chicago, USA
      -
        ins: Tanja Lange
        org: Department of Mathematics and Computer Science, Technische Universiteit Eindhoven, The Netherlands
  FIPS-186-4:
    title: Digital Signature Standard (DSS), FIPS PUB 186-4, July 2013
    target: https://csrc.nist.gov/publications/detail/fips/186/4/final
    authors:
      -
        ins: National Institute for Standards and Technology
        org:

  github-repo:
    title: draft-irtf-cfrg-hash-to-curve | github.com
    target: https://github.com/chris-wood/draft-irtf-cfrg-hash-to-curve/

  SAGE:
    title: SageMath, the Sage Mathematics Software System
    authors: The Sage Developers
    target: https://www.sagemath.org

  Schoof85:
    title: Elliptic Curves Over Finite Fields and the Computation of Square Roots mod p
    authors: René Schoof
    target: https://www.ams.org/journals/mcom/1985-44-170/S0025-5718-1985-0777280-6/S0025-5718-1985-0777280-6.pdf

--- abstract

This document specifies a number of algorithms that may be used to encode or hash an
arbitrary string to a point on an Elliptic Curve.

--- middle

# Introduction {#introduction}

Many cryptographic protocols require a procedure which maps arbitrary input, e.g.,
passwords, to points on an elliptic curve (EC). Prominent examples include
Simple Password Exponential Key Exchange {{Jablon96}}, Password Authenticated
Key Exchange {{BMP00}}, Identity-Based Encryption {{BF01}} and
Boneh-Lynn-Shacham signatures {{BLS01}}.

Unfortunately for implementors, the precise mapping which is suitable for a
given scheme is not necessarily included in the description of the protocol.
Compounding this problem is the need to pick a suitable curve for the specific
protocol.

This document aims to address this lapse by providing a thorough set of
recommendations across a range of implementations, and curve types. We provide
implementation and performance details for each mechanism, along with references
to the security rationale behind each recommendation and guidance for
applications not yet covered.

Each algorithm conforms to a common interface, i.e., it maps a bitstring
{0, 1}^\* to a point on an elliptic curve E. For each variant, we describe the requirements for
E to make it work. Sample code for each variant is presented in the
appendix.  Unless otherwise stated, all elliptic curve points are assumed to be
represented as affine coordinates, i.e., (x, y) points on a curve.

## Requirements

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT",
"SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this
document are to be interpreted as described in {{RFC2119}}.


# Background {#background}

Here we give a brief definition of elliptic curves, with an emphasis
on defining important parameters and their relation to encoding.

Let F be the finite field GF(p^k). We say that F is a field of characteristic
p. For most applications, F is a prime field, in which case k=1 and we will
simply write GF(p).

Elliptic curves can be represented by equations of different standard forms,
including, but not limited to: Weierstrass, Montgomery, and Edwards. Each
of these variants correspond to a different category of curve equation.
For example, the short Weierstrass equation is
`y^2 = x^3 + Ax + B`. Certain encoding functions may have requirements
on the curve form, the characteristic of the field, and the parameters, such as A and B in the previous example.

An elliptic curve E is specified by its equation, and a finite field F.
The curve E forms a group, whose elements correspond to those who satisfy the
curve equation, with values taken from the field F. As a group, E has order
n, which is the number of points on the curve. For security reasons, it is a
strong requirement that all cryptographic operations take place in a prime
order group. However, not all elliptic curves generate groups of prime order.
In those cases, it is allowed to work with elliptic curves of order n = qh,
where q is a large prime, and h is a short number known as the cofactor.
Thus, we may wish an encoding that returns points on the subgroup of order q.
Multiplying a point P on E by the cofactor h guarantees that hP is a point in
the subgroup of order q.

Summary of quantities:

| Symbol | Meaning | Relevance
|:------:|---------|----------
| p | Order of finite field, F = GF(p) | Curve points need to be represented in terms of p. For prime power extension fields, we write F = GF(p^k).
| n | Number of curve points, #E(F) = n |  For map to E, needs to produce n elements.
| q | Order of the largest prime subgroup of E, n = qh | If n is not prime, may need mapping to q.
| h | Cofactor | For mapping to subgroup, need to multiply by cofactor.

## Terminology {#terminology}

In the following, we categorize the terminology for mapping bitstrings to
points on elliptic curves.

### Encoding {#term-encoding}

In practice, the input of a given cryptographic algorithm will be a bitstring of
arbitrary length, denoted {0, 1}^\*. Hence, a concern for virtually all protocols
involving elliptic curves is how to convert this input into a curve point.
The general term "encoding" refers to the process of producing an
elliptic curve point given as input a bitstring. In some protocols, the original
message may also be recovered through a decoding procedure. An encoding may be deterministic
or probabilistic, although the latter is problematic in potentially leaking
plaintext information as a side-channel.

Suppose as the input to the encoding function we wish to use a fixed-length
bitstring of length L. Comparing sizes of the sets, 2^L and n,
an encoding function cannot be both deterministic and bijective.
We can instead use an injective encoding from {0, 1}^L to E, with
`L < log2(n)- 1`,  which is a bijection over a subset of points in E.
This ensures that encoded plaintext messages can be recovered.

In practice, encodings are commonly injective and invertible. Injective encodings map
inputs to a subset of points on the curve. Invertible encodings allow computation of
input bitstrings given a point on the curve.

### Serialization {#term-serialization}

A related issue is the conversion of an elliptic curve point to a bitstring. We
refer to this process as "serialization", since it is typically used for
compactly storing and transporting points, or for producing canonicalized
outputs. Since a deserialization algorithm can often be used as a type of
encoding algorithm, we also briefly document properties of these functions.

A straightforward serialization algorithm maps a point (x, y) on E to a bitstring of length
2\*log(p), given that x, y are both elements in GF(p). However, since
there are only n points in E (with n approximately equal to p), it is possible
to serialize to a bitstring of length log(n). For example, one common method
is to store the x-coordinate and a single bit to determine whether the point
is (x, y) or (x, -y), thus requiring log(p)+1 bits. This method reduces storage,
but adds computation, since the deserialization process must recover the y
coordinate.

### Random Oracle {#term-rom}

It is often the case that the output of the encoding function {{term-encoding}}
should be (a) distributed uniformly at random on the elliptic curve and (b) non-invertible.
That is, there is no discernible relation existing between outputs that can be computed
based on the inputs. Moreover, given such an encoding function F from bitstrings to
points on the curve, as well as a single point y, it is computationally intractable to
produce an input x that maps to a y via F. In practice, these requirement stem from needing
a random oracle which outputs elliptic curve points:  one way to construct this is by first
taking a regular random oracle, operating entirely on bitstrings, and applying a
suitable encoding function to the output.

This motivates the term "hashing to the curve", since cryptographic hash
functions are typically modeled as random oracles. However, this still leaves open
the question of what constitutes a suitable encoding method, which is a primary
concern of this document.

A random oracle onto an elliptic curve can also be instantiated using
direct constructions, however these tend to rely on many group operations
and are less efficient than hash and encode methods.


# Algorithm Recommendations {#recommendations}

In practice, two types of mappings are common: (1) Injective encodings, as can be used to
construct a PRF as F(k, m) = k\*H(m), and (2) Random Oracles, as required by PAKEs {{BMP00}},
BLS {{BLS01}}, and IBE {{BF01}}. (Some applications, such as IBE, have additional requirements,
such as a Supersingular, pairing-friendly curve.)

The following table lists recommended algorithms for different curves and mappings. To select
a suitable algorithm, choose the mapping associated with the target curve. For example,
Elligator2 is the recommended injective encoding function for Curve25519, whereas Simple SWU
is the recommended injective encoding for P-256. Similarly, the FFSTV Random Oracle construction
described in {{ffstv}} composed with Elligator2 should be used for Random Oracle mappings
to Curve25519. When the required mapping is not clear, applications SHOULD use a Random Oracle.

| Curve  | Inj. Encoding | Random Oracle |
|--------|---------------|------|
| P-256 | Simple SWU {{simple-swu}} | FFSTV(SWU) {{ffstv}}
| P-384 | Icart {{icart}} | FFSTV(Icart) {{ffstv}}
| Curve25519 | Elligator2 {{elligator2}} | FFSTV(Elligator2) {{ffstv}}
| Curve448 | Elligator2 {{elligator2}} | FFSTV(Elligator2) {{ffstv}}

# Utility Functions {#utility}

Algorithms in this document make use of utility functions described below.

- HashToBase(x, i).
  This method is parametrized by p and H, where p is the prime order of
  the base field Fp, and H is a cryptographic hash function which
  outputs at least floor(log2(p)) + 2 bits.
  The function first hashes x, converts the result to an integer,
  and reduces modulo p to give an element of Fp.

  We provide a more detailed algorithm in {{hashtobase}}. The value of i is used
  to separate inputs when used multiple times in one algorithm (see {{ffstv}}
  for example). When i is omitted, we set it to 0.

- CMOV(a, b, c): If c = 1, return a, else return b.

  Common software implementations of constant-time selects assume c = 1 or c = 0. CMOV
  may be implemented by computing the desired selector (0 or 1) by ORing all bits of c
  together. The end result will be either 0 if all bits of c are zero, or 1 if at least
  one bit of c is 1.

- CTEQ(a, b): Returns a == b.
  Inputs a and b must be the same length (as bytestrings) and the comparison
  must be implemented in constant time.

- Legendre(x, p): x^((p-1)/2).
  The Legendre symbol computes whether the value x is a "quadratic
  residue" modulo p, and takes values 1, -1, 0, for when x is a residue,
  non-residue, or zero, respectively. Due to Euler's criterion, this can be
  computed in constant time, with respect to a fixed p, using
  the equation x^((p-1)/2). For clarity, we will generally prefer using the
  formula directly, and annotate the usage with this definition.

- sqrt(x, p):
  Computing square roots should be done in constant time where possible.

  When p = 3 (mod 4), the square root can be computed as `sqrt(x, p) := x^(p+1)/4`.
  This applies to P256, P384, and Curve448.

  When p = 5 (mod 8), the square root can be computed by the following
  algorithm, in which `sqrt(-1)` is a field element and can be precomputed.
  This applies to Curve25519.

~~~
  sqrt(x, p) :=
                 x^(p+3)/8     if x^(p+3)/4 == x
      sqrt(-1) * x^(p+3)/8     otherwise
~~~

  The above two conditions hold for most practically used curves, due to the
  simplicity of the square root function. For others, a suitable constant-time
  Tonelli-Shanks variant should be used as in {{Schoof85}}.

# Deterministic Encodings

## Interface

The generic interface for deterministic encoding functions to elliptic curves is as follows:

~~~
map2curve(alpha)
~~~

where alpha is a message to encode on a curve.

## Encoding Variants

As a rough style guide for the following, we use (x, y) to be the output
coordinates of the encoding method. Indexed values are used when the algorithm
will choose between candidate values. For example, the SWU algorithm computes
three candidates (x1, y1), (x2, y2), (x3, y3), from which the final (x, y)
output is chosen via constant time comparison operations.

We use u, v to denote the values in Fp output from HashToBase, and use as
initial values in the encoding.

We use t1, t2, ..., as reusable temporary variables. For notable variables, we
will use a distinct name, for ease of debugging purposes when correlating with
test vectors.

The code presented here corresponds to the example Sage {{SAGE}} code found at
{{github-repo}}. Which is additionally used to generate intermediate test
vectors. The Sage code is also checked against the hacspec implementation.

### Icart Method {#icart}

The following map2curve_icart(alpha) implements the Icart method from {{Icart09}}.
This algorithm works for any curve over F_{p^n}, where p^n = 2 mod 3
(or p = 2 mod 3 and for odd n), including:

- P384
- Curve1174
- Curve448

Unsupported curves include: P224, P256, P521, and Curve25519 since,
for each, p = 1 mod 3.

Mathematically, given input alpha, and A and B from E, the Icart method works
as follows:

~~~
u = HashToBase(alpha)
v = ((3A - u^4) / 6u)
x = (v^2 - B - (u^6 / 27))^(1/3) + (u^2 / 3)
y = ux + v
~~~

The following procedure implements this algorithm in a straight-line fashion.
It requires knowledge of A and B, the constants from the curve Weierstrass form.
It outputs a point with affine coordinates.

~~~
map2curve_icart(alpha)

Input:

  alpha - value to be hashed, an octet string

Output:

  (x, y) - a point in E

Precomputations:

1. c1 = (2 * p) - 1
2. c1 = c1 / 3               // c1 = (2p-1)/3 as integer
3  c2 = 3^(-1)               // c2 = 1/3 (mod p)
4. c3 = c2^3                 // c3 = 1/27 (mod p)

Steps:

1.   u = HashToBase(alpha)   // {0,1}^* -> Fp
2.  u2 = u^2                 // u^2
3.  u4 = u2^2                // u^4
4.   v = 3 * A               // 3A in Fp
5.   v = v - u4              // 3A - u^4
6.  t1 = 6 * u               // 6u
7.  t1 = t1^(-1)             // modular inverse
8.   v = v * t1              // (3A - u^4)/(6u)
9.  x1 = v^2                 // v^2
10. x1 = x - B               // v^2 - B
11. u6 = u4 * c3             // u^4 / 27
12. u6 = u6 * u2             // u^6 / 27
13. x1 = x1 - u6             // v^2 - B - u^6/27
14. x1 = x^c1                // (v^2 - B - u^6/27) ^ (1/3)
15. t1 = u2 * c2             // u^2 / 3
16.  x = x + t1              // (v^2 - B - u^6/27) ^ (1/3) + (u^2 / 3)
17.  y = u * x               // ux
18.  y = y + v               // ux + v
19. Output (x, y)
~~~

### Shallue-Woestijne-Ulas Method {#swu}

The Shallue-Woestijne-Ulas (SWU) method, originated in part by
Shallue and Woestijne {{SW06}} and later simplified and extended by Ulas {{SWU07}},
deterministically encodes an arbitrary string to a point on a curve.
This algorithm works for any curve over F_{p^n}. Given curve equation
g(x) = x^3 + Ax + B, with A non-zero, this algorithm works as follows:

~~~
1.  u = HashToBase(alpha, 0)
2.  v = HashToBase(alpha, 1)
3. x1 = v
4. x2 = (-B / A)(1 + 1 / (u^4 * g(v)^2 + u^2 * g(v)))
5. x3 = u^2 * g(v)^2  * g(x2)
6. If g(x1) is square, output (x1, sqrt(g(x1)))
7. If g(x2) is square, output (x2, sqrt(g(x2)))
8. Output (x3, sqrt(g(x3)))
~~~

The algorithm relies on the following equality:

~~~
u^3 * g(v)^2  * g(x2) = g(x1) * g(x2) * g(x3)
~~~

The algorithm computes three candidate points, constructed such that at least one of
them lies on the curve.

The following procedure implements this algorithm. It outputs a point with affine
coordinates. It requires knowledge of A and B, the constants from the curve
Weierstrass form.

~~~
map2curve_swu(alpha)

Input:

  alpha - value to be hashed, an octet string

Output:

  (x, y) - a point in E

Precomputations:

1.  c1 = A^(-1)                 // 1 / A (mod p)
2.  c1 = -B * c0                // c1 = -B/A (mod p)
3.  c2 = (p - 1)/2              // Order over 2 as an integer

Steps:

1.    u = HashToBase(alpha, 0)  // {0,1}^* -> Fp
2.    v = HashToBase(alpha, 1)  // {0,1}^* -> Fp
3.   x1 = v                     // x1 = v
4.   gv = v^3
5.   gv = gv + (A * v)
6.   gv = gv + B                // gv = g(v)
7.  gx1 = gv                    // gx1 = g(x1)
8.   u2 = u^2
9.   t1 = u2 * gv               // t1 = u^2 * g(v)
10.  t2 = t1^2
11.  t2 = t2 + t1
12.  t2 = t2^(-1)               // t2 = 1/(u^4*g(v)^2 + u^2*g(v))
13.  n1 = 1 + t2
14.  x2 = c1 * n1               // x2 = -B/A * (1 + 1/(t1^2 + t1))
15. gx2 = x2^3
16.  t2 = A * x2
17. gx2 = gx2 + t2
18. gx2 = gx2 + B               // gx2 = g(x2)
19.  x3 = x2 * t1               // x3 = x2 * u^2 * g(v)
20. gx3 = x3^3
21. gx3 = gx3 + (A * x3)
22. gx3 = gx3 + B               // gx3 = g(X3(t, u))
23.  l1 = gx1^c2                // Legendre(gx1)
24.  l2 = gx2^c2                // Legendre(gx2)
25.  y1 = sqrt(gx1)             // TODO: Specify square root properly
26.  y2 = sqrt(gx2)             // TODO: Specify square root properly
27.  y3 = sqrt(gx3)             // TODO: Specify square root properly
28.  x  = CMOV(x2, x3, l2)      // If l2 = 1, choose x2, else choose x3
29.  y  = CMOV(y2, y3, l2)      // If l2 = 1, choose y2, else choose y3
30.  x  = CMOV(x1, x, l1)       // If l1 = 1, choose x1, else choose x
31.  y  = CMOV(y1, y, l1)       // If l1 = 1, choose y1, else choose y
32. Output (x, y)
~~~

### Simplified SWU Method {#simple-swu}

The following map2curve_simple_swu(alpha) implements the simplified
Shallue-Woestijne-Ulas algorithm from {{SimpleSWU}}. This algorithm
works for any curve over F_{p^n}, where p = 3 mod 4, including:

- P256
- ...

Given curve equation g(x) = x^3 + Ax + B, this algorithm works as follows:

~~~
1. u = HashToBase(alpha)
2. x1 = -B/A * (1 + (1 / (u^4 - u^2)))
3. x2 = −u^2 * x1
4. If g(x1) is square, output (x1, sqrt(g(x1)))
5. Output (x2, sqrt(g(x2)))
~~~

The following procedure implements this algorithm. It outputs a point with
affine coordinates. It requires knowledge of A and B, the constants from the
curve Weierstrass form.

~~~
map2curve_simple_swu(alpha)

Input:

  alpha - value to be encoded, an octet string

Output:

  (x, y) - a point in E

Precomputations:

1.  c1 = A^(-1)                 // 1 / A (mod p)
2.  c1 = -B * c0                // c1 = -B/A (mod p)
3.  c2 = (p - 1)/2              // Order over 2 as an integer

Steps:

1.    u = HashToBase(alpha, 0)  // {0,1}^* -> Fp
2.   u2 = u^2
3.   u2 = -u2                   // u2 = -u^2
4.   u4 = u2^2
5.   t1 = u4 + u2
6.   t1 = t1^(-1)
7.   n1 = 1 + t2                // n1 = 1 + (1 / (u^4 - u^2))
8.   x1 = c1 * n1               // x1 = -B/A * (1 + (1 / (u^4 - u^2)))
9.  gx1 = x1 ^ 3
10.  t1 = A * x1
11. gx1 = gx1 + t1
12. gx1 = gx1 + B               // gx1 = x1^3 + Ax1 + B = g(x1)
13.   x2 = u2 * x1              // x2 = -u^2 * x1
14.  gx2 = x2^3
15.   t1 = A * x2
16.  gx2 = gx2 + 12
17.  gx2 = gx2 + B              // gx2 = x2^3 + Ax2 + B = g(x2)
18.   e = gx1^c2
19   y1 = sqrt(gx1)             // TODO: Specify square root properly
20   y2 = sqrt(gx2)             // TODO: Specify square root properly
21.  x  = CMOV(x1, x2, l1)      // If l1 = 1, choose x1, else choose x2
22.  y  = CMOV(y1, y2, l1)      // If l1 = 1, choose y1, else choose y2
23. Output (x, y)
~~~

### Elligator2 Method {#elligator2}

The following map2curve_elligator2(alpha) implements the Elligator2
method from {{Elligator2}}. This algorithm works for any curve
with a point of order 2 and j-invariant != 1728. Given curve equation
y^2 = g(x) = x(x^2 + Ax + B), i.e., a Montgomery form with (0,0), a point of
order 2, this algorithm works as shown below. (Note that any curve
with a point of order 2 is isomorphic to this representation.)

The algorithm additionally requires a constant value N, which is a non-square
in Fp. For performance this is typically small in absolute size.

~~~
1. u = HashToBase(alpha)
2. v = -A/(1 + N*u^2)
3. e = Legendre(g(v))
4.1. If u != 0, then
4.2.    x = ev - (1 - e)A/2
4.3.    y = -e*sqrt(g(x))
4.4. Else, x=0 and y=0
5. Output (x,y)
~~~

Here, e is the Legendre symbol defined as in {{utility}}.

The following procedure implements this algorithm.

~~~
map2curve_elligator2(alpha)

Input:

  alpha - value to be encoded, an octet string
  N - fixed non-square value in Fp.

Output:

  (x, y) - a point in E

Precomputations:

1. c1 = (p - 1)/2     // as an integer
2. c2 = A / 2 (mod p) // in the field

Steps:

1.   u = HashToBase(alpha)
2.  t1 = u^2
3.  t1 = N * t1
4.  t1 = 1 + t1
5.  t1 = t1^(-1)
6.   v = A * t1
7.   v = -v               // v = -A / (1 + N * u^2)
8.  gv = v + A
9.  gv = gv * v
0.  gv = gv + B
11. gv =  gv * v          // gv = v^3 + Av^2 + Bv
12.  e = gv^c1            // Legendre(gv)
13.  x = e*v
14. ne = -e
15. t1 = 1 + ne
16. t1 = t1 * c2
17.  x = x - t1           // x = ev - (1 - e)*A/2
18.  y = x + A
19.  y = y * x
20.  y = y + B
21.  y = y * x
22.  y = sqrt(y)          // TODO: Specify square root properly
23.  y = y * ne            // y = -e * sqrt(x^3 + Ax^2 + Bx)
24.  x = CMOV(0, x, 1-u)
25.  y = CMOV(0, y, 1-u)
26. Output (x, y)
~~~

Elligator2 can be simplified with projective coordinates.

((TODO: write this variant))

## Cost Comparison

The following table summarizes the cost of each map2curve variant. We express this cost in
terms of additions (A), multiplications (M), squares (SQ), and square roots (SR).

((TODO: finish this section))

| Algorithm | Cost (Operations) |
| map2curve_icart | TODO |
| map2curve_swu | TODO |
| map2curve_simple_swu | TODO |
| map2curve_elligator2 | TODO |

# Random Oracles

## Interface

The generic interface for deterministic encoding functions to elliptic curves is as follows:

~~~
hash2curve(alpha)
~~~

where alpha is a message to encode on a curve.

## General Construction (FFSTV13) {#ffstv}

When applications need a Random Oracle (RO), they can be constructed from deterministic encoding
functions. In particular, let F : {0,1}^* -> E be a deterministic encoding function onto
curve E, and let H0 and H1 be two hash functions modeled as random oracles that map input
messages to the base field of E, i.e., Z_q. Farashahi et al. {{FFSTV13}} showed that the
following mapping is indistinguishable from a RO:

~~~
hash2curve(alpha) = F(H0(alpha)) + F(H1(alpha))
~~~

This construction works for the Icart, SWU, and Simplfied SWU encodings.

Here, H0 and H1 are constructed as follows:

~~~
H0(alpha) = HashToBase(alpha, 2)
H1(alpha) = HashToBase(alpha, 3)
~~~

# Curve Transformations

Every elliptic curve can be converted to an equivalent curve in short Weierstrass form
({{BL07}} Theorem 2.1), making SWU a generic algorithm that can be used for all curves.
Curves in either Edwards or Twisted Edwards form can be transformed into equivalent
curves in Montgomery form {{BL17}} for use with Elligator2.
{{RFC7748}} describes how to convert between points on Curve25519 and Ed25519,
and between Curve448 and its Edwards equivalent, Goldilocks.

# Ciphersuites

To provide concrete recommendations for algorithms we define a hash-to-curve
"ciphersuite" as a four-tuple containing:

* Destination Group (e.g. P256 or Curve25519)
* HashToBase algorithm
* HashToCurve algorithm (e.g. SSWU, Icart)
* (Optional) Transformation (e.g. FFSTV, cofactor clearing)

A ciphersuite defines an algorithm that takes an arbitrary octet string and
returns an element of the Destination Group defined in the ciphersuite by applying
HashToCurve and Transformation (if defined).

This document describes the following set of ciphersuites:
* H2C-P256-SHA256-SSWU-
* H2C-P384-SHA512-Icart-
* H2C-Curve25519-SHA512-Elligator2-Clear
* H2C-Curve448-SHA512-Elligator2-Clear
* H2C-Curve25519-SHA512-Elligator2-FFSTV
* H2C-Curve448-SHA512-Elligator2-FFSTV

H2C-P256-SHA256-SWU- is defined as follows:

* The destination group is the set of points on the NIST P-256 elliptic curve, with
  curve parameters as specified in {{DSS}} (Section D.1.2.3) and
  {{RFC5114}} (Section 2.6).
* HashToBase is defined as {#hashtobase} with the hash function defined as
  SHA-256 as specified in {{RFC6234}}, and p set to the prime field used in
  P-256 (2^256 - 2^224 + 2^192 + 2^96 - 1).
* HashToCurve is defined to be {#sswu} with A and B taken from the definition of P-256
  (A=-3, B=41058363725152142129326129780047268409114441015993725554835256314039467401291).

H2C-P384-SHA512-Icart- is defined as follows:

* The destination group is the set of points on the NIST P-384 elliptic curve, with
  curve parameters as specified in {{DSS}} (Section D.1.2.4) and
  {{RFC5114}} (Section 2.7).
* HashToBase is defined as {#hashtobase} with the hash function defined as
  SHA-512 as specified in {{RFC6234}}, and p set to the prime field used in
  P-384 (2^384 - 2^128 - 2^96 + 2^32 - 1).
* HashToCurve is defined to be {#icart} with A and B taken from the definition of P-384
  (A=-3, B=27580193559959705877849011840389048093056905856361568521428707301988689241309860865136260764883745107765439761230575).

H2C-Curve25519-SHA512-Elligator2-Clear is defined as follows:

* The destination group is the points on Curve25519, with
  curve parameters as specified in {{RFC7748}} (Section 4.1).
* HashToBase is defined as {#hashtobase} with the hash function defined as
  SHA-512 as specified in {{RFC6234}}, and p set to the prime field used in
  Curve25519 (2^255 - 19).
* HashToCurve is defined to be {#elligator2} with the curve function defined
  to be the Montgomery form of Curve25519 (y^2 = x^3 + 486662x^2 + x) and
  N = 2.
* The final output is multiplied by the cofactor of Curve25519, 8.

H2C-Curve448-SHA512-Elligator2-Clear is defined as follows:

* The destination group is the points on Curve448, with
  curve parameters as specified in {{RFC7748}} (Section 4.1).
* HashToBase is defined as {#hashtobase} with the hash function defined as
  SHA-512 as specified in {{RFC6234}}, and p set to the prime field used in
  Curve448 (2^448 - 2^224 - 1).
* HashToCurve is defined to be {#elligator2} with the curve function defined
  to be the Montgomery form of Curve448 (y^2 = x^3 + 156326x^2 + x) and
  N = -1.
* The final output is multiplied by the cofactor of Curve448, 4.

H2C-Curve25519-SHA512-Elligator2-FFSTV is defined as in H2C-Curve25519-SHA-512-Elligator2-Clear
except HashToCurve is defined to be {#ffstv} where F is {#elligator2}.

H2C-Curve448-SHA512-Elligator2-FFSTV is defined as in H2C-Curve448-SHA-512-Elligator2-Clear
except HashToCurve is defined to be {#ffstv} where F is {#elligator2}.

# IANA Considerations

This document has no IANA actions.

# Security Considerations

Each encoding function variant accepts arbitrary input and maps it to a pseudorandom
point on the curve. Points are close to indistinguishable from randomly chosen
elements on the curve. Not all encoding functions are full-domain hashes. Elligator2,
for example, only maps strings to "about half of all curve points," whereas Icart's
method only covers about 5/8 of the points.

# Acknowledgements

The authors would like to thank Adam Langley for this detailed writeup up Elligator2 with
Curve25519 {{ElligatorAGL}}. We also thank Sean Devlin and Thomas Icart for feedback on
earlier versions of this document.

# Contributors

* Sharon Goldberg \\
  Boston University \\
  goldbe@cs.bu.edu

--- back


# Related Work {#related}

In this chapter, we  give a background to some common methods to encode or
hash to the curve, motivated by the similar exposition in {{Icart09}}.
Understanding of this material is not required in order to choose a
suitable encoding function - we defer this to {{recommendations}}
 - the background covered here can work as a template for analyzing encoding
functions not found in this document, and as a guide for further research
into the topics covered.

## Probabilistic Encoding

As mentioned in {{background}}, as a rule of thumb, for every x in GF(p), there
is approximately a 1/2 chance that there exist a corresponding y value such that
(x, y) is on the curve E.

This motivates the construction of the MapToGroup
method described by Boneh et al. {{BLS01}}. For an input message m, a counter i,
and a standard hash function H : {0, 1}^* -> GF(p) x {0, 1}, one computes (x, b)
= H(i || m), where i || m denotes concatenation of the two values. Next, test to
see whether there exists a corresponding y value such that (x, y) is on the
curve, returning (x, y) if successful, where b determines whether to take +/- y.
If there does not exist such a y, then increment i and repeat. A maximum counter
value is set to I, and since each iteration succeeds with probability
approximately 1/2, this process fails with probability 2^-I. (See {{try}} for a
more detailed description of this algorithm.)

Although MapToGroup describes a method to hash to the curve, it can also be
adapted to a simple encoding mechanism. For a bitstring of length strictly
less than log2(p), one can make use of the spare bits in order to encode
the counter value. Allocating more space for the counter increases the expansion,
but reduces the failure probability.

Since the running time of the MapToGroup algorithm depends on m,
this algorithm is NOT safe for cases sensitive to timing side channel attacks.
Deterministic algorithms are needed in such cases where failures
are undesirable.

## Naive Encoding

A naive solution includes computing H(m)\*G as map2curve(m), where H is a standard hash
function H : {0, 1}^* -> GF(p), and G is a generator of the curve. Although
efficient, this solution is unsuitable for constructing a random oracle onto
E, since the discrete logarithm with respect to G is known. For example,
given y1 = map2curve(m1) and y2 = map2curve(m2) for any m1 and m2, it must
be true that y2 = H(m2) / H(m1) * map2curve(m1). This relationship would not
hold (with overwhelming probability) for truly random values y1 and y2.
This causes catastrophic failure in many cases. However, one exception is found in
SPEKE {{Jablon96}}, which constructs a base for a Diffie-Hellman key exchange by
hashing the password to a curve point. Notably the use of a hash function is
purely for encoding an arbitrary length string to a curve point, and does not
need to be a random oracle.

## Deterministic Encoding

Shallue, Woestijne, and Ulas {{SW06}} first introduced a deterministic
algorithm that maps elements in F_{q} to a curve in time O(log^4 q), where q = p^n for
some prime p, and time O(log^3 q) when q = 3 mod 4. Icart introduced yet another
deterministic algorithm which maps F_{q} to any EC where q = 2 mod 3 in time O(log^3 q) {{Icart09}}.
Elligator (2) {{Elligator2}} is yet another deterministic algorithm for any odd-characteristic
EC that has a point of order 2. Elligator2 can be applied to Curve25519 and Curve448, which
are both CFRG-recommended curves {{RFC7748}}.

However, an important caveat to all of the above deterministic encoding functions,
is that none of them map injectively to the entire curve, but rather
some fraction of the points. This makes them unable to use to directly
construct a random oracle on the curve.

Brier et al. {{SimpleSWU}} proposed a couple of solutions to this problem, The
first applies solely to Icart's method described above, by computing F(H0(m))
+ F(H1(m)) for two distinct hash functions H0, H1. The second uses a generator
G, and computes F(H0(m)) + H1(m)\*G. Later, Farashahi et al. {{FFSTV13}}
showed the generality of the F(H0(m)) + F(H1(m)) method, as well as the
applicability to hyperelliptic curves (not covered here).

## Supersingular Curves

For supersingular curves, for every y in GF(p) (with p>3), there exists a value
x such that (x, y) is on the curve E. Hence we can construct a bijection
F : GF(p) -> E (ignoring the point at infinity). This is the case for
{{BF01}}, but is not common.

## Twisted Variants

We can also consider curves which have twisted variants, E^d. For such curves,
for any x in GF(p), there exists y in GF(p) such that (x, y) is either a point
on E or E^d. Hence one can construct a bijection F : GF(p) x {0,1} -> E ∪ E^d,
where the extra bit is needed to choose the sign of the point. This can be
particularly useful for constructions which only need the x-coordinate of the
point. For example, x-only scalar multiplication can be computed on Montgomery
curves. In this case, there is no need for an encoding function, since the output
of F in GF(p) is sufficient to define a point on one of E or E^d.

# Try-and-Increment Method {#try}

In cases where constant time execution is not required, the so-called
try-and-increment method may be appropriate. As discussion in {{introduction}},
this variant works by hashing input m using a standard hash function ("Hash"), e.g., SHA256, and
then checking to see if the resulting point (m, f(m)), for curve function f, belongs on E.
This is detailed below.

~~~
1. ctr = 0
2. h = "INVALID"
3. While h is "INVALID" or h is EC point at infinity:
4.1   CTR = I2OSP(ctr, 4)
4.2   ctr = ctr + 1
4.3   attempted_hash = Hash(m || CTR)
4.4   h = RS2ECP(attempted_hash)
4.5   If h is not "INVALID" and cofactor > 1, set h = h * cofactor
5. Output h
~~~

I2OSP is a function that converts a nonnegative integer to octet string as
defined in Section 4.1 of {{RFC8017}}, and RS2ECP(h) = OS2ECP(0x02 || h), where
OS2ECP is specified in Section 2.3.4 of {{SECG1}}, which converts an input
string into an EC point.

# Sample Code {#samplecode}

This section contains reference implementations for each map2curve variant built
using {{hacspec}}.

## Icart Method

The following hacspec program implements map2curve_icart(alpha) for P-384.

~~~
from hacspec.speclib import *

prime = 2**384 - 2**128 - 2**96 + 2**32 - 1

felem_t = refine(nat, lambda x: x < prime)
affine_t = tuple2(felem_t, felem_t)

@typechecked
def to_felem(x: nat_t) -> felem_t:
    return felem_t(nat(x % prime))


@typechecked
def fadd(x: felem_t, y: felem_t) -> felem_t:
    return to_felem(x + y)


@typechecked
def fsub(x: felem_t, y: felem_t) -> felem_t:
    return to_felem(x - y)


@typechecked
def fmul(x: felem_t, y: felem_t) -> felem_t:
    return to_felem(x * y)


@typechecked
def fsqr(x: felem_t) -> felem_t:
    return to_felem(x * x)


@typechecked
def fexp(x: felem_t, n: nat_t) -> felem_t:
    return to_felem(pow(x, n, prime))


@typechecked
def finv(x: felem_t) -> felem_t:
    return to_felem(pow(x, prime-2, prime))

a384 = to_felem(prime - 3)
b384 = to_felem(27580193559959705877849011840389048093056905856361568521428707301988689241309860865136260764883745107765439761230575)

@typechecked
def map2p384(u:felem_t) -> affine_t:
    v = fmul(fsub(fmul(to_felem(3), a384), fexp(u, 4)), finv(fmul(to_felem(6), u)))
    u2 = fmul(fexp(u, 6), finv(to_felem(27)))
    x = fsub(fsqr(v), b384)
    x = fsub(x, u2)
    x = fexp(x, (2 * prime - 1) // 3)
    x = fadd(x, fmul(fsqr(u), finv(to_felem(3))))
    y = fadd(fmul(u, x), v)
    return (x, y)
~~~

## Shallue-Woestijne-Ulas Method

The following hacspec program implements map2curve_swu(alpha) for P-256.

~~~
from p256 import *
from hacspec.speclib import *

a256 = to_felem(prime - 3)
b256 = to_felem(41058363725152142129326129780047268409114441015993725554835256314039467401291)

@typechecked
def f_p256(x:felem_t) -> felem_t:
    return fadd(fexp(x, 3), fadd(fmul(to_felem(a256), x), to_felem(b256)))

@typechecked
def x1(t:felem_t, u:felem_t) -> felem_t:
    return u

@typechecked
def x2(t:felem_t, u:felem_t) -> felem_t:
    coefficient = fmul(to_felem(-b256), finv(to_felem(a256)))
    t2 = fsqr(t)
    t4 = fsqr(t2)
    gu = f_p256(u)
    gu2 = fsqr(gu)
    denom = fadd(fmul(t4, gu2), fmul(t2, gu))
    return fmul(coefficient, fadd(to_felem(1), finv(denom)))

@typechecked
def x3(t:felem_t, u:felem_t) -> felem_t:
    return fmul(fsqr(t), fmul(f_p256(u), x2(t, u)))

@typechecked
def map2p256(t:felem_t) -> felem_t:
    u = fadd(t, to_felem(1))
    x1v = x1(t, u)
    x2v = x2(t, u)
    x3v = x3(t, u)

    exp = to_felem((prime - 1) // 2)
    e1 = fexp(f_p256(x1v), exp)
    e2 = fexp(f_p256(x2v), exp)

    if e1 == 1:
        return x1v
    elif e2 == 1:
        return x2v
    else:
        return x3v
~~~

## Simplified SWU Method {#sswu}

The following hacspec program implements map2curve_simple_swu(alpha) for P-256.

~~~
from p256 import *
from hacspec.speclib import *

a256 = to_felem(prime - 3)
b256 = to_felem(41058363725152142129326129780047268409114441015993725554835256314039467401291)

def f_p256(x:felem_t) -> felem_t:
    return fadd(fexp(x, 3), fadd(fmul(to_felem(a256), x), to_felem(b256)))

def map2p256(t:felem_t) -> affine_t:
    alpha = to_felem(-(fsqr(t)))
    frac = finv((fadd(fsqr(alpha), alpha)))
    coefficient = fmul(to_felem(-b256), finv(to_felem(a256)))
    x2 = fmul(coefficient, fadd(to_felem(1), frac))

    x3 = fmul(alpha, x2)
    h2 = fadd(fexp(x2, 3), fadd(fmul(a256, x2), b256))
    h3 = fadd(fexp(x3, 3), fadd(fmul(a256, x3), b256))

    exp = fmul(fadd(to_felem(prime), to_felem(-1)), finv(to_felem(2)))
    e = fexp(h2, exp)

    exp = to_felem((prime + 1) // 4)
    if e == 1:
      return (x2, fexp(f_p256(x2), exp))
    else:
      return (x3, fexp(f_p256(x3), exp))
~~~

## Elligator2 Method

The following hacspec program implements map2curve_elligator2(alpha) for Curve25519.

~~~
from curve25519 import *
from hacspec.speclib import *

a25519 = to_felem(486662)
b25519 = to_felem(1)
u25519 = to_felem(2)

@typechecked
def f_25519(x:felem_t) -> felem_t:
    return fadd(fmul(x, fsqr(x)), fadd(fmul(a25519, fsqr(x)), x))

@typechecked
def map2curve25519(r:felem_t) -> felem_t:
    d = fsub(to_felem(p25519), fmul(a25519, finv(fadd(to_felem(1), fmul(u25519, fsqr(r))))))
    power = nat((p25519 - 1) // 2)
    e = fexp(f_25519(d), power)
    x = 0
    if e != 1:
        x = fsub(to_felem(-d), to_felem(a25519))
    else:
        x = d

    return x
~~~

## HashToBase {#hashtobase}

The following procedure implements HashToBase.

~~~
HashToBase(x, i)

Parameters:

  H - cryptographic hash function to use
  hbits - number of bits output by H
  p - order of the base field Fp
  label - context label for domain separation

Preconditions:

  floor(log2(p)) + 1 >= hbits

Input:

  x - value to be hashed, an octet string
  i - hash call index, a non-negative integer

Output:

  y - a value in the field Fp

Steps:

  1. t1 = H("h2c" || label || I2OSP(i, 4) || I2OSP(len(x), 4) || x)
  2. t2 = OS2IP(t1)
  3. y = t2 (mod p)
  4. Output y
~~~

where I2OSP, OS2IP {{RFC8017}} are used to convert an octet string to and from
a non-negative integer, and a || b denotes concatenation of a and b.

### Considerations

Performance: HashToBase requires hashing the entire input x. In some
algorithms/ciphersuite combinations, HashToBase is called multiple times. For
large inputs, implementers can therefore consider hashing x before calling
HashToBase. I.e. HashToBase(H'(x)).

Most algorithms assume that HashToBase maps its input to the base field
uniformly. In practice, there will be inherent biases. For example, taking H
as SHA256, over the finite field used by Curve25519 we have p = 2^255 - 19, and
thus when reducing from 255 bits, the values of 0 .. 19 will be twice as
likely to occur. This is a standard problem in generating uniformly
distributed integers from a bitstring. In this example, the resulting bias is
negligible, but for others this bias can be significant.

To address this, our HashToBase algorithm greedily takes as many bits as
possible before reducing mod p, in order to smooth out this bias. This is
preferable to an iterated procedure, such as rejection sampling, since this
can be hard to reliably implement in constant time.
