# Introduction

Backlang's main focus is on reducing code duplication and code by context. The macro system allows us to run functionality before compilation or to generate source code on the fly.
With macros you can create your own language constructs to hide the complexity of a problem.


## Why a new language?

C# is a really good language but has a lack of code reduction. 
F# has really nice features but is less intuitive for C# developers. So I have decided to build a new language to fill the gap between C# and F#, and have added a macro system for code reduction and the ability to make custom language constructs to hide complex problems in a Domain Specific Language. 

Users can also write inline intrinsics to use runtime features that are not yet available in the language itself (eg. inline-il).
