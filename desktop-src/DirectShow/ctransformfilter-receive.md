---
description: La méthode Receive reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: CTransformFilter. Receive, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523437"
---
# <a name="ctransformfilterreceive-method"></a><span data-ttu-id="3c902-103">CTransformFilter. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="3c902-103">CTransformFilter.Receive method</span></span>

<span data-ttu-id="3c902-104">La `Receive` méthode reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="3c902-104">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c902-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c902-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="3c902-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c902-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="3c902-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="3c902-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) sur l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3c902-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c902-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c902-109">Return value</span></span>

<span data-ttu-id="3c902-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c902-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3c902-111">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c902-111">Possible values include the following:</span></span>



| <span data-ttu-id="3c902-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3c902-112">Return code</span></span>                                                                             | <span data-ttu-id="3c902-113">Description</span><span class="sxs-lookup"><span data-stu-id="3c902-113">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="3c902-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3c902-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3c902-115">Le filtre amont doit cesser d’envoyer des exemples.</span><span class="sxs-lookup"><span data-stu-id="3c902-115">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="3c902-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c902-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3c902-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3c902-117">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="3c902-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3c902-118">Remarks</span></span>

<span data-ttu-id="3c902-119">La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un exemple.</span><span class="sxs-lookup"><span data-stu-id="3c902-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="3c902-120">Cette méthode appelle la méthode [**CTransformFilter :: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , qui prépare un nouvel exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="3c902-120">This method calls the [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) method, which prepares a new output sample.</span></span> <span data-ttu-id="3c902-121">Elle appelle ensuite la méthode [**CTransformFilter :: Transform**](ctransformfilter-transform.md) , que la classe dérivée doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="3c902-121">Then it calls the [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="3c902-122">La méthode **Transform** traite les données d’entrée et génère des données de sortie.</span><span class="sxs-lookup"><span data-stu-id="3c902-122">The **Transform** method processes the input data and produces output data.</span></span>

<span data-ttu-id="3c902-123">Si la méthode **Transform** retourne S \_ false, la `Receive` méthode supprime cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3c902-123">If the **Transform** method returns S\_FALSE, the `Receive` method drops this sample.</span></span> <span data-ttu-id="3c902-124">Sur le premier exemple supprimé, le filtre envoie un événement de [**\_ \_ modification de la qualité ce**](ec-quality-change.md) au gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="3c902-124">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="3c902-125">Dans le cas contraire, si la méthode **Transform** retourne \_ la valeur OK, le filtre remet l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="3c902-125">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="3c902-126">Pour ce faire, il appelle la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="3c902-126">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c902-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c902-127">Requirements</span></span>



| <span data-ttu-id="3c902-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c902-128">Requirement</span></span> | <span data-ttu-id="3c902-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c902-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c902-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c902-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3c902-131"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c902-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3c902-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c902-132">Library</span></span><br/> | <dl> <span data-ttu-id="3c902-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3c902-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c902-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c902-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c902-135">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="3c902-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




