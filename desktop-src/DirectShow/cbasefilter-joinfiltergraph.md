---
description: 'La méthode JoinFilterGraph avertit le filtre qu’il a rejoint un graphique de filtre. Cette méthode implémente la méthode IBaseFilter :: JoinFilterGraph.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Méthode CBaseFilter. JoinFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541689"
---
# <a name="cbasefilterjoinfiltergraph-method"></a><span data-ttu-id="5b476-104">Méthode CBaseFilter. JoinFilterGraph</span><span class="sxs-lookup"><span data-stu-id="5b476-104">CBaseFilter.JoinFilterGraph method</span></span>

<span data-ttu-id="5b476-105">La `JoinFilterGraph` méthode informe le filtre qu’elle a rejoint un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="5b476-105">The `JoinFilterGraph` method notifies the filter that it has joined or left a filter graph.</span></span> <span data-ttu-id="5b476-106">Cette méthode implémente la méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="5b476-106">This method implements the [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b476-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b476-107">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a><span data-ttu-id="5b476-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b476-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b476-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="5b476-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="5b476-110">Pointeur vers l’interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) du gestionnaire de graphique de filtre, ou **null** si le filtre quitte le graphique.</span><span class="sxs-lookup"><span data-stu-id="5b476-110">Pointer to the filter graph manager's [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface, or **NULL** if the filter is leaving the graph.</span></span>

</dd> <dt>

<span data-ttu-id="5b476-111">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b476-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b476-112">Pointeur vers une chaîne Unicode contenant un nom pour le filtre.</span><span class="sxs-lookup"><span data-stu-id="5b476-112">Pointer to a Unicode string containing a name for the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b476-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b476-113">Return value</span></span>

<span data-ttu-id="5b476-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b476-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b476-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5b476-115">Remarks</span></span>

<span data-ttu-id="5b476-116">Cette méthode définit la variable de membre [**CBaseFilter :: m \_ pGraph**](cbasefilter-m-pgraph.md) comme étant égale au paramètre *pGraph* .</span><span class="sxs-lookup"><span data-stu-id="5b476-116">This method sets the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable equal to the *pGraph* parameter.</span></span> <span data-ttu-id="5b476-117">Il interroge également un pointeur d’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) et le stocke dans la variable membre [**CBaseFilter :: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="5b476-117">It also queries for an [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface pointer and stores it in the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="5b476-118">Toutefois, le filtre ne conserve pas de nombre de références sur l’une de ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="5b476-118">However, the filter does not keep a reference count on either of these interfaces.</span></span> <span data-ttu-id="5b476-119">Cela créerait un nombre de références circulaires, car le gestionnaire de graphes de filtre conserve un décompte de références sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="5b476-119">Doing so would create a circular reference count, because the filter graph manager keeps a reference count on the filter.</span></span>

<span data-ttu-id="5b476-120">La méthode copie la chaîne spécifiée par *pname* dans la variable membre [**CBaseFilter :: m \_ pname**](cbasefilter-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="5b476-120">The method copies the string specified by *pName* into the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b476-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b476-121">Requirements</span></span>



| <span data-ttu-id="5b476-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b476-122">Requirement</span></span> | <span data-ttu-id="5b476-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b476-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b476-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b476-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5b476-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b476-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5b476-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5b476-126">Library</span></span><br/> | <dl> <span data-ttu-id="5b476-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5b476-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b476-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b476-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b476-129">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="5b476-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




