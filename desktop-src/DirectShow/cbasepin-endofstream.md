---
description: 'La méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode implémente la méthode IPin :: EndOfStream. Appelez cette méthode uniquement sur les broches d’entrée.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Méthode CBasePin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545658"
---
# <a name="cbasepinendofstream-method"></a><span data-ttu-id="a4f15-105">Méthode CBasePin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="a4f15-105">CBasePin.EndOfStream method</span></span>

<span data-ttu-id="a4f15-106">La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="a4f15-106">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="a4f15-107">Cette méthode implémente la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="a4f15-107">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span> <span data-ttu-id="a4f15-108">Appelez cette méthode uniquement sur les broches d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a4f15-108">Call this method only on input pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f15-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4f15-109">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="a4f15-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4f15-110">Parameters</span></span>

<span data-ttu-id="a4f15-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a4f15-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4f15-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4f15-112">Return value</span></span>

<span data-ttu-id="a4f15-113">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a4f15-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f15-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a4f15-114">Remarks</span></span>

<span data-ttu-id="a4f15-115">Le filtre doit passer des notifications de fin de flux en aval, aux broches d’entrée des filtres connectés.</span><span class="sxs-lookup"><span data-stu-id="a4f15-115">The filter should pass end-of-stream notifications downstream, to the input pins of connected filters.</span></span> <span data-ttu-id="a4f15-116">Si le filtre est un convertisseur, il doit envoyer une notification d’événements [**EC \_ complet**](ec-complete.md) au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="a4f15-116">If the filter is a renderer, it should post an [**EC\_COMPLETE**](ec-complete.md) event notification to the filter graph manager.</span></span> <span data-ttu-id="a4f15-117">Pour plus d’informations, consultez [Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="a4f15-117">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="a4f15-118">Dans la classe de base, cette méthode n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="a4f15-118">In the base class, this method does nothing.</span></span> <span data-ttu-id="a4f15-119">Les classes dérivées doivent remplacer cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a4f15-119">Derived classes should override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f15-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4f15-120">Requirements</span></span>



| <span data-ttu-id="a4f15-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4f15-121">Requirement</span></span> | <span data-ttu-id="a4f15-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f15-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f15-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4f15-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a4f15-124"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f15-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a4f15-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a4f15-125">Library</span></span><br/> | <dl> <span data-ttu-id="a4f15-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a4f15-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f15-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4f15-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f15-128">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="a4f15-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




