---
description: La méthode AddHead ajoute une liste au début de la liste.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Méthode CGenericList. AddHead (Wxlist. h)-paramètres plist
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
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106525910"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a><span data-ttu-id="ae5e6-103">Méthode CGenericList. AddHead (Wxlist. h)-paramètres plist</span><span class="sxs-lookup"><span data-stu-id="ae5e6-103">CGenericList.AddHead method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="ae5e6-104">La `AddHead` méthode ajoute une liste au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="ae5e6-104">The `AddHead` method adds a list to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae5e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae5e6-105">Syntax</span></span>


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="ae5e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae5e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae5e6-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="ae5e6-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ae5e6-108">Pointeur vers la liste des éléments à ajouter.</span><span class="sxs-lookup"><span data-stu-id="ae5e6-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae5e6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae5e6-109">Return value</span></span>

<span data-ttu-id="ae5e6-110">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ae5e6-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae5e6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae5e6-111">Requirements</span></span>

| <span data-ttu-id="ae5e6-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae5e6-112">Requirement</span></span> | <span data-ttu-id="ae5e6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae5e6-113">Value</span></span> |
|-|-|
| <span data-ttu-id="ae5e6-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae5e6-114">Header</span></span> | <span data-ttu-id="ae5e6-115">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="ae5e6-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="ae5e6-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae5e6-116">Library</span></span>| <span data-ttu-id="ae5e6-117">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="ae5e6-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae5e6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae5e6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5e6-119">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="ae5e6-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




