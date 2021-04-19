---
description: La \_ méthode obtenir VideoHeight récupère la hauteur de la vidéo native.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Méthode CBaseControlVideo.get_VideoHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542553"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a><span data-ttu-id="17b2c-103">Méthode CBaseControlVideo. obten \_ VideoHeight</span><span class="sxs-lookup"><span data-stu-id="17b2c-103">CBaseControlVideo.get\_VideoHeight method</span></span>

<span data-ttu-id="17b2c-104">La `get_VideoHeight` méthode récupère la hauteur de la vidéo native.</span><span class="sxs-lookup"><span data-stu-id="17b2c-104">The `get_VideoHeight` method retrieves the height of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17b2c-105">Syntax</span></span>


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a><span data-ttu-id="17b2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17b2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b2c-107">*pVideoHeight*</span><span class="sxs-lookup"><span data-stu-id="17b2c-107">*pVideoHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="17b2c-108">Pointeur vers la hauteur de la vidéo native, en pixels.</span><span class="sxs-lookup"><span data-stu-id="17b2c-108">Pointer to the height of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b2c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17b2c-109">Return value</span></span>

<span data-ttu-id="17b2c-110">Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="17b2c-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="17b2c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="17b2c-111">Remarks</span></span>

<span data-ttu-id="17b2c-112">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) .</span><span class="sxs-lookup"><span data-stu-id="17b2c-112">This member function implements the [**IBasicVideo::get\_VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) method.</span></span> <span data-ttu-id="17b2c-113">Elle appelle la CBaseControlVideo virtuelle pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="17b2c-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b2c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17b2c-114">Requirements</span></span>



| <span data-ttu-id="17b2c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17b2c-115">Requirement</span></span> | <span data-ttu-id="17b2c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="17b2c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b2c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="17b2c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="17b2c-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17b2c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17b2c-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17b2c-119">Library</span></span><br/> | <dl> <span data-ttu-id="17b2c-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="17b2c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b2c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17b2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b2c-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="17b2c-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




