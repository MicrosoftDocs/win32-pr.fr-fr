---
description: La méthode AlignDown tronque une valeur à une limite d’alignement spécifiée.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Méthode CPullPin. AlignDown (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527310"
---
# <a name="cpullpinaligndown-method"></a><span data-ttu-id="121c7-103">Méthode CPullPin. AlignDown</span><span class="sxs-lookup"><span data-stu-id="121c7-103">CPullPin.AlignDown method</span></span>

<span data-ttu-id="121c7-104">La `AlignDown` méthode tronque une valeur à une limite d’alignement spécifiée.</span><span class="sxs-lookup"><span data-stu-id="121c7-104">The `AlignDown` method truncates a value to a specified alignment boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="121c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="121c7-105">Syntax</span></span>


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="121c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="121c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="121c7-107">*ll*</span><span class="sxs-lookup"><span data-stu-id="121c7-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="121c7-108">Spécifie le nombre à aligner.</span><span class="sxs-lookup"><span data-stu-id="121c7-108">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="121c7-109">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="121c7-109">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="121c7-110">Spécifie la limite d’alignement.</span><span class="sxs-lookup"><span data-stu-id="121c7-110">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="121c7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="121c7-111">Return value</span></span>

<span data-ttu-id="121c7-112">Retourne le résultat aligné.</span><span class="sxs-lookup"><span data-stu-id="121c7-112">Returns the aligned result.</span></span>

## <a name="requirements"></a><span data-ttu-id="121c7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="121c7-113">Requirements</span></span>



| <span data-ttu-id="121c7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="121c7-114">Requirement</span></span> | <span data-ttu-id="121c7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="121c7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="121c7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="121c7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="121c7-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="121c7-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="121c7-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="121c7-118">Library</span></span><br/> | <dl> <span data-ttu-id="121c7-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="121c7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="121c7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="121c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="121c7-121">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="121c7-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




