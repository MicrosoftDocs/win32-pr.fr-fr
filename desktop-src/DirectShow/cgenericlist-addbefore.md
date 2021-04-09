---
description: La méthode AddBefore insère un élément avant la position spécifiée. Cette méthode utilise les paramètres « p » et « pObj ».
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Méthode CGenericList. AddBefore (Wxlist. h)-p, paramètres pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954034"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="5883c-104">Méthode CGenericList. AddBefore (Wxlist. h)-p, paramètres pObj</span><span class="sxs-lookup"><span data-stu-id="5883c-104">CGenericList.AddBefore method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="5883c-105">La `AddBefore` méthode insère un élément avant la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5883c-105">The `AddBefore` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="5883c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5883c-106">Syntax</span></span>


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="5883c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5883c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5883c-108">*p*</span><span class="sxs-lookup"><span data-stu-id="5883c-108">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="5883c-109">Position avant laquelle insérer la liste.</span><span class="sxs-lookup"><span data-stu-id="5883c-109">Position before which to insert the list.</span></span> <span data-ttu-id="5883c-110">Si *p* est **null**, cette méthode ajoute l’élément à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="5883c-110">If *p* is **NULL**, this method adds the item to the tail of the list.</span></span>

</dd> <dt>

<span data-ttu-id="5883c-111">*pObj*</span><span class="sxs-lookup"><span data-stu-id="5883c-111">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="5883c-112">Pointeur vers un objet de type **Object** (type de modèle).</span><span class="sxs-lookup"><span data-stu-id="5883c-112">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5883c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5883c-113">Return value</span></span>

<span data-ttu-id="5883c-114">Retourne l’indicateur de position pour l’élément inséré.</span><span class="sxs-lookup"><span data-stu-id="5883c-114">Returns the position indicator for the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="5883c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5883c-115">Requirements</span></span>

| <span data-ttu-id="5883c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5883c-116">Requirement</span></span> | <span data-ttu-id="5883c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5883c-117">Value</span></span> |
|-|-|
| <span data-ttu-id="5883c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="5883c-118">Header</span></span> | <span data-ttu-id="5883c-119">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="5883c-119">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="5883c-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5883c-120">Library</span></span>| <span data-ttu-id="5883c-121">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="5883c-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5883c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5883c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5883c-123">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="5883c-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




