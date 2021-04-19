---
description: 'La méthode Receive reçoit l’exemple de support suivant dans le flux. Cette méthode remplace la méthode CBaseInputPin :: Receive.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: CRendererInputPin. Receive, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540684"
---
# <a name="crendererinputpinreceive-method"></a><span data-ttu-id="bb21e-104">CRendererInputPin. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="bb21e-104">CRendererInputPin.Receive method</span></span>

<span data-ttu-id="bb21e-105">La `Receive` méthode reçoit l’échantillon de média suivant dans le flux.</span><span class="sxs-lookup"><span data-stu-id="bb21e-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="bb21e-106">Cette méthode remplace la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="bb21e-106">This method overrides the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb21e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb21e-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="bb21e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb21e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb21e-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="bb21e-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="bb21e-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="bb21e-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb21e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb21e-111">Return value</span></span>

<span data-ttu-id="bb21e-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb21e-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb21e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bb21e-113">Remarks</span></span>

<span data-ttu-id="bb21e-114">Cette méthode appelle la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) du filtre, qui gère le rendu.</span><span class="sxs-lookup"><span data-stu-id="bb21e-114">This method calls the filter's [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, which handles the rendering.</span></span> <span data-ttu-id="bb21e-115">Si cette méthode échoue, le code PIN envoie un \_ événement EC ERRORABORT.</span><span class="sxs-lookup"><span data-stu-id="bb21e-115">If that method fails, the pin sends an EC\_ERRORABORT event.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb21e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb21e-116">Requirements</span></span>



| <span data-ttu-id="bb21e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb21e-117">Requirement</span></span> | <span data-ttu-id="bb21e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb21e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb21e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb21e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bb21e-120"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb21e-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb21e-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb21e-121">Library</span></span><br/> | <dl> <span data-ttu-id="bb21e-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb21e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb21e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb21e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb21e-124">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="bb21e-124">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




