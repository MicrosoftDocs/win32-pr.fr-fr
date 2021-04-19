---
description: La méthode IsSpecialSample détermine si les données mises en file d’attente sont des messages de contrôle.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Méthode COutputQueue. IsSpecialSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535894"
---
# <a name="coutputqueueisspecialsample-method"></a><span data-ttu-id="2064f-103">Méthode COutputQueue. IsSpecialSample</span><span class="sxs-lookup"><span data-stu-id="2064f-103">COutputQueue.IsSpecialSample method</span></span>

<span data-ttu-id="2064f-104">La `IsSpecialSample` méthode détermine si les données mises en file d’attente sont des messages de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2064f-104">The `IsSpecialSample` method determines whether queued data is a control message.</span></span>

## <a name="syntax"></a><span data-ttu-id="2064f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2064f-105">Syntax</span></span>


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="2064f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2064f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2064f-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="2064f-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2064f-108">Pointeur vers un élément de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2064f-108">Pointer to an item in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2064f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2064f-109">Return value</span></span>

<span data-ttu-id="2064f-110">Retourne la **valeur true** si *pSample* est un message de contrôle, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2064f-110">Returns **TRUE** if *pSample* is a control message, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2064f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2064f-111">Remarks</span></span>

<span data-ttu-id="2064f-112">La méthode [**COutputQueue :: QueueSample**](coutputqueue-queuesample.md) peut recevoir des messages de contrôle en plus des exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="2064f-112">The [**COutputQueue::QueueSample**](coutputqueue-queuesample.md) method can receive control messages in addition to media samples.</span></span> <span data-ttu-id="2064f-113">Un message de contrôle est une constante définie (castée en un \_ type PTR long) qui indique au thread d’effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="2064f-113">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform an action.</span></span> <span data-ttu-id="2064f-114">Les messages de contrôle ne contiennent pas de données multimédias.</span><span class="sxs-lookup"><span data-stu-id="2064f-114">Control messages do not contain media data.</span></span> <span data-ttu-id="2064f-115">Pour plus d’informations, consultez **COutputQueue :: QueueSample**.</span><span class="sxs-lookup"><span data-stu-id="2064f-115">For more information, see **COutputQueue::QueueSample**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2064f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2064f-116">Requirements</span></span>



| <span data-ttu-id="2064f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2064f-117">Requirement</span></span> | <span data-ttu-id="2064f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2064f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2064f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="2064f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2064f-120"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2064f-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2064f-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2064f-121">Library</span></span><br/> | <dl> <span data-ttu-id="2064f-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2064f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2064f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2064f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2064f-124">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="2064f-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




