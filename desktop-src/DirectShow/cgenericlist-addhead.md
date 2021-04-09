---
description: La méthode AddHead ajoute un élément au début de la liste.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Méthode CGenericList. AddHead (Wxlist. h)-paramètre pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104043202"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a><span data-ttu-id="cfaf8-103">Méthode CGenericList. AddHead (Wxlist. h)-paramètre pObj</span><span class="sxs-lookup"><span data-stu-id="cfaf8-103">CGenericList.AddHead method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="cfaf8-104">La `AddHead` méthode ajoute un élément au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-104">The `AddHead` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfaf8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfaf8-105">Syntax</span></span>


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="cfaf8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfaf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfaf8-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="cfaf8-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="cfaf8-108">Pointeur vers un objet de type **Object** (type de modèle).</span><span class="sxs-lookup"><span data-stu-id="cfaf8-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfaf8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfaf8-109">Return value</span></span>

<span data-ttu-id="cfaf8-110">Retourne une valeur de POSITION indiquant la nouvelle position de la tête.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-110">Returns a POSITION value indicating the new head position.</span></span> <span data-ttu-id="cfaf8-111">Si la méthode échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-111">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfaf8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfaf8-112">Requirements</span></span>

| <span data-ttu-id="cfaf8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfaf8-113">Requirement</span></span> | <span data-ttu-id="cfaf8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfaf8-114">Value</span></span> |
|-|-|
| <span data-ttu-id="cfaf8-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfaf8-115">Header</span></span> | <span data-ttu-id="cfaf8-116">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="cfaf8-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="cfaf8-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cfaf8-117">Library</span></span>| <span data-ttu-id="cfaf8-118">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="cfaf8-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="cfaf8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfaf8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfaf8-120">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="cfaf8-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




