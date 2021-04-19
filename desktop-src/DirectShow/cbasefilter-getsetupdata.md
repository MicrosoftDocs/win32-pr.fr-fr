---
description: La méthode GetSetupData récupère les données d’inscription du filtre.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Méthode CBaseFilter. GetSetupData (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521690"
---
# <a name="cbasefiltergetsetupdata-method"></a><span data-ttu-id="2f48e-103">Méthode CBaseFilter. GetSetupData</span><span class="sxs-lookup"><span data-stu-id="2f48e-103">CBaseFilter.GetSetupData method</span></span>

<span data-ttu-id="2f48e-104">La `GetSetupData` méthode récupère les données d’inscription pour le filtre.</span><span class="sxs-lookup"><span data-stu-id="2f48e-104">The `GetSetupData` method retrieves the registration data for the filter.</span></span>

> [!Note]  
> <span data-ttu-id="2f48e-105">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="2f48e-105">This method is obsolete.</span></span> <span data-ttu-id="2f48e-106">Elle est appelée par les méthodes [**CBaseFilter :: Register**](cbasefilter-register.md) et [**CBaseFilter :: Unregister**](cbasefilter-unregister.md) .</span><span class="sxs-lookup"><span data-stu-id="2f48e-106">It is called by the [**CBaseFilter::Register**](cbasefilter-register.md) and [**CBaseFilter::Unregister**](cbasefilter-unregister.md) methods.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2f48e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f48e-107">Syntax</span></span>


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a><span data-ttu-id="2f48e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f48e-108">Parameters</span></span>

<span data-ttu-id="2f48e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2f48e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f48e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f48e-110">Return value</span></span>

<span data-ttu-id="2f48e-111">Retourne un pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) contenant des informations d’inscription pour le filtre.</span><span class="sxs-lookup"><span data-stu-id="2f48e-111">Returns a pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure containing registration information for the filter.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f48e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2f48e-112">Remarks</span></span>

<span data-ttu-id="2f48e-113">La classe de base retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2f48e-113">The base class returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f48e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f48e-114">Requirements</span></span>



| <span data-ttu-id="2f48e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f48e-115">Requirement</span></span> | <span data-ttu-id="2f48e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f48e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f48e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f48e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2f48e-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f48e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f48e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f48e-119">Library</span></span><br/> | <dl> <span data-ttu-id="2f48e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2f48e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f48e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f48e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f48e-122">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="2f48e-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




