---
description: 'Tableau d’exemples de taille COutputQueue :: m \_ lBatchSize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Membre COutputQueue :: m_ppSamples (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543223"
---
# <a name="coutputqueuem_ppsamples-member"></a><span data-ttu-id="afcd3-103">COutputQueue :: m \_ ppSamples, membre</span><span class="sxs-lookup"><span data-stu-id="afcd3-103">COutputQueue::m\_ppSamples member</span></span>

<span data-ttu-id="afcd3-104">Tableau d’exemples de taille [**COutputQueue :: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).</span><span class="sxs-lookup"><span data-stu-id="afcd3-104">Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="afcd3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afcd3-105">Syntax</span></span>


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a><span data-ttu-id="afcd3-106">Notes</span><span class="sxs-lookup"><span data-stu-id="afcd3-106">Remarks</span></span>

<span data-ttu-id="afcd3-107">Le thread de travail extrait des exemples de la file d’attente et les place dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="afcd3-107">The worker thread pulls samples from the queue and places them in this array.</span></span> <span data-ttu-id="afcd3-108">Il passe le tableau à la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="afcd3-108">It passes the array to the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span> <span data-ttu-id="afcd3-109">Si l’objet n’utilise pas de thread de travail, l’objet place des exemples directement dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="afcd3-109">If the object is not using a worker thread, the object places samples directly into this array.</span></span> <span data-ttu-id="afcd3-110">La variable de membre de [**\_ liste COutputQueue :: m**](coutputqueue-m-list.md) contient la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="afcd3-110">The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="afcd3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afcd3-111">Requirements</span></span>



| <span data-ttu-id="afcd3-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afcd3-112">Requirement</span></span> | <span data-ttu-id="afcd3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="afcd3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afcd3-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="afcd3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="afcd3-115"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afcd3-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="afcd3-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="afcd3-116">Library</span></span><br/> | <dl> <span data-ttu-id="afcd3-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="afcd3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afcd3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afcd3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afcd3-119">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="afcd3-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




