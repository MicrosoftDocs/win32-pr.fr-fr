---
description: Indicateur qui spécifie si le filtre a envoyé une notification de fin de flux.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Membre CTransformFilter :: m_bEOSDelivered (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541668"
---
# <a name="ctransformfilterm_beosdelivered-member"></a><span data-ttu-id="3798b-103">CTransformFilter :: m \_ bEOSDelivered, membre</span><span class="sxs-lookup"><span data-stu-id="3798b-103">CTransformFilter::m\_bEOSDelivered member</span></span>

<span data-ttu-id="3798b-104">Indicateur qui spécifie si le filtre a envoyé une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="3798b-104">Flag that indicates whether the filter has sent an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="3798b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3798b-105">Syntax</span></span>


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a><span data-ttu-id="3798b-106">Notes</span><span class="sxs-lookup"><span data-stu-id="3798b-106">Remarks</span></span>

<span data-ttu-id="3798b-107">Si le filtre s’interrompt lorsqu’il n’a pas de connexion d’entrée, il envoie une notification de fin de flux en aval et définit cet indicateur sur **true**.</span><span class="sxs-lookup"><span data-stu-id="3798b-107">If the filter pauses when it does not have an input connection, it sends an end-of-stream notification downstream and sets this flag to **TRUE**.</span></span> <span data-ttu-id="3798b-108">La notification de fin de flux garantit que le filtre en aval n’attend pas les exemples.</span><span class="sxs-lookup"><span data-stu-id="3798b-108">The end-of-stream notification ensures that the downstream filter does not wait for samples.</span></span> <span data-ttu-id="3798b-109">Notez que la méthode [**EndOfStream**](ctransformfilter-endofstream.md) du filtre ne définit pas cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="3798b-109">Note that the filter's [**EndOfStream**](ctransformfilter-endofstream.md) method does not set this flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="3798b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3798b-110">Requirements</span></span>



| <span data-ttu-id="3798b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3798b-111">Requirement</span></span> | <span data-ttu-id="3798b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3798b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3798b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="3798b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3798b-114"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3798b-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3798b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3798b-115">Library</span></span><br/> | <dl> <span data-ttu-id="3798b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3798b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3798b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3798b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3798b-118">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="3798b-118">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




