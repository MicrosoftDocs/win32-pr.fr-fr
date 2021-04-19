---
description: La fonction Int64x32Div32 implémente la formule ((a \* b) + RND)/c où a est une valeur 64 bits et b, c et RND sont des valeurs 32 bits.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Int64x32Div32, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535352"
---
# <a name="int64x32div32-function"></a><span data-ttu-id="ec463-103">Int64x32Div32 fonction)</span><span class="sxs-lookup"><span data-stu-id="ec463-103">Int64x32Div32 function</span></span>

<span data-ttu-id="ec463-104">La `Int64x32Div32` fonction implémente la formule `((a*b)+rnd)/c` où *a* est une valeur 64 bits et *b*, *c* et *Rnd* sont des valeurs 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ec463-104">The `Int64x32Div32` function implements the formula `((a*b)+rnd)/c` where *a* is a 64-bit value and *b*, *c*, and *rnd* are 32-bit values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec463-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec463-105">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a><span data-ttu-id="ec463-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec463-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec463-107">*un*</span><span class="sxs-lookup"><span data-stu-id="ec463-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="ec463-108">Multiplicande.</span><span class="sxs-lookup"><span data-stu-id="ec463-108">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="ec463-109">*b*</span><span class="sxs-lookup"><span data-stu-id="ec463-109">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="ec463-110">Multiplicateur.</span><span class="sxs-lookup"><span data-stu-id="ec463-110">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="ec463-111">*c*</span><span class="sxs-lookup"><span data-stu-id="ec463-111">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="ec463-112">Division.</span><span class="sxs-lookup"><span data-stu-id="ec463-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="ec463-113">*RND*</span><span class="sxs-lookup"><span data-stu-id="ec463-113">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ec463-114">Facteur d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="ec463-114">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec463-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec463-115">Return value</span></span>

<span data-ttu-id="ec463-116">Retourne soit le calcul, soit l' `(a * b + rnd)/c` une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ec463-116">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="ec463-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ec463-117">Return code</span></span>                                                                                       | <span data-ttu-id="ec463-118">Description</span><span class="sxs-lookup"><span data-stu-id="ec463-118">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec463-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="ec463-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="ec463-120">Un dépassement s’est produit, car le résultat est trop grand (positif).</span><span class="sxs-lookup"><span data-stu-id="ec463-120">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="ec463-121"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="ec463-121"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="ec463-122">Un dépassement s’est produit, car le résultat est trop grand (négatif).</span><span class="sxs-lookup"><span data-stu-id="ec463-122">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec463-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ec463-123">Remarks</span></span>

<span data-ttu-id="ec463-124">L’arrondi sur la Division est vers zéro.</span><span class="sxs-lookup"><span data-stu-id="ec463-124">Rounding on the division is toward zero.</span></span> <span data-ttu-id="ec463-125">La division par zéro est comptée comme une condition de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="ec463-125">Division by zero is counted as an overflow condition.</span></span>

<span data-ttu-id="ec463-126">Les horodatages et les temps de recherche étant des valeurs 64 bits, cette fonction est utile pour effectuer des conversions sur les systèmes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ec463-126">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="ec463-127">Par exemple, dans MPEG-1, la référence de l’horloge système est 90-kHz, ou 90 000 graduations par seconde.</span><span class="sxs-lookup"><span data-stu-id="ec463-127">For example, in MPEG-1 the system clock reference is 90-kHz, or 90,000 ticks per second.</span></span> <span data-ttu-id="ec463-128">La formule à convertir en temps de référence (unités de 100 nanosecondes) est</span><span class="sxs-lookup"><span data-stu-id="ec463-128">The formula to convert this to reference time (100-nanosecond units) is</span></span>


```C++
(timestamp * 1000) / 9
```



<span data-ttu-id="ec463-129">qui peut être calculé comme `Int64x32Div32(timestamp, 1000, 9, 0)` .</span><span class="sxs-lookup"><span data-stu-id="ec463-129">which can be calculated as `Int64x32Div32(timestamp, 1000, 9, 0)`.</span></span> <span data-ttu-id="ec463-130">Utilisez le paramètre *Rnd* comme facteur d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="ec463-130">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec463-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec463-131">Requirements</span></span>



| <span data-ttu-id="ec463-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec463-132">Requirement</span></span> | <span data-ttu-id="ec463-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec463-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec463-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec463-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ec463-135"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec463-135"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ec463-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec463-136">Library</span></span><br/> | <dl> <span data-ttu-id="ec463-137"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec463-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec463-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec463-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec463-139">Fonctions d’assistance diverses</span><span class="sxs-lookup"><span data-stu-id="ec463-139">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="ec463-140">**llMulDiv**</span><span class="sxs-lookup"><span data-stu-id="ec463-140">**llMulDiv**</span></span>](llmuldiv.md)
</dt> </dl>

 

 




