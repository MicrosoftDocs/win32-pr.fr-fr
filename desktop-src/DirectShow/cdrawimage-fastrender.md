---
description: La méthode FastRender dessine l’image vidéo à l’aide des fonctions BitBlt ou StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Méthode CDrawImage. FastRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541083"
---
# <a name="cdrawimagefastrender-method"></a><span data-ttu-id="d3df4-103">Méthode CDrawImage. FastRender</span><span class="sxs-lookup"><span data-stu-id="d3df4-103">CDrawImage.FastRender method</span></span>

<span data-ttu-id="d3df4-104">La `FastRender` méthode dessine l’image vidéo à l’aide des fonctions **BitBlt** ou **StretchBlt** .</span><span class="sxs-lookup"><span data-stu-id="d3df4-104">The `FastRender` method draws the video image using the **BitBlt** or **StretchBlt** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3df4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3df4-105">Syntax</span></span>


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="d3df4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3df4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3df4-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="d3df4-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d3df4-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple qui contient l’image.</span><span class="sxs-lookup"><span data-stu-id="d3df4-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3df4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3df4-109">Return value</span></span>

<span data-ttu-id="d3df4-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d3df4-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3df4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d3df4-111">Remarks</span></span>

<span data-ttu-id="d3df4-112">La méthode [**CDrawImage ::D rawimage**](cdrawimage-drawimage.md) appelle cette méthode, mais uniquement si l’allocateur pour la connexion est un objet [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="d3df4-112">The [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method calls this method, but only if the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span> <span data-ttu-id="d3df4-113">Dans ce cas, l’exemple de support est garanti comme un objet [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="d3df4-113">In that case, the media sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="d3df4-114">L’objet **CImageSample** utilise la fonction **CreateDIBSection** pour allouer de la mémoire partagée pour la bitmap, ce qui permet de dessiner l’image à l’aide de **BitBlt** ou de **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="d3df4-114">The **CImageSample** object uses the **CreateDIBSection** function to allocate shared memory for the bitmap, which makes it possible to draw the image using either **BitBlt** or **StretchBlt**.</span></span>

<span data-ttu-id="d3df4-115">Cette méthode appelle **BitBlt** si les rectangles source et cible correspondent exactement, ou **StretchBlt** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d3df4-115">This method calls **BitBlt** if the source and targer rectangles exactly match, or **StretchBlt** otherwise.</span></span>

<span data-ttu-id="d3df4-116">Si le filtre n’est pas propriétaire de l’allocateur, la méthode **DrawImage** utilise [**CDrawImage :: SlowRender**](cdrawimage-slowrender.md) pour dessiner l’image.</span><span class="sxs-lookup"><span data-stu-id="d3df4-116">If the filter does not own the allocator, the **DrawImage** method uses [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) to draw the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3df4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3df4-117">Requirements</span></span>



| <span data-ttu-id="d3df4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3df4-118">Requirement</span></span> | <span data-ttu-id="d3df4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3df4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3df4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3df4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d3df4-121"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3df4-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3df4-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d3df4-122">Library</span></span><br/> | <dl> <span data-ttu-id="d3df4-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d3df4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3df4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3df4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3df4-125">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="d3df4-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




