---
description: Méthode de constructeur.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Constructeur CBaseList. CBaseList (TCHAR *, INT) (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541142"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="d80e4-103">Constructeur CBaseList. CBaseList (TCHAR \* , int)</span><span class="sxs-lookup"><span data-stu-id="d80e4-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="d80e4-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="d80e4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d80e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d80e4-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="d80e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d80e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d80e4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d80e4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d80e4-108">Pointeur vers le nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="d80e4-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="d80e4-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="d80e4-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="d80e4-110">Taille du cache du nœud.</span><span class="sxs-lookup"><span data-stu-id="d80e4-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d80e4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d80e4-111">Remarks</span></span>

<span data-ttu-id="d80e4-112">Pour des performances optimales, la `CBaseList` classe gère un cache de nœuds de liste.</span><span class="sxs-lookup"><span data-stu-id="d80e4-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="d80e4-113">Si vous connaissez approximativement le nombre d’éléments que la liste doit contenir, utilisez cette version du constructeur.</span><span class="sxs-lookup"><span data-stu-id="d80e4-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="d80e4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d80e4-114">Requirements</span></span>



| <span data-ttu-id="d80e4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d80e4-115">Requirement</span></span> | <span data-ttu-id="d80e4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d80e4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d80e4-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d80e4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d80e4-118"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d80e4-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d80e4-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d80e4-119">Library</span></span><br/> | <dl> <span data-ttu-id="d80e4-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d80e4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d80e4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d80e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d80e4-122">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="d80e4-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




