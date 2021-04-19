---
description: La \_ méthode obtenir DestinationLeft récupère la coordonnée gauche du rectangle de destination actuel.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: Méthode CBaseControlVideo.get_DestinationLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f433d880fd7f568a173a91c533e0d07bf97e6443
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523593"
---
# <a name="cbasecontrolvideoget_destinationleft-method"></a><span data-ttu-id="5ca32-103">Méthode CBaseControlVideo. obten \_ DestinationLeft</span><span class="sxs-lookup"><span data-stu-id="5ca32-103">CBaseControlVideo.get\_DestinationLeft method</span></span>

<span data-ttu-id="5ca32-104">La `get_DestinationLeft` méthode récupère la coordonnée gauche du rectangle de destination actuel.</span><span class="sxs-lookup"><span data-stu-id="5ca32-104">The `get_DestinationLeft` method retrieves the left coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ca32-105">Syntax</span></span>


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## <a name="parameters"></a><span data-ttu-id="5ca32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ca32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca32-107">*pDestinationLeft*</span><span class="sxs-lookup"><span data-stu-id="5ca32-107">*pDestinationLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="5ca32-108">Pointeur vers la coordonnée gauche du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="5ca32-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca32-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ca32-109">Return value</span></span>

<span data-ttu-id="5ca32-110">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="5ca32-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="5ca32-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5ca32-111">Return code</span></span>                                                                                           | <span data-ttu-id="5ca32-112">Description</span><span class="sxs-lookup"><span data-stu-id="5ca32-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ca32-113"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="5ca32-114">Échec.</span><span class="sxs-lookup"><span data-stu-id="5ca32-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="5ca32-115"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5ca32-116">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="5ca32-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5ca32-117"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5ca32-118">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="5ca32-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="5ca32-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="5ca32-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="5ca32-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="5ca32-121">Notes</span><span class="sxs-lookup"><span data-stu-id="5ca32-121">Remarks</span></span>

<span data-ttu-id="5ca32-122">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) .</span><span class="sxs-lookup"><span data-stu-id="5ca32-122">This member function implements the [**IBasicVideo::get\_DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) method.</span></span>

<span data-ttu-id="5ca32-123">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="5ca32-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="5ca32-124">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="5ca32-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="5ca32-125">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="5ca32-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="5ca32-126">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="5ca32-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca32-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ca32-127">Requirements</span></span>



| <span data-ttu-id="5ca32-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ca32-128">Requirement</span></span> | <span data-ttu-id="5ca32-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ca32-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca32-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ca32-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5ca32-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ca32-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ca32-132">Library</span></span><br/> | <dl> <span data-ttu-id="5ca32-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5ca32-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca32-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ca32-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca32-135">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="5ca32-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




