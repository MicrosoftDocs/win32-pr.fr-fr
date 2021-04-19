---
description: La méthode SlowRender dessine l’image vidéo à l’aide des fonctions SetDIBitsToDevice ou StretchDIBits.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Méthode CDrawImage. SlowRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528092"
---
# <a name="cdrawimageslowrender-method"></a><span data-ttu-id="9f7e3-103">Méthode CDrawImage. SlowRender</span><span class="sxs-lookup"><span data-stu-id="9f7e3-103">CDrawImage.SlowRender method</span></span>

<span data-ttu-id="9f7e3-104">La `SlowRender` méthode dessine l’image vidéo à l’aide des fonctions **SetDIBitsToDevice** ou **StretchDIBits** .</span><span class="sxs-lookup"><span data-stu-id="9f7e3-104">The `SlowRender` method draws the video image using the **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f7e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f7e3-105">Syntax</span></span>


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="9f7e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f7e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f7e3-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="9f7e3-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="9f7e3-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple qui contient l’image.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f7e3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f7e3-109">Return value</span></span>

<span data-ttu-id="9f7e3-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f7e3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9f7e3-111">Remarks</span></span>

<span data-ttu-id="9f7e3-112">Si [**CDrawImage :: UsingImageAllocator**](cdrawimage-usingimageallocator.md) retourne **false**, la méthode [**CDrawImage ::D rawimage**](cdrawimage-drawimage.md) utilise `SlowRender` pour dessiner l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-112">If [**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md) returns **FALSE**, the [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method uses `SlowRender` to draw the video image.</span></span> <span data-ttu-id="9f7e3-113">Dans le cas contraire, DrawImage utilise la méthode **FastRender** .</span><span class="sxs-lookup"><span data-stu-id="9f7e3-113">Otherwise, DrawImage uses the **FastRender** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f7e3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f7e3-114">Requirements</span></span>



| <span data-ttu-id="9f7e3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f7e3-115">Requirement</span></span> | <span data-ttu-id="9f7e3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f7e3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f7e3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f7e3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9f7e3-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f7e3-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f7e3-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9f7e3-119">Library</span></span><br/> | <dl> <span data-ttu-id="9f7e3-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f7e3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f7e3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f7e3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f7e3-122">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="9f7e3-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="9f7e3-123">**CDrawImage::FastRender**</span><span class="sxs-lookup"><span data-stu-id="9f7e3-123">**CDrawImage::FastRender**</span></span>](cdrawimage-fastrender.md)
</dt> </dl>

 

 




