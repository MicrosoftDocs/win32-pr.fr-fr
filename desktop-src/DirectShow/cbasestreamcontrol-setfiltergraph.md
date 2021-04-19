---
description: La méthode SetFilterGraph spécifie le récepteur d’événements pour les événements de contrôle de flux.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Méthode CBaseStreamControl. SetFilterGraph (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529648"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a><span data-ttu-id="7fec5-103">Méthode CBaseStreamControl. SetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="7fec5-103">CBaseStreamControl.SetFilterGraph method</span></span>

<span data-ttu-id="7fec5-104">La `SetFilterGraph` méthode spécifie le récepteur d’événements pour les événements de contrôle de flux.</span><span class="sxs-lookup"><span data-stu-id="7fec5-104">The `SetFilterGraph` method specifies the event sink for stream control events.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fec5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fec5-105">Syntax</span></span>


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="7fec5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fec5-107">*pSink*</span><span class="sxs-lookup"><span data-stu-id="7fec5-107">*pSink*</span></span> 
</dt> <dd>

<span data-ttu-id="7fec5-108">Pointeur vers l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) du gestionnaire de graphique de filtre, ou **null** lorsque le filtre quitte le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="7fec5-108">Pointer to the Filter Graph Manager's [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, or **NULL** when the filter leaves the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fec5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fec5-109">Return value</span></span>

<span data-ttu-id="7fec5-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7fec5-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fec5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7fec5-111">Remarks</span></span>

<span data-ttu-id="7fec5-112">Appelez cette méthode à l’intérieur de la méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) du filtre.</span><span class="sxs-lookup"><span data-stu-id="7fec5-112">Call this method from inside the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="7fec5-113">La classe **CBaseStreamControl** utilise l’interface **IMediaEventSink** pour envoyer le contrôle de flux de [**ce qui \_ \_ \_ a démarré**](ec-stream-control-started.md) et les événements de [**contrôle de flux EC \_ \_ \_ arrêtés**](ec-stream-control-stopped.md) .</span><span class="sxs-lookup"><span data-stu-id="7fec5-113">The **CBaseStreamControl** class uses the **IMediaEventSink** interface to send [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) events.</span></span>

<span data-ttu-id="7fec5-114">Si votre filtre dérive de **CBaseFilter**, appelez d’abord la méthode [**CBaseFilter :: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , qui définit la variable de membre [**CBaseFilter :: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="7fec5-114">If your filter derives from **CBaseFilter**, first call the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, which sets the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="7fec5-115">Transmettez ensuite **m \_ pSink** à la `SetFilterGraph` méthode.</span><span class="sxs-lookup"><span data-stu-id="7fec5-115">Then pass **m\_pSink** to the `SetFilterGraph` method.</span></span> <span data-ttu-id="7fec5-116">Notez que **m \_ pSink** a la **valeur null** lorsque le filtre quitte le graphique, ce qui est correct.</span><span class="sxs-lookup"><span data-stu-id="7fec5-116">Note that **m\_pSink** is **NULL** when the filter leaves the graph, which is correct.</span></span>

## <a name="examples"></a><span data-ttu-id="7fec5-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="7fec5-117">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="7fec5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fec5-118">Requirements</span></span>



| <span data-ttu-id="7fec5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fec5-119">Requirement</span></span> | <span data-ttu-id="7fec5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fec5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fec5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fec5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7fec5-122"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fec5-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7fec5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7fec5-123">Library</span></span><br/> | <dl> <span data-ttu-id="7fec5-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7fec5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fec5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fec5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fec5-126">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="7fec5-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




