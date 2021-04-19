---
description: La \_ méthode obtenir sourceTop récupère la coordonnée supérieure du rectangle source actuel.
ms.assetid: 78dbd1e6-f591-487e-b9fe-fcbda55f5338
title: Méthode CBaseControlVideo.get_SourceTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1c2a2a90b441571a23bfa4210002b352e388a98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530511"
---
# <a name="cbasecontrolvideoget_sourcetop-method"></a><span data-ttu-id="8f905-103">Méthode CBaseControlVideo. obten \_ sourceTop</span><span class="sxs-lookup"><span data-stu-id="8f905-103">CBaseControlVideo.get\_SourceTop method</span></span>

<span data-ttu-id="8f905-104">La `get_SourceTop` méthode récupère la coordonnée supérieure du rectangle source actuel.</span><span class="sxs-lookup"><span data-stu-id="8f905-104">The `get_SourceTop` method retrieves the top coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f905-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f905-105">Syntax</span></span>


```C++
HRESULT get_SourceTop(
   long *pSourceTop
);
```



## <a name="parameters"></a><span data-ttu-id="8f905-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f905-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f905-107">*pSourceTop*</span><span class="sxs-lookup"><span data-stu-id="8f905-107">*pSourceTop*</span></span> 
</dt> <dd>

<span data-ttu-id="8f905-108">Pointeur vers la coordonnée supérieure du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="8f905-108">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f905-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f905-109">Return value</span></span>

<span data-ttu-id="8f905-110">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="8f905-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="8f905-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8f905-111">Return code</span></span>                                                                                           | <span data-ttu-id="8f905-112">Description</span><span class="sxs-lookup"><span data-stu-id="8f905-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f905-113"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8f905-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="8f905-114">Échec.</span><span class="sxs-lookup"><span data-stu-id="8f905-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="8f905-115"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f905-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="8f905-116">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="8f905-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="8f905-117"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="8f905-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8f905-118">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="8f905-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="8f905-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="8f905-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="8f905-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="8f905-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="8f905-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8f905-121">Remarks</span></span>

<span data-ttu-id="8f905-122">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ sourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) .</span><span class="sxs-lookup"><span data-stu-id="8f905-122">This member function implements the [**IBasicVideo::get\_SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) method.</span></span>

<span data-ttu-id="8f905-123">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="8f905-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="8f905-124">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="8f905-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="8f905-125">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="8f905-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="8f905-126">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="8f905-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f905-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f905-127">Requirements</span></span>



| <span data-ttu-id="8f905-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f905-128">Requirement</span></span> | <span data-ttu-id="8f905-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f905-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f905-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f905-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8f905-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f905-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8f905-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8f905-132">Library</span></span><br/> | <dl> <span data-ttu-id="8f905-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8f905-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f905-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f905-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f905-135">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="8f905-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




