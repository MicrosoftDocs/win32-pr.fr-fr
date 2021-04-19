---
description: 'La méthode Receive reçoit l’exemple de support suivant dans le flux. Cette méthode implémente la méthode IMemInputPin :: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: CTransformInputPin. Receive, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531132"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="afc45-104">CTransformInputPin. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="afc45-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="afc45-105">La `Receive` méthode reçoit l’échantillon de média suivant dans le flux.</span><span class="sxs-lookup"><span data-stu-id="afc45-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="afc45-106">Cette méthode implémente la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="afc45-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc45-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afc45-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="afc45-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afc45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc45-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="afc45-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="afc45-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="afc45-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc45-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="afc45-111">Return value</span></span>

<span data-ttu-id="afc45-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afc45-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="afc45-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="afc45-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="afc45-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="afc45-114">Return code</span></span>                                                                             | <span data-ttu-id="afc45-115">Description</span><span class="sxs-lookup"><span data-stu-id="afc45-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="afc45-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="afc45-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="afc45-117">Le code PIN est en cours de vidage ; l’exemple a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="afc45-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="afc45-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="afc45-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="afc45-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="afc45-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="afc45-120">Notes</span><span class="sxs-lookup"><span data-stu-id="afc45-120">Remarks</span></span>

<span data-ttu-id="afc45-121">Cette méthode appelle la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) du pin, qui vérifie l’état de diffusion en continu du pin et vérifie les modifications de format dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="afc45-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="afc45-122">Elle appelle ensuite la méthode [**CTransformFilter :: Receive**](ctransformfilter-receive.md) du filtre, qui traite l’exemple et le remet en aval.</span><span class="sxs-lookup"><span data-stu-id="afc45-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="afc45-123">Si le filtre doit accéder à l’exemple après le retour de cette méthode, il doit contenir un décompte de références en appelant la méthode **IUnknown :: AddRef** sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="afc45-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="afc45-124">Par exemple, certains filtres de décodeur ont besoin de l’exemple actuel pour décoder l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="afc45-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc45-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afc45-125">Requirements</span></span>



| <span data-ttu-id="afc45-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afc45-126">Requirement</span></span> | <span data-ttu-id="afc45-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="afc45-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc45-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="afc45-128">Header</span></span><br/>  | <dl> <span data-ttu-id="afc45-129"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afc45-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="afc45-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="afc45-130">Library</span></span><br/> | <dl> <span data-ttu-id="afc45-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="afc45-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




