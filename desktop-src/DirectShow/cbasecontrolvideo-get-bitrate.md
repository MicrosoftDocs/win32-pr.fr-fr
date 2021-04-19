---
description: La méthode obtenir le \_ débit binaire récupère une vitesse de transmission approximative pour la vidéo.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Méthode CBaseControlVideo.get_BitRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539645"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a><span data-ttu-id="d47bc-103">CBaseControlVideo. obtient la \_ méthode de débit binaire</span><span class="sxs-lookup"><span data-stu-id="d47bc-103">CBaseControlVideo.get\_BitRate method</span></span>

<span data-ttu-id="d47bc-104">La `get_BitRate` méthode récupère une vitesse de transmission approximative de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d47bc-104">The `get_BitRate` method retrieves an approximate bit rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d47bc-105">Syntax</span></span>


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a><span data-ttu-id="d47bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d47bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47bc-107">*pBitRate*</span><span class="sxs-lookup"><span data-stu-id="d47bc-107">*pBitRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d47bc-108">Pointeur vers la vitesse de transmission, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="d47bc-108">Pointer to the bit rate, in bits per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47bc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d47bc-109">Return value</span></span>

<span data-ttu-id="d47bc-110">Retourne une erreur en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d47bc-110">Returns NOERROR if successful or E\_OUTOFMEMORY if not enough memory is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="d47bc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d47bc-111">Remarks</span></span>

<span data-ttu-id="d47bc-112">Cette fonction membre implémente la méthode [**IBasicVideo :: obtient le \_ débit binaire**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) .</span><span class="sxs-lookup"><span data-stu-id="d47bc-112">This member function implements the [**IBasicVideo::get\_BitRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) method.</span></span> <span data-ttu-id="d47bc-113">Elle appelle la CBaseControlVideo virtuelle pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="d47bc-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47bc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d47bc-114">Requirements</span></span>



| <span data-ttu-id="d47bc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d47bc-115">Requirement</span></span> | <span data-ttu-id="d47bc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d47bc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47bc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d47bc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d47bc-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d47bc-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d47bc-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d47bc-119">Library</span></span><br/> | <dl> <span data-ttu-id="d47bc-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d47bc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47bc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d47bc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47bc-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="d47bc-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




