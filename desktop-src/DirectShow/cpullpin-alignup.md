---
description: La méthode AlignUp arrondit une valeur à une limite d’alignement spécifiée. Remarque supprimée dans Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Méthode CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542378"
---
# <a name="cpullpinalignup-method"></a><span data-ttu-id="020bd-104">Méthode CPullPin. AlignUp</span><span class="sxs-lookup"><span data-stu-id="020bd-104">CPullPin.AlignUp method</span></span>

<span data-ttu-id="020bd-105">La méthode **AlignUp** arrondit une valeur à une limite d’alignement spécifiée.</span><span class="sxs-lookup"><span data-stu-id="020bd-105">The **AlignUp** method rounds a value up to a specified alignment boundary.</span></span>

> [!Note]  
> <span data-ttu-id="020bd-106">Supprimé dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="020bd-106">Removed in Windows 7.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="020bd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="020bd-107">Syntax</span></span>


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="020bd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="020bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="020bd-109">*ll*</span><span class="sxs-lookup"><span data-stu-id="020bd-109">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="020bd-110">Spécifie le nombre à aligner.</span><span class="sxs-lookup"><span data-stu-id="020bd-110">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="020bd-111">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="020bd-111">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="020bd-112">Spécifie la limite d’alignement.</span><span class="sxs-lookup"><span data-stu-id="020bd-112">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="020bd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="020bd-113">Return value</span></span>

<span data-ttu-id="020bd-114">Retourne le résultat aligné.</span><span class="sxs-lookup"><span data-stu-id="020bd-114">Returns the aligned result.</span></span>

## <a name="remarks"></a><span data-ttu-id="020bd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="020bd-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="020bd-116">Cette méthode peut provoquer un dépassement de capacité numérique si *ll* + (*lAlign* -1) déborde.</span><span class="sxs-lookup"><span data-stu-id="020bd-116">This method can cause numeric overflow if *ll* + (*lAlign* - 1) overflows.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="020bd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="020bd-117">Requirements</span></span>



| <span data-ttu-id="020bd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="020bd-118">Requirement</span></span> | <span data-ttu-id="020bd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="020bd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="020bd-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="020bd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="020bd-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="020bd-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="020bd-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="020bd-122">Library</span></span><br/> | <dl> <span data-ttu-id="020bd-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="020bd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="020bd-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="020bd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="020bd-125">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="020bd-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




