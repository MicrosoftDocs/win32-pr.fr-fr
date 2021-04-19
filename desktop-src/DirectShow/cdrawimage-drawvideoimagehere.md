---
description: La méthode DrawVideoImageHere dessine une image à partir d’un exemple de média dans un contexte de périphérique spécifié.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Méthode CDrawImage. DrawVideoImageHere (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535953"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a><span data-ttu-id="03d65-103">Méthode CDrawImage. DrawVideoImageHere</span><span class="sxs-lookup"><span data-stu-id="03d65-103">CDrawImage.DrawVideoImageHere method</span></span>

<span data-ttu-id="03d65-104">La `DrawVideoImageHere` méthode dessine une image à partir d’un exemple de média dans un contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="03d65-104">The `DrawVideoImageHere` method draws an image from a media sample to a specified device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d65-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03d65-105">Syntax</span></span>


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a><span data-ttu-id="03d65-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03d65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d65-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="03d65-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="03d65-108">Handle vers un contexte de périphérique (Device Context), où le dessin se produira.</span><span class="sxs-lookup"><span data-stu-id="03d65-108">Handle to a device context, where the drawing will occur.</span></span>

</dd> <dt>

<span data-ttu-id="03d65-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="03d65-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="03d65-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple qui contient l’image.</span><span class="sxs-lookup"><span data-stu-id="03d65-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> <dt>

<span data-ttu-id="03d65-111">*lprcSrc*</span><span class="sxs-lookup"><span data-stu-id="03d65-111">*lprcSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="03d65-112">Pointeur désignant un rectangle source à utiliser pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="03d65-112">Pointer to a source rectangle to use for drawing.</span></span> <span data-ttu-id="03d65-113">Si la **valeur est null**, le rectangle dans [**CDrawImage :: m \_ SourceRect**](cdrawimage-m-sourcerect.md) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="03d65-113">If **NULL**, the rectangle in [**CDrawImage::m\_SourceRect**](cdrawimage-m-sourcerect.md) is used.</span></span>

</dd> <dt>

<span data-ttu-id="03d65-114">*lprcDst*</span><span class="sxs-lookup"><span data-stu-id="03d65-114">*lprcDst*</span></span> 
</dt> <dd>

<span data-ttu-id="03d65-115">Pointeur désignant un rectangle cible à utiliser pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="03d65-115">Pointer to a target rectangle to use for drawing.</span></span> <span data-ttu-id="03d65-116">Si la **valeur est null**, le rectangle dans [**CDrawImage :: m \_ TargetRect**](cdrawimage-m-targetrect.md) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="03d65-116">If **NULL**, the rectangle in [**CDrawImage::m\_TargetRect**](cdrawimage-m-targetrect.md) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d65-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03d65-117">Return value</span></span>

<span data-ttu-id="03d65-118">Retourne la **valeur true** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="03d65-118">Returns **TRUE** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d65-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03d65-119">Requirements</span></span>



| <span data-ttu-id="03d65-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03d65-120">Requirement</span></span> | <span data-ttu-id="03d65-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="03d65-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d65-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="03d65-122">Header</span></span><br/>  | <dl> <span data-ttu-id="03d65-123"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03d65-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03d65-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03d65-124">Library</span></span><br/> | <dl> <span data-ttu-id="03d65-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="03d65-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d65-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03d65-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d65-127">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="03d65-127">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




