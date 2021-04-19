---
description: La méthode ShouldDrawSampleNow détermine si la vidéo doit être dessinée sans définir un lien de notification de minuterie avec l’horloge.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Méthode CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523901"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a><span data-ttu-id="63caf-103">Méthode CBaseVideoRenderer. ShouldDrawSampleNow</span><span class="sxs-lookup"><span data-stu-id="63caf-103">CBaseVideoRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="63caf-104">La `ShouldDrawSampleNow` méthode détermine si la vidéo doit être dessinée sans définir un lien de notification de minuterie avec l’horloge.</span><span class="sxs-lookup"><span data-stu-id="63caf-104">The `ShouldDrawSampleNow` method determines if the video should be drawn without setting a timer advise link with the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="63caf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63caf-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a><span data-ttu-id="63caf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63caf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63caf-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="63caf-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="63caf-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="63caf-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface for the sample.</span></span>

</dd> <dt>

<span data-ttu-id="63caf-109">*ptrStart*</span><span class="sxs-lookup"><span data-stu-id="63caf-109">*ptrStart*</span></span> 
</dt> <dd>

<span data-ttu-id="63caf-110">Pointeur vers l’heure de début du rendu.</span><span class="sxs-lookup"><span data-stu-id="63caf-110">Pointer to the time to begin rendering.</span></span>

</dd> <dt>

<span data-ttu-id="63caf-111">*ptrEnd*</span><span class="sxs-lookup"><span data-stu-id="63caf-111">*ptrEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="63caf-112">Pointeur vers le temps d’arrêt du rendu.</span><span class="sxs-lookup"><span data-stu-id="63caf-112">Pointer to the time to stop rendering.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63caf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63caf-113">Return value</span></span>

<span data-ttu-id="63caf-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63caf-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="63caf-115">Retourne \_ la valeur OK pour signifier un dessin à la fois sans attendre, s \_ false pour signifier dessiner à l' *ptrStart*, ou une erreur pour signifier ne pas dessiner l’exemple ; autrement dit, vous pouvez l’ignorer pour gagner du temps.</span><span class="sxs-lookup"><span data-stu-id="63caf-115">Returns S\_OK to mean draw at once without waiting, S\_FALSE to mean draw at time *ptrStart*, or an error to mean do not draw the sample; that is, skip it to save time.</span></span>

## <a name="remarks"></a><span data-ttu-id="63caf-116">Notes</span><span class="sxs-lookup"><span data-stu-id="63caf-116">Remarks</span></span>

<span data-ttu-id="63caf-117">Cette fonction membre substitue [**CBaseRenderer :: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span><span class="sxs-lookup"><span data-stu-id="63caf-117">This member function overrides [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63caf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63caf-118">Requirements</span></span>



| <span data-ttu-id="63caf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63caf-119">Requirement</span></span> | <span data-ttu-id="63caf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="63caf-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63caf-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="63caf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="63caf-122"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63caf-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63caf-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63caf-123">Library</span></span><br/> | <dl> <span data-ttu-id="63caf-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63caf-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63caf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63caf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63caf-126">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="63caf-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




