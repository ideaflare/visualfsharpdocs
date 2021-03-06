---
title: Seq.sumBy<'T,^U> Function (F#)
description: Seq.sumBy<'T,^U> Function (F#)
keywords: visual f#, f#, functional programming
author: dend
manager: danielfe
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: visual-studio-dev14
ms.technology: devlang-fsharp
ms.assetid: 1c957828-4713-4695-93b7-828bb9790b3e
---

# Seq.sumBy<'T,^U> Function (F#)

Returns the sum of the results generated by applying the function to each element of the sequence.

**Namespace/Module Path:** Microsoft.FSharp.Collections.Seq

**Assembly:** FSharp.Core (in FSharp.Core.dll)


## Syntax

```fsharp
// Signature:
Seq.sumBy : ('T -> ^U) -> seq<'T> -> ^U (requires ^U with static member (+) and ^U with static member Zero)

// Usage:
Seq.sumBy projection source
```


#### Parameters
*projection*
Type: **'T -&gt; ^U**

A function to transform items from the input sequence into the quantity that will be summed.


*source*
Type: [seq](https://msdn.microsoft.com/library/2f0c87c6-8a0d-4d33-92a6-10d1d037ce75)**&lt;'T&gt;**

The input sequence.


## Return Value
The sum of the results of applying the projection function to each element of the sequence.


## Exceptions
May throw an [OverflowException](https://msdn.microsoft.com/library/system.overflowexception.aspx) due to arithmetic overflows.


## Remarks
The results are summed using the [checked + operator](https://msdn.microsoft.com/visualfsharpdocs/conceptual/checked.[-p-][%5Et1%2c%5Et2%2c%5Et3]-function-[fsharp]) and `Zero` property associated with the summed type.

This function is named `SumBy` in compiled assemblies. If you are accessing the function from a language other than F#, or through reflection, use this name.


## Platforms
Windows 8, Windows 7, Windows Server 2012, Windows Server 2008 R2


## Version Information
**F# Core Library Versions**

Supported in: 2.0, 4.0, Portable


## See Also
[Collections.Seq Module &#40;F&#35;&#41;](Collections.Seq-Module-%5BFSharp%5D.md)

[Microsoft.FSharp.Collections Namespace &#40;F&#35;&#41;](Microsoft.FSharp.Collections-Namespace-%5BFSharp%5D.md)
