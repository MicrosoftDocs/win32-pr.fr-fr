---
description: La méthode GetVideoFormat récupère un exemple de vidéo qui représente le format vidéo actuel.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Méthode CBaseControlVideo. GetVideoFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529983"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a><span data-ttu-id="ad76d-103">Méthode CBaseControlVideo. GetVideoFormat</span><span class="sxs-lookup"><span data-stu-id="ad76d-103">CBaseControlVideo.GetVideoFormat method</span></span>

<span data-ttu-id="ad76d-104">La `GetVideoFormat` méthode récupère un exemple de vidéo qui représente le format vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="ad76d-104">The `GetVideoFormat` method retrieves a video sample that represents the current video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad76d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad76d-105">Syntax</span></span>


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a><span data-ttu-id="ad76d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad76d-106">Parameters</span></span>

<span data-ttu-id="ad76d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad76d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad76d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad76d-108">Return value</span></span>

<span data-ttu-id="ad76d-109">Retourne un pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) qui contient le format vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="ad76d-109">Returns a pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the current video format.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad76d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ad76d-110">Remarks</span></span>

<span data-ttu-id="ad76d-111">Pour retourner et vérifier certaines informations par le biais de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), l’objet doit connaître le format vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="ad76d-111">To return and check certain information through [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), the object must know the current video format.</span></span> <span data-ttu-id="ad76d-112">Elle obtient ces informations en appelant cette méthode virtuelle pure qui doit être substituée par les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="ad76d-112">It gets this information by calling this pure virtual method that derived classes must override.</span></span> <span data-ttu-id="ad76d-113">Cette fonction membre est appelée par les fonctions membres [**CBaseControlVideo**](cbasecontrolvideo.md) suivantes.</span><span class="sxs-lookup"><span data-stu-id="ad76d-113">This member function is called by the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="ad76d-114">**CBaseControlVideo::OnVideoSizeChange**</span><span class="sxs-lookup"><span data-stu-id="ad76d-114">**CBaseControlVideo::OnVideoSizeChange**</span></span>](cbasecontrolvideo-onvideosizechange.md)
-   [<span data-ttu-id="ad76d-115">**CBaseControlVideo :: obtient \_ AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="ad76d-115">**CBaseControlVideo::get\_AvgTimePerFrame**</span></span>](cbasecontrolvideo-get-avgtimeperframe.md)
-   [<span data-ttu-id="ad76d-116">**CBaseControlVideo :: obtient la \_ vitesse de transmission**</span><span class="sxs-lookup"><span data-stu-id="ad76d-116">**CBaseControlVideo::get\_BitRate**</span></span>](cbasecontrolvideo-get-bitrate.md)
-   [<span data-ttu-id="ad76d-117">**CBaseControlVideo :: obtient \_ BitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="ad76d-117">**CBaseControlVideo::get\_BitErrorRate**</span></span>](cbasecontrolvideo-get-biterrorrate.md)
-   [<span data-ttu-id="ad76d-118">**CBaseControlVideo :: obtient \_ VideoWidth**</span><span class="sxs-lookup"><span data-stu-id="ad76d-118">**CBaseControlVideo::get\_VideoWidth**</span></span>](cbasecontrolvideo-get-videowidth.md)
-   [<span data-ttu-id="ad76d-119">**CBaseControlVideo :: obtient \_ VideoHeight**</span><span class="sxs-lookup"><span data-stu-id="ad76d-119">**CBaseControlVideo::get\_VideoHeight**</span></span>](cbasecontrolvideo-get-videoheight.md)
-   [<span data-ttu-id="ad76d-120">**CBaseControlVideo::GetVideoPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="ad76d-120">**CBaseControlVideo::GetVideoPaletteEntries**</span></span>](cbasecontrolvideo-getvideopaletteentries.md)
-   [<span data-ttu-id="ad76d-121">**CBaseControlVideo::GetVideoSize**</span><span class="sxs-lookup"><span data-stu-id="ad76d-121">**CBaseControlVideo::GetVideoSize**</span></span>](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a><span data-ttu-id="ad76d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad76d-122">Requirements</span></span>



| <span data-ttu-id="ad76d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad76d-123">Requirement</span></span> | <span data-ttu-id="ad76d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad76d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad76d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad76d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ad76d-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad76d-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad76d-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad76d-127">Library</span></span><br/> | <dl> <span data-ttu-id="ad76d-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ad76d-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad76d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad76d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad76d-130">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="ad76d-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




