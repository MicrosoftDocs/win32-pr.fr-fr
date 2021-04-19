---
description: La méthode ReconnectPin rompt une connexion de code confidentiel existante et la reconnecte au même code PIN, à l’aide d’un type de média spécifié.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Méthode CBaseFilter. ReconnectPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532496"
---
# <a name="cbasefilterreconnectpin-method"></a><span data-ttu-id="9d93b-103">Méthode CBaseFilter. ReconnectPin</span><span class="sxs-lookup"><span data-stu-id="9d93b-103">CBaseFilter.ReconnectPin method</span></span>

<span data-ttu-id="9d93b-104">La `ReconnectPin` méthode interrompt une connexion de code confidentiel existante et la reconnecte au même code confidentiel, à l’aide d’un type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d93b-104">The `ReconnectPin` method breaks an existing pin connection and reconnects it to the same pin, using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d93b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d93b-105">Syntax</span></span>


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="9d93b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d93b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d93b-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="9d93b-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9d93b-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du pin.</span><span class="sxs-lookup"><span data-stu-id="9d93b-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9d93b-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="9d93b-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="9d93b-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui spécifie le type de média, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="9d93b-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d93b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d93b-111">Return value</span></span>

<span data-ttu-id="9d93b-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d93b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9d93b-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d93b-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9d93b-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9d93b-114">Return code</span></span>                                                                                   | <span data-ttu-id="9d93b-115">Description</span><span class="sxs-lookup"><span data-stu-id="9d93b-115">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d93b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d93b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9d93b-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9d93b-117">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="9d93b-118"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="9d93b-118"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="9d93b-119">la variable de membre [**m \_ pGraph**](cbasefilter-m-pgraph.md) a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9d93b-119">[**m\_pGraph**](cbasefilter-m-pgraph.md) member variable is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9d93b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="9d93b-120">Remarks</span></span>

<span data-ttu-id="9d93b-121">Cette méthode appelle la méthode [**IFilterGraph2 :: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9d93b-121">This method calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span> <span data-ttu-id="9d93b-122">Si l’interface [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) n’est pas disponible, la méthode appelle [**IFilterGraph :: reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span><span class="sxs-lookup"><span data-stu-id="9d93b-122">If the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface is not available, the method calls [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d93b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d93b-123">Requirements</span></span>



| <span data-ttu-id="9d93b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d93b-124">Requirement</span></span> | <span data-ttu-id="9d93b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d93b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d93b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d93b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9d93b-127"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d93b-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d93b-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d93b-128">Library</span></span><br/> | <dl> <span data-ttu-id="9d93b-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d93b-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d93b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d93b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d93b-131">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="9d93b-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




