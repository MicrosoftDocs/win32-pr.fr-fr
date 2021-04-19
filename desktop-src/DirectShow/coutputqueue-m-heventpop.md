---
description: 'Événement facultatif signalé chaque fois que l’objet supprime un échantillon de la file d’attente. La valeur est initialement NULL. Appelez la méthode COutputQueue :: SetPopEvent pour spécifier un handle d’événement.'
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Membre COutputQueue :: m_hEventPop (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520892"
---
# <a name="coutputqueuem_heventpop-member"></a><span data-ttu-id="9e37c-105">COutputQueue :: m \_ hEventPop, membre</span><span class="sxs-lookup"><span data-stu-id="9e37c-105">COutputQueue::m\_hEventPop member</span></span>

<span data-ttu-id="9e37c-106">Événement facultatif signalé chaque fois que l’objet supprime un échantillon de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9e37c-106">Optional event that is signaled whenever the object removes a sample from the queue.</span></span> <span data-ttu-id="9e37c-107">La valeur est initialement **null**.</span><span class="sxs-lookup"><span data-stu-id="9e37c-107">The value is initially **NULL**.</span></span> <span data-ttu-id="9e37c-108">Appelez la méthode [**COutputQueue :: SetPopEvent**](coutputqueue-setpopevent.md) pour spécifier un handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="9e37c-108">Call the [**COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) method to specify an event handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e37c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e37c-109">Syntax</span></span>


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a><span data-ttu-id="9e37c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e37c-110">Requirements</span></span>



| <span data-ttu-id="9e37c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e37c-111">Requirement</span></span> | <span data-ttu-id="9e37c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e37c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e37c-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e37c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9e37c-114"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e37c-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9e37c-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e37c-115">Library</span></span><br/> | <dl> <span data-ttu-id="9e37c-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9e37c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e37c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e37c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e37c-118">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="9e37c-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




