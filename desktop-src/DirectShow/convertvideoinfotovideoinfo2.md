---
description: La fonction ConvertVideoInfoToVideoInfo2 convertit un type de média qui utilise VIDEOINFOHEADER en un type qui utilise VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: ConvertVideoInfoToVideoInfo2, fonction (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528358"
---
# <a name="convertvideoinfotovideoinfo2-function"></a><span data-ttu-id="b334b-103">ConvertVideoInfoToVideoInfo2 fonction)</span><span class="sxs-lookup"><span data-stu-id="b334b-103">ConvertVideoInfoToVideoInfo2 function</span></span>

<span data-ttu-id="b334b-104">La `ConvertVideoInfoToVideoInfo2` fonction convertit un type de média qui utilise [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en un type qui utilise [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="b334b-104">The `ConvertVideoInfoToVideoInfo2` function converts a media type that uses [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) to one that uses [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

## <a name="syntax"></a><span data-ttu-id="b334b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b334b-105">Syntax</span></span>


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b334b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b334b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b334b-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="b334b-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b334b-108">Pointeur vers la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à convertir.</span><span class="sxs-lookup"><span data-stu-id="b334b-108">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to convert.</span></span> <span data-ttu-id="b334b-109">La structure doit avoir le type de format \_ videoinfo.</span><span class="sxs-lookup"><span data-stu-id="b334b-109">The structure must have format type FORMAT\_VideoInfo.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b334b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b334b-110">Return value</span></span>

<span data-ttu-id="b334b-111">Retourne S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b334b-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b334b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b334b-112">Remarks</span></span>

<span data-ttu-id="b334b-113">Cette fonction alloue une nouvelle structure **VIDEOINFOHEADER2** , y copie les membres de la structure **VIDEOINFOHEADER** , puis remplace l’ancienne structure par la nouvelle structure dans le bloc de format du type de média.</span><span class="sxs-lookup"><span data-stu-id="b334b-113">This function allocates a new **VIDEOINFOHEADER2** structure, copies the members of the **VIDEOINFOHEADER** structure into it, and replaces the old structure with the new structure in the format block of the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b334b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b334b-114">Requirements</span></span>



| <span data-ttu-id="b334b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b334b-115">Requirement</span></span> | <span data-ttu-id="b334b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b334b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b334b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b334b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b334b-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b334b-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b334b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b334b-119">Library</span></span><br/> | <dl> <span data-ttu-id="b334b-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b334b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b334b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b334b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b334b-122">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="b334b-122">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




