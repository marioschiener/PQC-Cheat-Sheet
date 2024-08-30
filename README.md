# PQC Cheat Sheet(s)
A cheat sheet for the new post quantum cryptography (PQC) algorithms.
(OK, actually multiple cheat sheets, it's just a little too much for one one page...)


#### Information
![GitHub Latest Release)](https://img.shields.io/github/v/release/marioschiener/PQC-Cheat-Sheet?logo=github&color=yellow) [![Github All Releases](https://img.shields.io/github/downloads/marioschiener/PQC-Cheat-Sheet/total?color=blue&logo=github)]()
[![Github Latest](https://img.shields.io/github/downloads/marioschiener/PQC-Cheat-Sheet/latest/total?color=blue&logo=github)]() [![Searches](https://img.shields.io/github/search/marioschiener/PQC-Cheat-Sheet/total?color=orange&logo=github)]()

#### Tech Stack
![LaTeX](https://img.shields.io/badge/LaTeX-LuaLaTex-green)

## Target Audience and Objectives

The target audience are technical roles such as software developers, architects or engineers or simply anyone interested in cryptography and PQC. The cheat sheets aim to make it easier for them to select the right algorithm for their use cases, based on various different algorithm characteristics presented in a simplified form.

**The main goal is quick information, not absolute precision! The cheat sheet is not intended to replace studying more specific specifications in a second step!**


## The PQC Cheat Sheet(s)
[PQC Cheat Sheet](https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/PQC_Cheat_Sheet.pdf)

The cheat sheets are currently in **DRAFT** status and are still **work in progress**! They are still incomplete and likely contain mistakes. Feedback and corrections are appreciated!

No responsibility is taken for the correctness of the information contained in the document.

### Working with the cheat sheet
The document takes the approach of simplifying algorithm characteristic (e.g. key sizes, signature or ciphertext sizes, CPU cycle counts, etc.) by boiling them down to only their **order of magnitude** (of kilobytes / kilocycles) and by **color-coding** accordingly. Green is always good, red not so much.

Yes, the order-of-magnitude-approach does make it impossible to spot differences that are smaller than a factor of 10 in the actual numbers, and yes, a factor of 10 is  definitely not negligible normally. This trade-off is however accepted as the goal of this cheat sheet is to make it as easy as possible to get a good **first impression** if an algorithm performs well in a certain category without having to interpret lots of specific byte numbers.

Please provide feedback if this approach is diluting the information too much.

The cheat sheet attempts to simplify things even further by assigning an overall **algorithm usability score** to each algorithm that takes into account all the different criteria.

Again keep in mind that this is all about quick initial information and providing rules of thumb, not absolute truth and precision, so take the information with a grain of salt.

### Preview

<p align="center">
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-1.png"  alt="Page 1" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-2.png"  alt="Page 2" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-3.png"  alt="Page 3" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-4.png"  alt="Page 4" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-5.png"  alt="Page 5" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-6.png"  alt="Page 6" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-7.png"  alt="Page 7" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-8.png"  alt="Page 8" width = 720px>
    <img src="https://github.com/marioschiener/PQC-Cheat-Sheet/blob/main/Screenshots/PQC-Cheat-Sheet-9.png"  alt="Page 9" width = 720px>
</p>



## Compiling the Source Files
Use LuaLaTeX for compiling the .tex files (PQC-Cheat-Sheet.tex is the root document). You may need to install the provided fonts in your system first. Set the -shell-escape option in order to reconvert the *.svg graphics after any change during compilation (this requires inkscape to be installed).

(Currently, all content except for the preamble is in one document on purpose. This is to make it easier to change formatting for each page using search/replace. Once everything stands, the content will be broken down into different smaller files.)


