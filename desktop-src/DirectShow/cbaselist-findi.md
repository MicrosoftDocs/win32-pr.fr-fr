---
description: La méthode Findi récupère la première position qui contient l’élément spécifié.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: CBaseList. Findi, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525499"
---
# <a name="cbaselistfindi-method"></a><span data-ttu-id="71c18-103">CBaseList. Findi, méthode</span><span class="sxs-lookup"><span data-stu-id="71c18-103">CBaseList.FindI method</span></span>

<span data-ttu-id="71c18-104">La `FindI` méthode récupère la première position qui contient l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="71c18-104">The `FindI` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c18-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71c18-105">Syntax</span></span>


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="71c18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71c18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c18-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="71c18-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="71c18-108">Pointeur désignant l’élément.</span><span class="sxs-lookup"><span data-stu-id="71c18-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c18-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71c18-109">Return value</span></span>

<span data-ttu-id="71c18-110">Retourne une valeur de POSITION, ou **null** si l’élément n’est pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="71c18-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="71c18-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71c18-111">Requirements</span></span>



| <span data-ttu-id="71c18-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71c18-112">Requirement</span></span> | <span data-ttu-id="71c18-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="71c18-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c18-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="71c18-114">Header</span></span><br/>  | <dl> <span data-ttu-id="71c18-115"><dt>Wxlist. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71c18-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="71c18-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71c18-116">Library</span></span><br/> | <dl> <span data-ttu-id="71c18-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="71c18-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71c18-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71c18-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c18-119">**CBaseList, classe**</span><span class="sxs-lookup"><span data-stu-id="71c18-119">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




