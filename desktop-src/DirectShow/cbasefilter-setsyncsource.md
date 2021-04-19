---
description: 'La méthode SetSyncSource définit une horloge de référence pour le filtre. Cette méthode implémente la méthode IMediaFilter :: SetSyncSource.'
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Méthode CBaseFilter. SetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8eaab23f1afd7e7b502d6828bc3f10cbfec49410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541454"
---
# <a name="cbasefiltersetsyncsource-method"></a><span data-ttu-id="17b55-104">Méthode CBaseFilter. SetSyncSource</span><span class="sxs-lookup"><span data-stu-id="17b55-104">CBaseFilter.SetSyncSource method</span></span>

<span data-ttu-id="17b55-105">La méthode **SetSyncSource** définit une horloge de référence pour le filtre.</span><span class="sxs-lookup"><span data-stu-id="17b55-105">The **SetSyncSource** method sets a reference clock for the filter.</span></span> <span data-ttu-id="17b55-106">Cette méthode implémente la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="17b55-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b55-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17b55-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="17b55-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17b55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b55-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="17b55-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="17b55-110">Pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) de l’horloge, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="17b55-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b55-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17b55-111">Return value</span></span>

<span data-ttu-id="17b55-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="17b55-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17b55-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17b55-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b55-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17b55-114">Requirements</span></span>



| <span data-ttu-id="17b55-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17b55-115">Requirement</span></span> | <span data-ttu-id="17b55-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="17b55-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b55-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="17b55-117">Header</span></span><br/>  | <dl> <span data-ttu-id="17b55-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17b55-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="17b55-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17b55-119">Library</span></span><br/> | <dl> <span data-ttu-id="17b55-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="17b55-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b55-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17b55-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b55-122">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="17b55-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




