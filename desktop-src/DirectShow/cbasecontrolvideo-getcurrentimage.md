---
description: La méthode GetCurrentImage récupère une copie de l’image actuelle au niveau du convertisseur.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Méthode CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526699"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a><span data-ttu-id="eb235-103">Méthode CBaseControlVideo. GetCurrentImage</span><span class="sxs-lookup"><span data-stu-id="eb235-103">CBaseControlVideo.GetCurrentImage method</span></span>

<span data-ttu-id="eb235-104">La `GetCurrentImage` méthode récupère une copie de l’image actuelle au niveau du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="eb235-104">The `GetCurrentImage` method retrieves a copy of the current image at the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb235-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb235-105">Syntax</span></span>


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a><span data-ttu-id="eb235-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb235-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb235-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="eb235-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="eb235-108">Pointeur vers la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="eb235-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="eb235-109">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="eb235-109">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="eb235-110">Pointeur vers la mémoire tampon de sortie de l’image.</span><span class="sxs-lookup"><span data-stu-id="eb235-110">Pointer to the output buffer for the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb235-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb235-111">Return value</span></span>

<span data-ttu-id="eb235-112">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="eb235-112">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="eb235-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="eb235-113">Return code</span></span>                                                                                        | <span data-ttu-id="eb235-114">Description</span><span class="sxs-lookup"><span data-stu-id="eb235-114">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb235-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="eb235-115"><dt>**E\_FAIL**</dt></span></span> </dl>             | <span data-ttu-id="eb235-116">Échec.</span><span class="sxs-lookup"><span data-stu-id="eb235-116">Failure.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="eb235-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="eb235-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>       | <span data-ttu-id="eb235-118">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="eb235-118">Invalid argument.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="eb235-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="eb235-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>      | <span data-ttu-id="eb235-120">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="eb235-120">Out of memory.</span></span> <span data-ttu-id="eb235-121">Retourné lorsque le paramètre *pVideoInfo* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="eb235-121">Returned when the *pVideoInfo* parameter is **NULL**.</span></span><br/>   |
| <dl> <span data-ttu-id="eb235-122"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="eb235-122"><dt>**NOERROR**</dt></span></span> </dl>             | <span data-ttu-id="eb235-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="eb235-123">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="eb235-124"><dt>**VFW \_ E \_ non \_ suspendu**</dt></span><span class="sxs-lookup"><span data-stu-id="eb235-124"><dt>**VFW\_E\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="eb235-125">L’opération n’a pas pu être effectuée car le filtre n’est pas suspendu.</span><span class="sxs-lookup"><span data-stu-id="eb235-125">The operation could not be performed because the filter is not paused.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb235-126">Notes</span><span class="sxs-lookup"><span data-stu-id="eb235-126">Remarks</span></span>

<span data-ttu-id="eb235-127">Cette fonction membre récupère l’image à partir de l’exemple et la copie dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="eb235-127">This member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="eb235-128">La section de la vidéo copiée dans la mémoire tampon de sortie reflète le rectangle source défini par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="eb235-128">The section of video copied into the output buffer reflects the source rectangle set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="eb235-129">Elle ne reflète pas le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="eb235-129">It does not reflect the destination rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb235-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb235-130">Requirements</span></span>



| <span data-ttu-id="eb235-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb235-131">Requirement</span></span> | <span data-ttu-id="eb235-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb235-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb235-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb235-133">Header</span></span><br/>  | <dl> <span data-ttu-id="eb235-134"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb235-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb235-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb235-135">Library</span></span><br/> | <dl> <span data-ttu-id="eb235-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="eb235-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb235-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb235-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb235-138">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="eb235-138">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




