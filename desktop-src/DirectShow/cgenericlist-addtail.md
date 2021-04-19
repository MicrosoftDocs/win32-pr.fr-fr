---
description: La méthode AddTail ajoute un élément à la fin de la liste.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Méthode CGenericList. AddTail (Wxlist. h)-paramètre pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106522768"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a><span data-ttu-id="5a2b1-103">Méthode CGenericList. AddTail (Wxlist. h)-paramètre pObj</span><span class="sxs-lookup"><span data-stu-id="5a2b1-103">CGenericList.AddTail method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="5a2b1-104">La `AddTail` méthode ajoute un élément à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="5a2b1-104">The `AddTail` method appends an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a2b1-105">Syntax</span></span>


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="5a2b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a2b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2b1-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="5a2b1-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="5a2b1-108">Pointeur vers un objet de type **Object** (type de modèle).</span><span class="sxs-lookup"><span data-stu-id="5a2b1-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2b1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a2b1-109">Return value</span></span>

<span data-ttu-id="5a2b1-110">Retourne une valeur de POSITION pour la nouvelle position de fin.</span><span class="sxs-lookup"><span data-stu-id="5a2b1-110">Returns a POSITION value for the new tail position.</span></span> <span data-ttu-id="5a2b1-111">Si la méthode échoue, elle retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5a2b1-111">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2b1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a2b1-112">Requirements</span></span>

| <span data-ttu-id="5a2b1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a2b1-113">Requirement</span></span> | <span data-ttu-id="5a2b1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a2b1-114">Value</span></span> |
|-|-|
| <span data-ttu-id="5a2b1-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a2b1-115">Header</span></span> | <span data-ttu-id="5a2b1-116">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="5a2b1-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="5a2b1-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a2b1-117">Library</span></span>| <span data-ttu-id="5a2b1-118">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="5a2b1-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5a2b1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a2b1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2b1-120">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="5a2b1-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




