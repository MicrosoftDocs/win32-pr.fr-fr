---
description: La méthode BeginFlush commence une opération de vidage.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Méthode COutputQueue. BeginFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522816"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="14881-103">Méthode COutputQueue. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="14881-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="14881-104">La `BeginFlush` méthode commence une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="14881-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14881-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14881-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="14881-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14881-106">Parameters</span></span>

<span data-ttu-id="14881-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="14881-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14881-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14881-108">Return value</span></span>

<span data-ttu-id="14881-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="14881-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14881-110">Notes</span><span class="sxs-lookup"><span data-stu-id="14881-110">Remarks</span></span>

<span data-ttu-id="14881-111">Cette méthode définit la variable de membre [**COutputQueue :: m \_ BFlushing**](coutputqueue-m-bflushing.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="14881-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="14881-112">Si l’objet utilise un thread, le thread appelle la méthode [**COutputQueue :: FreeSamples**](coutputqueue-freesamples.md) pour libérer les échantillons en attente.</span><span class="sxs-lookup"><span data-stu-id="14881-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="14881-113">Dans le cas contraire, l’objet appelle **FreeSamples** pendant la méthode [**COutputQueue :: EndFlush**](coutputqueue-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="14881-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="14881-114">Cette méthode définit également la variable de membre [**COutputQueue :: m \_ HR**](coutputqueue-m-hr.md) sur S \_ false, ce qui provoque l’annulation de tous les nouveaux exemples de l’objet.</span><span class="sxs-lookup"><span data-stu-id="14881-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="14881-115">L’objet transmet la notification de vidage en aval en appelant la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="14881-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="14881-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14881-116">Requirements</span></span>



| <span data-ttu-id="14881-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14881-117">Requirement</span></span> | <span data-ttu-id="14881-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="14881-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14881-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="14881-119">Header</span></span><br/>  | <dl> <span data-ttu-id="14881-120"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14881-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="14881-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14881-121">Library</span></span><br/> | <dl> <span data-ttu-id="14881-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="14881-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14881-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14881-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14881-124">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="14881-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




