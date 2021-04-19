---
description: La \_ méthode obtenir DestinationTop récupère la coordonnée supérieure du rectangle de destination actuel.
ms.assetid: 8d5c1361-18db-4ea1-a507-781397189630
title: Méthode CBaseControlVideo.get_DestinationTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2c7d450c50b11186546a25ceebd317a308dd805
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530512"
---
# <a name="cbasecontrolvideoget_destinationtop-method"></a><span data-ttu-id="ab2de-103">Méthode CBaseControlVideo. obten \_ DestinationTop</span><span class="sxs-lookup"><span data-stu-id="ab2de-103">CBaseControlVideo.get\_DestinationTop method</span></span>

<span data-ttu-id="ab2de-104">La `get_DestinationTop` méthode récupère la coordonnée supérieure du rectangle de destination actuel.</span><span class="sxs-lookup"><span data-stu-id="ab2de-104">The `get_DestinationTop` method retrieves the top coordinate of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab2de-105">Syntax</span></span>


```C++
HRESULT get_DestinationTop(
   long *pDestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="ab2de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab2de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab2de-107">*pDestinationTop*</span><span class="sxs-lookup"><span data-stu-id="ab2de-107">*pDestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="ab2de-108">Pointeur vers la coordonnée supérieure du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ab2de-108">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab2de-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab2de-109">Return value</span></span>

<span data-ttu-id="ab2de-110">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="ab2de-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="ab2de-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ab2de-111">Return code</span></span>                                                                                           | <span data-ttu-id="ab2de-112">Description</span><span class="sxs-lookup"><span data-stu-id="ab2de-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab2de-113"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2de-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="ab2de-114">Échec.</span><span class="sxs-lookup"><span data-stu-id="ab2de-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="ab2de-115"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2de-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="ab2de-116">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="ab2de-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="ab2de-117"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2de-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ab2de-118">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="ab2de-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="ab2de-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2de-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="ab2de-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ab2de-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="ab2de-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ab2de-121">Remarks</span></span>

<span data-ttu-id="ab2de-122">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ DestinationTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) .</span><span class="sxs-lookup"><span data-stu-id="ab2de-122">This member function implements the [**IBasicVideo::get\_DestinationTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationtop) method.</span></span>

<span data-ttu-id="ab2de-123">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="ab2de-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="ab2de-124">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ab2de-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="ab2de-125">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="ab2de-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="ab2de-126">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="ab2de-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2de-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab2de-127">Requirements</span></span>



| <span data-ttu-id="ab2de-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab2de-128">Requirement</span></span> | <span data-ttu-id="ab2de-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab2de-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2de-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab2de-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ab2de-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab2de-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab2de-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab2de-132">Library</span></span><br/> | <dl> <span data-ttu-id="ab2de-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab2de-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab2de-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab2de-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2de-135">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="ab2de-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




