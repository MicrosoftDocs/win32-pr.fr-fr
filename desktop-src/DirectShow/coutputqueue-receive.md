---
description: La méthode Receive fournit un exemple de support à la broche d’entrée.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: COutputQueue. Receive, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ce8a0d44730fa35b38cf6d738edd26168284a46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545345"
---
# <a name="coutputqueuereceive-method"></a><span data-ttu-id="2d634-103">COutputQueue. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="2d634-103">COutputQueue.Receive method</span></span>

<span data-ttu-id="2d634-104">La `Receive` méthode remet un échantillon de média à la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2d634-104">The `Receive` method delivers a media sample to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d634-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d634-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="2d634-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d634-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d634-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="2d634-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2d634-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="2d634-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d634-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d634-109">Return value</span></span>

<span data-ttu-id="2d634-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d634-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2d634-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d634-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2d634-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2d634-112">Return code</span></span>                                                                             | <span data-ttu-id="2d634-113">Description</span><span class="sxs-lookup"><span data-stu-id="2d634-113">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d634-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2d634-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2d634-115">Notification de fin de flux reçue avant le traitement de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="2d634-115">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="2d634-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2d634-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2d634-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2d634-117">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="2d634-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2d634-118">Remarks</span></span>

<span data-ttu-id="2d634-119">Cette méthode appelle la méthode [**COutputQueue :: ReceiveMultiple**](coutputqueue-receivemultiple.md) .</span><span class="sxs-lookup"><span data-stu-id="2d634-119">This method calls the [**COutputQueue::ReceiveMultiple**](coutputqueue-receivemultiple.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d634-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d634-120">Requirements</span></span>



| <span data-ttu-id="2d634-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d634-121">Requirement</span></span> | <span data-ttu-id="2d634-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d634-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d634-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d634-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2d634-124"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d634-124"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d634-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d634-125">Library</span></span><br/> | <dl> <span data-ttu-id="2d634-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2d634-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d634-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d634-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d634-128">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="2d634-128">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




