---
description: La méthode QueueSample met en file d’attente un exemple.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Méthode COutputQueue. QueueSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523479"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="4d785-103">Méthode COutputQueue. QueueSample</span><span class="sxs-lookup"><span data-stu-id="4d785-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="4d785-104">La `QueueSample` méthode met en file d’attente un exemple.</span><span class="sxs-lookup"><span data-stu-id="4d785-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d785-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d785-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="4d785-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d785-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="4d785-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4d785-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="4d785-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d785-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d785-109">Return value</span></span>

<span data-ttu-id="4d785-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4d785-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d785-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4d785-111">Remarks</span></span>

<span data-ttu-id="4d785-112">Cette méthode ajoute un exemple à la fin de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4d785-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="4d785-113">Maintenez la section critique avant d’appeler cette méthode et appelez-la uniquement lorsque l’objet utilise un thread pour remettre des exemples.</span><span class="sxs-lookup"><span data-stu-id="4d785-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="4d785-114">Pour déterminer si l’objet utilise un thread, appelez la méthode [**COutputQueue :: IsQueued**](coutputqueue-isqueued.md) .</span><span class="sxs-lookup"><span data-stu-id="4d785-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="4d785-115">Cette méthode peut également être utilisée pour placer des messages de contrôle dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4d785-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="4d785-116">Un message de contrôle est une constante définie (castée en un \_ type PTR long) qui indique au thread d’effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="4d785-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="4d785-117">La classe **COutputQueue** définit les messages de contrôle présentés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4d785-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



|               |                                        |
|---------------|----------------------------------------|
| <span data-ttu-id="4d785-118">Message</span><span class="sxs-lookup"><span data-stu-id="4d785-118">Message</span></span>       | <span data-ttu-id="4d785-119">Action</span><span class="sxs-lookup"><span data-stu-id="4d785-119">Action</span></span>                                 |
| <span data-ttu-id="4d785-120">\_paquet EOS</span><span class="sxs-lookup"><span data-stu-id="4d785-120">EOS\_PACKET</span></span>   | <span data-ttu-id="4d785-121">Fournir une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="4d785-121">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="4d785-122">NOUVEAU \_ segment</span><span class="sxs-lookup"><span data-stu-id="4d785-122">NEW\_SEGMENT</span></span>  | <span data-ttu-id="4d785-123">Fournissez un nouveau segment.</span><span class="sxs-lookup"><span data-stu-id="4d785-123">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="4d785-124">RÉINITIALISER le \_ paquet</span><span class="sxs-lookup"><span data-stu-id="4d785-124">RESET\_PACKET</span></span> | <span data-ttu-id="4d785-125">Réinitialisez l’état de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4d785-125">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="4d785-126">Envoyer le \_ paquet</span><span class="sxs-lookup"><span data-stu-id="4d785-126">SEND\_PACKET</span></span>  | <span data-ttu-id="4d785-127">Envoyer un lot partiel d’exemples.</span><span class="sxs-lookup"><span data-stu-id="4d785-127">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="4d785-128">Il s’agit d’une méthode protégée, que la classe **COutputQueue** utilise en interne.</span><span class="sxs-lookup"><span data-stu-id="4d785-128">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d785-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d785-129">Requirements</span></span>



| <span data-ttu-id="4d785-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d785-130">Requirement</span></span> | <span data-ttu-id="4d785-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d785-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d785-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d785-132">Header</span></span><br/>  | <dl> <span data-ttu-id="4d785-133"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d785-133"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d785-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d785-134">Library</span></span><br/> | <dl> <span data-ttu-id="4d785-135"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4d785-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d785-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d785-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d785-137">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="4d785-137">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




