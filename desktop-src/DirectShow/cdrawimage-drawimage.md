---
description: La méthode DrawImage dessine une image vidéo dans la fenêtre vidéo.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: CDrawImage. DrawImage, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526053"
---
# <a name="cdrawimagedrawimage-method"></a><span data-ttu-id="337c6-103">CDrawImage. DrawImage, méthode</span><span class="sxs-lookup"><span data-stu-id="337c6-103">CDrawImage.DrawImage method</span></span>

<span data-ttu-id="337c6-104">La `DrawImage` méthode dessine une image vidéo dans la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="337c6-104">The `DrawImage` method draws a video frame on the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="337c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="337c6-105">Syntax</span></span>


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="337c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="337c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="337c6-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="337c6-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="337c6-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple qui contient l’image.</span><span class="sxs-lookup"><span data-stu-id="337c6-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="337c6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="337c6-109">Return value</span></span>

<span data-ttu-id="337c6-110">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="337c6-110">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="337c6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="337c6-111">Remarks</span></span>

<span data-ttu-id="337c6-112">Cette méthode délègue à [**CDrawImage :: FastRender**](cdrawimage-fastrender.md) ou [**CDrawImage :: SlowRender**](cdrawimage-slowrender.md), selon que le filtre possède ou non l’allocateur qui a fourni l’exemple.</span><span class="sxs-lookup"><span data-stu-id="337c6-112">This method delegates to [**CDrawImage::FastRender**](cdrawimage-fastrender.md) or [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), depending on whether the filter owns the allocator that provided the sample.</span></span> <span data-ttu-id="337c6-113">Si le filtre est propriétaire de l’Allocator, il est garanti que l’exemple est un objet [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="337c6-113">If the filter does own the allocator, the sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="337c6-114">Dans ce cas, l’exemple utilise la mémoire partagée allouée par GDI, et l’image peut être dessinée à l’aide de **BitBlt** ou de **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="337c6-114">In that case, the sample uses shared memory allocated by GDI, and the image can be drawn using either **BitBlt** or **StretchBlt**.</span></span> <span data-ttu-id="337c6-115">Dans le cas contraire, les images doivent être dessinées à l’aide des fonctions **SetDIBitsToDevice** ou **StretchDIBits** plus lentes.</span><span class="sxs-lookup"><span data-stu-id="337c6-115">Otherwise, the images must be drawn using the slower **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

<span data-ttu-id="337c6-116">Dans les versions Debug, cette méthode appelle **DisplaySampleTimes** pour dessiner les horodatages de l’exemple sur l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="337c6-116">In debug builds, this method calls **DisplaySampleTimes** to draw the sample's time stamps over the video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="337c6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="337c6-117">Requirements</span></span>



| <span data-ttu-id="337c6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="337c6-118">Requirement</span></span> | <span data-ttu-id="337c6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="337c6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337c6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="337c6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="337c6-121"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="337c6-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="337c6-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="337c6-122">Library</span></span><br/> | <dl> <span data-ttu-id="337c6-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="337c6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337c6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="337c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337c6-125">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="337c6-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="337c6-126">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="337c6-126">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




