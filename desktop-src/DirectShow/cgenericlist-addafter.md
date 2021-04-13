---
description: La méthode AddAfter insère un élément après la position spécifiée et utilise les paramètres « p » et « pObj ».
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Méthode CGenericList. AddAfter (Wxlist. h)-p, paramètres pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323438"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="91ff9-103">Méthode CGenericList. AddAfter (Wxlist. h)-p, paramètres pObj</span><span class="sxs-lookup"><span data-stu-id="91ff9-103">CGenericList.AddAfter method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="91ff9-104">La `AddAfter` méthode insère un élément après la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="91ff9-104">The `AddAfter` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ff9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91ff9-105">Syntax</span></span>


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="91ff9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91ff9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ff9-107">*p*</span><span class="sxs-lookup"><span data-stu-id="91ff9-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="91ff9-108">Position après laquelle l’élément doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="91ff9-108">Position after which to add the item.</span></span> <span data-ttu-id="91ff9-109">Si *p* est **null**, la méthode ajoute l’élément au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="91ff9-109">If *p* is **NULL**, the method adds the item to the head of the list.</span></span>

</dd> <dt>

<span data-ttu-id="91ff9-110">*pObj*</span><span class="sxs-lookup"><span data-stu-id="91ff9-110">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="91ff9-111">Pointeur vers un objet de type **Object** (type de modèle).</span><span class="sxs-lookup"><span data-stu-id="91ff9-111">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ff9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91ff9-112">Return value</span></span>

<span data-ttu-id="91ff9-113">Retourne l’indicateur de position de l’élément inséré.</span><span class="sxs-lookup"><span data-stu-id="91ff9-113">Returns the position indicator of the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ff9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91ff9-114">Requirements</span></span>

| <span data-ttu-id="91ff9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91ff9-115">Requirement</span></span> | <span data-ttu-id="91ff9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="91ff9-116">Value</span></span> |
|-|-|
| <span data-ttu-id="91ff9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="91ff9-117">Header</span></span> | <span data-ttu-id="91ff9-118">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="91ff9-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="91ff9-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91ff9-119">Library</span></span>| <span data-ttu-id="91ff9-120">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="91ff9-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="91ff9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91ff9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ff9-122">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="91ff9-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




