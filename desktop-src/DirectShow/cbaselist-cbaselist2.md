---
description: Méthode constructeur CBaseList. CBaseList.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Constructeur CBaseList. CBaseList (Wxlist. h)
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096326"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="e9e63-103">Constructeur CBaseList. CBaseList</span><span class="sxs-lookup"><span data-stu-id="e9e63-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="e9e63-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="e9e63-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9e63-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="e9e63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9e63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e63-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e9e63-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e63-108">Pointeur vers le nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="e9e63-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9e63-109">Notes </span><span class="sxs-lookup"><span data-stu-id="e9e63-109">Remarks</span></span>

<span data-ttu-id="e9e63-110">Pour des performances optimales, la `CBaseList` classe gère un cache de nœuds de liste.</span><span class="sxs-lookup"><span data-stu-id="e9e63-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="e9e63-111">Cette version du constructeur utilise une taille de cache par défaut.</span><span class="sxs-lookup"><span data-stu-id="e9e63-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e63-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9e63-112">Requirements</span></span>



| <span data-ttu-id="e9e63-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9e63-113">Requirement</span></span> | <span data-ttu-id="e9e63-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9e63-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e63-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9e63-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e9e63-116"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9e63-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e9e63-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9e63-117">Library</span></span><br/> | <dl> <span data-ttu-id="e9e63-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9e63-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e63-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9e63-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e63-120">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="e9e63-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




