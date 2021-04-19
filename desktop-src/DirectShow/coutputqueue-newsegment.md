---
description: La méthode NewSegment fournit un nouveau segment à la broche d’entrée.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Méthode COutputQueue. NewSegment (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538126"
---
# <a name="coutputqueuenewsegment-method"></a><span data-ttu-id="78d2f-103">Méthode COutputQueue. NewSegment</span><span class="sxs-lookup"><span data-stu-id="78d2f-103">COutputQueue.NewSegment method</span></span>

<span data-ttu-id="78d2f-104">La `NewSegment` méthode remet un nouveau segment à la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="78d2f-104">The `NewSegment` method delivers a new segment to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d2f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78d2f-105">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="78d2f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78d2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d2f-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="78d2f-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="78d2f-108">Position du média de départ du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="78d2f-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="78d2f-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="78d2f-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="78d2f-110">Position du média de fin du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="78d2f-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="78d2f-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="78d2f-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="78d2f-112">Taux auquel ce segment doit être traité, sous la forme d’un pourcentage du taux d’origine.</span><span class="sxs-lookup"><span data-stu-id="78d2f-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d2f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78d2f-113">Return value</span></span>

<span data-ttu-id="78d2f-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="78d2f-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78d2f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="78d2f-115">Remarks</span></span>

<span data-ttu-id="78d2f-116">Si l’objet utilise un thread, il met en file d’attente les éléments suivants, dans l’ordre :</span><span class="sxs-lookup"><span data-stu-id="78d2f-116">If the object is using a thread, it queues the following items, in order:</span></span>

-   <span data-ttu-id="78d2f-117">NOUVEAU \_ message de contrôle de segment.</span><span class="sxs-lookup"><span data-stu-id="78d2f-117">A NEW\_SEGMENT control message.</span></span>
-   <span data-ttu-id="78d2f-118">Données de segment.</span><span class="sxs-lookup"><span data-stu-id="78d2f-118">The segment data.</span></span>

<span data-ttu-id="78d2f-119">Le nouveau \_ message de segment avertit le thread que l’élément suivant de la file d’attente contiendra les données de segment.</span><span class="sxs-lookup"><span data-stu-id="78d2f-119">The NEW\_SEGMENT message notifies the thread that the next item on the queue will contain segment data.</span></span> <span data-ttu-id="78d2f-120">Les données de segment sont regroupées dans une structure, déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="78d2f-120">The segment data is bundled in a structure, declared as follows:</span></span>


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



<span data-ttu-id="78d2f-121">Le thread appelle la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sur la broche d’entrée, à l’aide des données fournies dans la structure.</span><span class="sxs-lookup"><span data-stu-id="78d2f-121">The thread calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin, using the data given in the structure.</span></span>

<span data-ttu-id="78d2f-122">Si l’objet n’utilise pas de thread, il appelle la méthode [**COutputQueue :: SendAnyway**](coutputqueue-sendanyway.md) pour remettre tous les échantillons en attente.</span><span class="sxs-lookup"><span data-stu-id="78d2f-122">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="78d2f-123">Ensuite, il appelle **IPIN :: NewSegment** sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="78d2f-123">Then it calls **IPin::NewSegment** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d2f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78d2f-124">Requirements</span></span>



| <span data-ttu-id="78d2f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78d2f-125">Requirement</span></span> | <span data-ttu-id="78d2f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="78d2f-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78d2f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="78d2f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="78d2f-128"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78d2f-128"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78d2f-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78d2f-129">Library</span></span><br/> | <dl> <span data-ttu-id="78d2f-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="78d2f-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d2f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78d2f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d2f-132">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="78d2f-132">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




