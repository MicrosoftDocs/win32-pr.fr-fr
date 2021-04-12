---
description: En savoir plus sur la méthode de constructeur pour CGenericList. CGenericList (Wxlist. h). Cette méthode utilise les paramètres’pName’et’iItems'.
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Constructeur CGenericList. CGenericList (Wxlist. h)
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
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323457"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a><span data-ttu-id="cb607-104">CGenericList. CGenericList, constructeur (Wxlist. h)-pName, paramètres iItems</span><span class="sxs-lookup"><span data-stu-id="cb607-104">CGenericList.CGenericList constructor (Wxlist.h) - pName, iItems parameters</span></span>

<span data-ttu-id="cb607-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="cb607-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb607-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb607-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a><span data-ttu-id="cb607-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb607-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb607-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="cb607-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cb607-109">Pointeur vers le nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="cb607-109">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="cb607-110">*iItems*</span><span class="sxs-lookup"><span data-stu-id="cb607-110">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="cb607-111">Taille du cache du nœud.</span><span class="sxs-lookup"><span data-stu-id="cb607-111">Size of the node cache.</span></span>

</dd> <dt>

<span data-ttu-id="cb607-112">*Plage*</span><span class="sxs-lookup"><span data-stu-id="cb607-112">*bLock*</span></span> 
</dt> <dd>

<span data-ttu-id="cb607-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb607-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cb607-114">*Alerte*</span><span class="sxs-lookup"><span data-stu-id="cb607-114">*bAlert*</span></span> 
</dt> <dd>

<span data-ttu-id="cb607-115">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb607-115">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb607-116">Notes</span><span class="sxs-lookup"><span data-stu-id="cb607-116">Remarks</span></span>

<span data-ttu-id="cb607-117">Pour des performances optimales, la `CGenericList` classe gère un cache de nœuds de liste.</span><span class="sxs-lookup"><span data-stu-id="cb607-117">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="cb607-118">Si vous connaissez approximativement le nombre d’éléments que la liste doit contenir, utilisez cette version du constructeur.</span><span class="sxs-lookup"><span data-stu-id="cb607-118">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb607-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb607-119">Requirements</span></span>

| <span data-ttu-id="cb607-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb607-120">Requirement</span></span> | <span data-ttu-id="cb607-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb607-121">Value</span></span> |
|-|-|
| <span data-ttu-id="cb607-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb607-122">Header</span></span> | <span data-ttu-id="cb607-123">Wxlist. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="cb607-123">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="cb607-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb607-124">Library</span></span>| <span data-ttu-id="cb607-125">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="cb607-125">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="cb607-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb607-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb607-127">**CGenericList, classe**</span><span class="sxs-lookup"><span data-stu-id="cb607-127">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




