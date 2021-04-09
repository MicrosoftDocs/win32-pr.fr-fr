---
description: En savoir plus sur la méthode de constructeur pour CGenericList. CGenericList (Wxlist. h). Cette méthode utilise le paramètre’pName'.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: CGenericList. CGenericList, constructeur (Wxlist. h)-pName, paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103870217"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a><span data-ttu-id="fa993-104">CGenericList. CGenericList, constructeur (Wxlist. h)-pName, paramètre</span><span class="sxs-lookup"><span data-stu-id="fa993-104">CGenericList.CGenericList constructor (Wxlist.h) - pName parameter</span></span>

<span data-ttu-id="fa993-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="fa993-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa993-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa993-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="fa993-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa993-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa993-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="fa993-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="fa993-109">Pointeur vers le nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="fa993-109">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa993-110">Notes</span><span class="sxs-lookup"><span data-stu-id="fa993-110">Remarks</span></span>

<span data-ttu-id="fa993-111">Pour des performances optimales, la `CGenericList` classe gère un cache de nœuds de liste.</span><span class="sxs-lookup"><span data-stu-id="fa993-111">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="fa993-112">Cette version du constructeur utilise une taille de cache par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa993-112">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa993-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa993-113">Requirements</span></span>

| <span data-ttu-id="fa993-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa993-114">Requirement</span></span> | <span data-ttu-id="fa993-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa993-115">Value</span></span> |
|-|-|
| <span data-ttu-id="fa993-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa993-116">Header</span></span> | <span data-ttu-id="fa993-117">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="fa993-117">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="fa993-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa993-118">Library</span></span>| <span data-ttu-id="fa993-119">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="fa993-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="fa993-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa993-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa993-121">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="fa993-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




