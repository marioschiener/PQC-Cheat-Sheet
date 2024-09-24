<p align="center">
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/resources/Github-Logo.png"  alt="Logo" width = 500px>
</p>

# The Post-Quantum Cryptopgraphy Cheat Sheets
A series of cheat sheets for the new post-quantum cryptography (PQC) algorithms and about picking the right one for your application.


#### Information
![GitHub Latest Release)](https://img.shields.io/github/v/release/marioschiener/PQC-Cheat-Sheet?logo=github&color=yellow) [![Github All Releases](https://img.shields.io/github/downloads/marioschiener/PQC-Cheat-Sheet/total?color=blue&logo=github)]()
[![Github Latest](https://img.shields.io/github/downloads/marioschiener/PQC-Cheat-Sheet/latest/total?color=blue&logo=github)]() [![Searches](https://img.shields.io/github/search/marioschiener/PQC-Cheat-Sheet/total?color=orange&logo=github)]()

#### Tech Stack
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTex-green)


# Table of Contents


1. [The PQC Cheat Sheet(s)](#cheatsheet)
    1. [Algorithms](#algorithms)
    2. [Working with and Interpreting the Cheat Sheet](#howto)
    3. [Target Audience and Objectives](#target)
2. [Preview](#preview)
3. [Compiling the Source Files](#compiling)
4. [Credit and Further Reading](#credits)
5. [Disclaimer](#disclaimer)


---

# The PQC Cheat Sheet(s)<a name="cheatsheet"></a>
[PQC Cheat Sheet](https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/PQC_Cheat_Sheet.pdf)

The cheat sheets are currently in **DRAFT** status and are still **work in progress**! They are still incomplete and likely contain mistakes. Feedback and corrections are appreciated!

No responsibility is taken for the correctness of the information contained in the document.

## Algorithms<a name="algorithms"></a>

**Signature:** ML-DSA (CRYSTALS-DILITHIUM), Falcon, SLH-DSA (SHPINCS+), XMSS/XMSSMT, LMS/HSS

**Encryption/KEM:** ML-KEM (CRYSTALS-KYBER), BIKE, HQC, Classic McEliece, FrodoKEM

## Working with and Interpreting the Cheat Sheet<a name="howto"></a>
**The goal of this series of cheat sheets is to make it as easy as possible to figure out which algorithm to pick for a given use case. Algorithm ID cards break down algorithm parameter sets, their important values and performance characteristics. The cheat sheets are intended to help users primarily in technical roles, such as engineers, architects or software developers working with post-quantum cryptography.**

The focus is to avoid giving specific numbers measured in bits, bytes or cycles as this makes makes comparing numbers across algorithms difficult. Instead, this complexity is simplified by only providing a
**color-coded number indicating the order of magnitude of each metric.**

**This approach prioritizes easy interpretation and comparability of metrics and in general quick informational gain over absolute precision of data -- remember this is a cheat sheet, not a standard! This document is not intended to replace the study of algorithm specifications. It just aims to point you in the right direction quickly.**

The approach of focusing on orders of magnitude walks a fine line between treating too many things as "equal" and not simplifying things enough to be easy to read and compare. "In the same order of magnitude" usually refers to "equal up to a factor of at most 10", which is a very coarse way of comparing numbers. Treating metrics that differ by a factor of e.g. 9.9 as "equal" because 9.9 < 10 paints a distorted picture. In cryptography, factors of 5 or even 2 can make a significant difference in security or performance, both in theory and in practice. In order to still tease out the differences in metrics without throwing too many things together that actually differ significantly, this cheat sheet applies different scaling and "orders of magnitude" (i.e., not regarding base 10) for different metrics.

It turns out that for **metrics measured in (kilo) CPU cycle counts, i.e. algorithm performance, "up to a factor of 5"** is a scale that is granular enough to work out the differences between algorithms while maintaining easy comparability. Those cycle counts heavily depend on the CPU used during measurement, hence the numbers need to be taken with a grain of salt, even if given exactly and not in terms of orders of magnitude.

For **signature and ciphertext sizes as well as key sizes, measuring numbers in kilobytes "up to a factor of 2"** is well suited to work out the differences between algorithms while allowing for quick comparison. Specifically for signature public key sizes only, we offset the corresponding color coding by 5 orders of magnitude. This is because SLH-DSA has extremely small pubic keys compared to all other signature algorithms, which would extend the scale into negative numbers (e.g. for SLH-DSA-SHA2-128s, the public key has 32=2^5 bytes, which corresponds to an order of magnitude of -5 when measuring in orders of magnitude of base 2 and in kilobytes). This phenomenon of algorithm metrics spanning a very large range of orders of (base 2) magnitudes does not occur to this extent for encryption algorithms, making an offset unnecessary.

All values thus have a lower bound of 0. We do not limit the upper end of scales, but don't distinguish values greater than 10 anymore in terms of color coding. Please refer to the definitions in the cheat sheet for symbol explanations, color coding and interpretation of numeric values.

## Target Audience and Objectives<a name="target"></a>

The target audience are technical roles such as software developers, architects or engineers or simply anyone interested in cryptography and PQC. The cheat sheets aim to make it easier for them to select the right algorithm for their use cases, based on various different algorithm characteristics presented in a simplified form.

**The main goal is quick information, not absolute precision! The cheat sheets are not intended to replace studying more specific specifications in a second step!**

# Preview<a name="preview"></a>

<p align="center">
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-01.png"  alt="Page 1" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-02.png"  alt="Page 2" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-03.png"  alt="Page 3" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-04.png"  alt="Page 4" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-05.png"  alt="Page 5" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-06.png"  alt="Page 6" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-07.png"  alt="Page 7" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-08.png"  alt="Page 8" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-09.png"  alt="Page 9" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-10.png"  alt="Page 10" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-11.png"  alt="Page 11" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-12.png"  alt="Page 12" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-13.png"  alt="Page 13" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-14.png"  alt="Page 14" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-15.png"  alt="Page 15" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-16.png"  alt="Page 16" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-17.png"  alt="Page 17" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-18.png"  alt="Page 18" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-19.png"  alt="Page 19" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-20.png"  alt="Page 21" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-21.png"  alt="Page 21" width = 720px>
</p>



# Compiling the Source Files<a name="compiling"></a>

Use LuaLaTeX for compiling the .tex files (PQC-Cheat-Sheet.tex is the root document). You may need to install the provided fonts in your system first. Set the -shell-escape option in order to reconvert the *.svg graphics after any change during compilation (this requires Inkscape to be installed).

# Credits and Further Reading<a name="credits"></a>

TBD

---

# Disclaimer<a name="disclaimer"></a>
No responsibility is taken for the correctness of the information in this cheat sheet.
