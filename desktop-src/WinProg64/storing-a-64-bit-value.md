---
title: Stockage d’une valeur 64 bits
description: Pour stocker une valeur de pointeur 64 bits, utilisez ULONG \_ ptr. Une \_ valeur PTR ulong est 32 bits quand elle est compilée avec un compilateur 32 bits et 64 bits lorsqu’elle est compilée avec un compilateur 64 bits.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- stockage des valeurs 64 bits de la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310057"
---
# <a name="storing-a-64-bit-value"></a><span data-ttu-id="e0b31-105">Stockage d’une valeur 64 bits</span><span class="sxs-lookup"><span data-stu-id="e0b31-105">Storing a 64-bit Value</span></span>

<span data-ttu-id="e0b31-106">Pour stocker une valeur de pointeur 64 bits, utilisez **ULong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="e0b31-106">To store a 64-bit pointer value, use **ULONG\_PTR**.</span></span> <span data-ttu-id="e0b31-107">Une **valeur \_ ptr ULONG** est 32 bits quand elle est compilée avec un compilateur 32 bits et 64 bits lorsqu’elle est compilée avec un compilateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e0b31-107">A **ULONG\_PTR** value is 32 bits when compiled with a 32-bit compiler and 64 bits when compiled with a 64-bit compiler.</span></span>

<span data-ttu-id="e0b31-108">Les exemples suivants utilisent du code réel qui a été porté sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e0b31-108">The following examples use real-world code that has been ported to 64-bit Windows.</span></span> <span data-ttu-id="e0b31-109">Des commentaires sur les étapes permettant de rendre le code compatible 64 bits sont inclus.</span><span class="sxs-lookup"><span data-stu-id="e0b31-109">Commentary on the steps to make the code 64-bit compatible is included.</span></span>

## <a name="example-1-getting-an-address"></a><span data-ttu-id="e0b31-110">Exemple 1 : obtention d’une adresse</span><span class="sxs-lookup"><span data-stu-id="e0b31-110">Example 1: Getting an Address</span></span>

<span data-ttu-id="e0b31-111">Le code suivant illustre un moyen portable d’obtenir une adresse.</span><span class="sxs-lookup"><span data-stu-id="e0b31-111">The following code illustrates a portable way to get an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0b31-112">Utilisation de ULONG (méthode 32 bits uniquement)</span><span class="sxs-lookup"><span data-stu-id="e0b31-112">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0b31-113">Utilisation de ULONG_PTR (méthode portable)</span><span class="sxs-lookup"><span data-stu-id="e0b31-113">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a><span data-ttu-id="e0b31-114">Exemple 2 : calcul d’une adresse</span><span class="sxs-lookup"><span data-stu-id="e0b31-114">Example 2: Calculating an Address</span></span>

<span data-ttu-id="e0b31-115">Le code suivant illustre un moyen portable de calculer une adresse.</span><span class="sxs-lookup"><span data-stu-id="e0b31-115">The following code illustrates a portable way to calculate an address.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0b31-116">Utilisation de ULONG (méthode 32 bits uniquement)</span><span class="sxs-lookup"><span data-stu-id="e0b31-116">Using ULONG (a 32-bit-only method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0b31-117">Utilisation de ULONG_PTR (méthode portable)</span><span class="sxs-lookup"><span data-stu-id="e0b31-117">Using ULONG_PTR (the portable method)</span></span></td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




