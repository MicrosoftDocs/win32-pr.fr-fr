---
description: La méthode ReceiveMultiple fournit un lot d’exemples de supports à la broche d’entrée.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Méthode COutputQueue. ReceiveMultiple (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532514"
---
# <a name="coutputqueuereceivemultiple-method"></a><span data-ttu-id="e6c4a-103">Méthode COutputQueue. ReceiveMultiple</span><span class="sxs-lookup"><span data-stu-id="e6c4a-103">COutputQueue.ReceiveMultiple method</span></span>

<span data-ttu-id="e6c4a-104">La `ReceiveMultiple` méthode remet un lot d’exemples de supports à la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-104">The `ReceiveMultiple` method delivers a batch of media samples to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c4a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6c4a-105">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="e6c4a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6c4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c4a-107">*ppSamples*</span><span class="sxs-lookup"><span data-stu-id="e6c4a-107">*ppSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c4a-108">Adresse d’un pointeur vers un tableau d’exemples.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-108">Address of a pointer to an array of samples.</span></span>

</dd> <dt>

<span data-ttu-id="e6c4a-109">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="e6c4a-109">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c4a-110">Nombre d’échantillons dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-110">Number of samples in the array.</span></span>

</dd> <dt>

<span data-ttu-id="e6c4a-111">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="e6c4a-111">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c4a-112">Pointeur vers une variable qui reçoit le nombre d’exemples remis avec succès.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-112">Pointer to a variable that receives the number of samples delivered successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6c4a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6c4a-113">Return value</span></span>

<span data-ttu-id="e6c4a-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6c4a-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e6c4a-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6c4a-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e6c4a-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e6c4a-116">Return code</span></span>                                                                             | <span data-ttu-id="e6c4a-117">Description</span><span class="sxs-lookup"><span data-stu-id="e6c4a-117">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6c4a-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e6c4a-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e6c4a-119">Notification de fin de flux reçue avant le traitement de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-119">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="e6c4a-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6c4a-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e6c4a-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-121">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="e6c4a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e6c4a-122">Remarks</span></span>

<span data-ttu-id="e6c4a-123">Si l’objet utilise un thread, cette méthode met en file d’attente tous les exemples passés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-123">If the object is using a thread, this method queues all of the samples passed in the array.</span></span> <span data-ttu-id="e6c4a-124">Dans le cas contraire, la méthode appelle la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6c4a-124">Otherwise, the method calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c4a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6c4a-125">Requirements</span></span>



| <span data-ttu-id="e6c4a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6c4a-126">Requirement</span></span> | <span data-ttu-id="e6c4a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6c4a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c4a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6c4a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e6c4a-129"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6c4a-129"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6c4a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6c4a-130">Library</span></span><br/> | <dl> <span data-ttu-id="e6c4a-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6c4a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c4a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6c4a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c4a-133">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="e6c4a-133">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




