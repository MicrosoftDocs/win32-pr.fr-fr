---
description: Crée une copie de mémoire d’une image.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Méthode CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528111"
---
# <a name="cbasecontrolvideocopyimage-method"></a><span data-ttu-id="c614e-103">Méthode CBaseControlVideo. CopyImage</span><span class="sxs-lookup"><span data-stu-id="c614e-103">CBaseControlVideo.CopyImage method</span></span>

<span data-ttu-id="c614e-104">Crée une copie de mémoire d’une image.</span><span class="sxs-lookup"><span data-stu-id="c614e-104">Creates a memory copy of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="c614e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c614e-105">Syntax</span></span>


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="c614e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c614e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c614e-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c614e-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c614e-108">Pointeur vers l’exemple contenant l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="c614e-108">Pointer to the sample containing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="c614e-109">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="c614e-109">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c614e-110">Pointeur vers le format représentant l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="c614e-110">Pointer to the format representing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="c614e-111">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="c614e-111">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c614e-112">Pointeur vers la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="c614e-112">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c614e-113">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="c614e-113">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="c614e-114">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="c614e-114">Pointer to the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c614e-115">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="c614e-115">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="c614e-116">Pointeur vers le rectangle de la vidéo source.</span><span class="sxs-lookup"><span data-stu-id="c614e-116">Pointer to the source video rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c614e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c614e-117">Return value</span></span>

<span data-ttu-id="c614e-118">Si le paramètre *pVideoImage* est **null**, le paramètre *pBufferSize* est renseigné avec le nombre d’octets requis par la mémoire tampon de sortie pour stocker l’image.</span><span class="sxs-lookup"><span data-stu-id="c614e-118">If the *pVideoImage* parameter is **NULL**, the *pBufferSize* parameter is filled in with the number of bytes the output buffer requires to store the image.</span></span> <span data-ttu-id="c614e-119">Si la mémoire tampon transmise est trop petite ou si la fonction membre ne parvient pas à allouer suffisamment de mémoire, la fonction membre retourne E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c614e-119">If the buffer passed in is too small or the member function fails to allocate sufficient memory, the member function returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c614e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c614e-120">Remarks</span></span>

<span data-ttu-id="c614e-121">La fonction membre récupère l’image à partir de l’exemple et la copie dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="c614e-121">The member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="c614e-122">La section de la vidéo copiée dans la mémoire tampon de sortie reflète le rectangle source qui est défini par l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (bien qu’elle ne reflète pas le rectangle de destination).</span><span class="sxs-lookup"><span data-stu-id="c614e-122">The section of video copied into the output buffer reflects the source rectangle that is set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface (although it does not reflect the destination rectangle).</span></span>

## <a name="requirements"></a><span data-ttu-id="c614e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c614e-123">Requirements</span></span>



| <span data-ttu-id="c614e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c614e-124">Requirement</span></span> | <span data-ttu-id="c614e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c614e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c614e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c614e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c614e-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c614e-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c614e-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c614e-128">Library</span></span><br/> | <dl> <span data-ttu-id="c614e-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c614e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c614e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c614e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c614e-131">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="c614e-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




