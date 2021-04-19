---
description: La méthode EOS met à jour les horodatages mis en cache après une notification de fin de flux.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: CRendererPosPassThru. EOS, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543948"
---
# <a name="crendererpospassthrueos-method"></a><span data-ttu-id="77f59-103">CRendererPosPassThru. EOS, méthode</span><span class="sxs-lookup"><span data-stu-id="77f59-103">CRendererPosPassThru.EOS method</span></span>

<span data-ttu-id="77f59-104">La `EOS` méthode met à jour les horodatages mis en cache après une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="77f59-104">The `EOS` method updates the cached time stamps after an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77f59-105">Syntax</span></span>


```C++
HRESULT EOS();
```



## <a name="parameters"></a><span data-ttu-id="77f59-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77f59-106">Parameters</span></span>

<span data-ttu-id="77f59-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="77f59-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="77f59-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77f59-108">Return value</span></span>

<span data-ttu-id="77f59-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77f59-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="77f59-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="77f59-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="77f59-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="77f59-111">Return code</span></span>                                                                            | <span data-ttu-id="77f59-112">Description</span><span class="sxs-lookup"><span data-stu-id="77f59-112">Description</span></span>                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="77f59-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="77f59-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="77f59-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="77f59-114">Success.</span></span><br/>                                       |
| <dl> <span data-ttu-id="77f59-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="77f59-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="77f59-116">Échec.</span><span class="sxs-lookup"><span data-stu-id="77f59-116">Failure.</span></span> <span data-ttu-id="77f59-117">Le filtre n’est peut-être pas diffusé.</span><span class="sxs-lookup"><span data-stu-id="77f59-117">Possibly the filter is not streaming.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="77f59-118">Notes</span><span class="sxs-lookup"><span data-stu-id="77f59-118">Remarks</span></span>

<span data-ttu-id="77f59-119">Le filtre doit appeler cette méthode lorsqu’il reçoit une notification de fin de flux ([**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span><span class="sxs-lookup"><span data-stu-id="77f59-119">The filter should call this method when it receives an end-of-stream notification ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span></span> <span data-ttu-id="77f59-120">La méthode définit les horodatages mis en cache comme étant égaux à la position d’arrêt, ce qui garantit que la méthode [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retourne les valeurs correctes à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="77f59-120">The method sets both cached time stamps equal to the stop position, ensuring that the [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the correct values at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f59-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77f59-121">Requirements</span></span>



| <span data-ttu-id="77f59-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77f59-122">Requirement</span></span> | <span data-ttu-id="77f59-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="77f59-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f59-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="77f59-124">Header</span></span><br/>  | <dl> <span data-ttu-id="77f59-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77f59-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77f59-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77f59-126">Library</span></span><br/> | <dl> <span data-ttu-id="77f59-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="77f59-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




