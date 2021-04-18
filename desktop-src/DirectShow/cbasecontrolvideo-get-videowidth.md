---
description: La \_ méthode obtenir VideoWidth récupère la largeur de la vidéo native.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Méthode CBaseControlVideo.get_VideoWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533500"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a><span data-ttu-id="9b770-103">Méthode CBaseControlVideo. obten \_ VideoWidth</span><span class="sxs-lookup"><span data-stu-id="9b770-103">CBaseControlVideo.get\_VideoWidth method</span></span>

<span data-ttu-id="9b770-104">La `get_VideoWidth` méthode récupère la largeur de la vidéo native.</span><span class="sxs-lookup"><span data-stu-id="9b770-104">The `get_VideoWidth` method retrieves the width of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b770-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b770-105">Syntax</span></span>


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a><span data-ttu-id="9b770-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b770-107">*pVideoWidth*</span><span class="sxs-lookup"><span data-stu-id="9b770-107">*pVideoWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="9b770-108">Pointeur vers la largeur de la vidéo native, en pixels.</span><span class="sxs-lookup"><span data-stu-id="9b770-108">Pointer to the width of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b770-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b770-109">Return value</span></span>

<span data-ttu-id="9b770-110">Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="9b770-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b770-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9b770-111">Remarks</span></span>

<span data-ttu-id="9b770-112">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) .</span><span class="sxs-lookup"><span data-stu-id="9b770-112">This member function implements the [**IBasicVideo::get\_VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) method.</span></span> <span data-ttu-id="9b770-113">Elle appelle la CBaseControlVideo virtuelle pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="9b770-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b770-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b770-114">Requirements</span></span>



| <span data-ttu-id="9b770-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b770-115">Requirement</span></span> | <span data-ttu-id="9b770-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b770-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b770-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b770-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9b770-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b770-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b770-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9b770-119">Library</span></span><br/> | <dl> <span data-ttu-id="9b770-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9b770-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b770-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b770-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b770-122">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="9b770-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




