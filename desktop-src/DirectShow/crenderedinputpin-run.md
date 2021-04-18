---
description: 'La méthode Run indique au code confidentiel que le filtre est en cours d’exécution. Cette méthode remplace la méthode CBasePin :: Run.'
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: CRenderedInputPin. Run, méthode (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526110"
---
# <a name="crenderedinputpinrun-method"></a><span data-ttu-id="bc8a8-104">CRenderedInputPin. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="bc8a8-104">CRenderedInputPin.Run method</span></span>

<span data-ttu-id="bc8a8-105">La `Run` méthode notifie le code confidentiel que le filtre est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-105">The `Run` method notifies the pin that the filter is now running.</span></span> <span data-ttu-id="bc8a8-106">Cette méthode remplace la méthode [**CBasePin :: Run**](cbasepin-run.md) .</span><span class="sxs-lookup"><span data-stu-id="bc8a8-106">This method overrides the [**CBasePin::Run**](cbasepin-run.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8a8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc8a8-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="bc8a8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc8a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8a8-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="bc8a8-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="bc8a8-110">Heure de début passée à la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) du filtre.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-110">The start time that was passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8a8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc8a8-111">Return value</span></span>

<span data-ttu-id="bc8a8-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8a8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc8a8-113">Requirements</span></span>



| <span data-ttu-id="bc8a8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc8a8-114">Requirement</span></span> | <span data-ttu-id="bc8a8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc8a8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8a8-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc8a8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bc8a8-117"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc8a8-117"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bc8a8-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc8a8-118">Library</span></span><br/> | <dl> <span data-ttu-id="bc8a8-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bc8a8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc8a8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc8a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8a8-121">**CRenderedInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="bc8a8-121">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




