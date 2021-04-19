---
description: Méthode de constructeur.
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
ms.openlocfilehash: 3afc0a4acf54e186e122f676ac14e9e80aaeafdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525272"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="05183-103">Constructeur CBaseList. CBaseList</span><span class="sxs-lookup"><span data-stu-id="05183-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="05183-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="05183-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05183-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05183-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="05183-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05183-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="05183-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="05183-108">Pointeur vers le nom de la liste.</span><span class="sxs-lookup"><span data-stu-id="05183-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05183-109">Notes</span><span class="sxs-lookup"><span data-stu-id="05183-109">Remarks</span></span>

<span data-ttu-id="05183-110">Pour des performances optimales, la `CBaseList` classe gère un cache de nœuds de liste.</span><span class="sxs-lookup"><span data-stu-id="05183-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="05183-111">Cette version du constructeur utilise une taille de cache par défaut.</span><span class="sxs-lookup"><span data-stu-id="05183-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="05183-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05183-112">Requirements</span></span>



| <span data-ttu-id="05183-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05183-113">Requirement</span></span> | <span data-ttu-id="05183-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="05183-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05183-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="05183-115">Header</span></span><br/>  | <dl> <span data-ttu-id="05183-116"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05183-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="05183-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05183-117">Library</span></span><br/> | <dl> <span data-ttu-id="05183-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="05183-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05183-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05183-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05183-120">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="05183-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




