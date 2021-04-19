---
description: La méthode AddTail ajoute une liste à la fin de la liste.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Méthode CGenericList. AddTail (Wxlist. h)-paramètres plist
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
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106528584"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a><span data-ttu-id="d2cb6-103">Méthode CGenericList. AddTail (Wxlist. h)-paramètres plist</span><span class="sxs-lookup"><span data-stu-id="d2cb6-103">CGenericList.AddTail method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="d2cb6-104">La `AddTail` méthode ajoute une liste à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="d2cb6-104">The `AddTail` method appends a list to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cb6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2cb6-105">Syntax</span></span>


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a><span data-ttu-id="d2cb6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2cb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2cb6-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="d2cb6-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="d2cb6-108">Pointeur vers la liste à ajouter.</span><span class="sxs-lookup"><span data-stu-id="d2cb6-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2cb6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2cb6-109">Return value</span></span>

<span data-ttu-id="d2cb6-110">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d2cb6-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2cb6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2cb6-111">Requirements</span></span>

| <span data-ttu-id="d2cb6-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2cb6-112">Requirement</span></span> | <span data-ttu-id="d2cb6-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2cb6-113">Value</span></span> |
|-|-|
| <span data-ttu-id="d2cb6-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2cb6-114">Header</span></span> | <span data-ttu-id="d2cb6-115">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="d2cb6-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="d2cb6-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d2cb6-116">Library</span></span>| <span data-ttu-id="d2cb6-117">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="d2cb6-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d2cb6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2cb6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2cb6-119">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="d2cb6-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




