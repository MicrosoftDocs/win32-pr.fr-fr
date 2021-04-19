---
description: La fonction llMulDiv implémente la formule ((a \* b) + RND)/c où chaque terme est une valeur 64 bits.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: llMulDiv, fonction (Wxutil. h)
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
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542334"
---
# <a name="llmuldiv-function"></a><span data-ttu-id="9979f-103">llMulDiv fonction)</span><span class="sxs-lookup"><span data-stu-id="9979f-103">llMulDiv function</span></span>

<span data-ttu-id="9979f-104">La `llMulDiv` fonction implémente la formule `((a*b)+rnd)/c` où chaque terme est une valeur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9979f-104">The `llMulDiv` function implements the formula `((a*b)+rnd)/c` where each term is a 64-bit value.</span></span>

<span data-ttu-id="9979f-105">Les horodatages et les temps de recherche étant des valeurs 64 bits, cette fonction est utile pour effectuer des conversions sur les systèmes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9979f-105">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="9979f-106">Par exemple, la formule pour les octets par seconde est</span><span class="sxs-lookup"><span data-stu-id="9979f-106">For example, the formula for bytes-per-second is</span></span>


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



<span data-ttu-id="9979f-107">qui peut être calculé comme `llMulDiv(nBytes, rtTime, 10000000, 0)` .</span><span class="sxs-lookup"><span data-stu-id="9979f-107">which can be calculated as `llMulDiv(nBytes, rtTime, 10000000, 0)`.</span></span> <span data-ttu-id="9979f-108">Utilisez le paramètre *Rnd* comme facteur d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="9979f-108">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9979f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9979f-109">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a><span data-ttu-id="9979f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9979f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9979f-111">*un*</span><span class="sxs-lookup"><span data-stu-id="9979f-111">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="9979f-112">Multiplicande.</span><span class="sxs-lookup"><span data-stu-id="9979f-112">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="9979f-113">*b*</span><span class="sxs-lookup"><span data-stu-id="9979f-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="9979f-114">Multiplicateur.</span><span class="sxs-lookup"><span data-stu-id="9979f-114">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="9979f-115">*c*</span><span class="sxs-lookup"><span data-stu-id="9979f-115">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="9979f-116">Division.</span><span class="sxs-lookup"><span data-stu-id="9979f-116">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="9979f-117">*RND*</span><span class="sxs-lookup"><span data-stu-id="9979f-117">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9979f-118">Facteur d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="9979f-118">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9979f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9979f-119">Return value</span></span>

<span data-ttu-id="9979f-120">Retourne soit le calcul, soit l' `(a * b + rnd)/c` une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9979f-120">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="9979f-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9979f-121">Return code</span></span>                                                                                       | <span data-ttu-id="9979f-122">Description</span><span class="sxs-lookup"><span data-stu-id="9979f-122">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9979f-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="9979f-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="9979f-124">Un dépassement s’est produit, car le résultat est trop grand (positif).</span><span class="sxs-lookup"><span data-stu-id="9979f-124">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="9979f-125"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="9979f-125"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="9979f-126">Un dépassement s’est produit, car le résultat est trop grand (négatif).</span><span class="sxs-lookup"><span data-stu-id="9979f-126">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9979f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9979f-127">Remarks</span></span>

<span data-ttu-id="9979f-128">L’arrondi sur la Division est vers zéro.</span><span class="sxs-lookup"><span data-stu-id="9979f-128">Rounding on the division is toward zero.</span></span> <span data-ttu-id="9979f-129">La division par zéro est comptée comme une condition de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="9979f-129">Division by zero is counted as an overflow condition.</span></span>

## <a name="requirements"></a><span data-ttu-id="9979f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9979f-130">Requirements</span></span>



| <span data-ttu-id="9979f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9979f-131">Requirement</span></span> | <span data-ttu-id="9979f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="9979f-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9979f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9979f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9979f-134"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9979f-134"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9979f-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9979f-135">Library</span></span><br/> | <dl> <span data-ttu-id="9979f-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9979f-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9979f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9979f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9979f-138">Fonctions d’assistance diverses</span><span class="sxs-lookup"><span data-stu-id="9979f-138">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="9979f-139">**Int64x32Div32**</span><span class="sxs-lookup"><span data-stu-id="9979f-139">**Int64x32Div32**</span></span>](int64x32div32.md)
</dt> </dl>

 

 




