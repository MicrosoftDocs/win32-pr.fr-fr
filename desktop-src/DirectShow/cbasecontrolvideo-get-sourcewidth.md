---
description: La \_ méthode obtenir SourceWidth récupère la largeur du rectangle source actuel.
ms.assetid: e8e27f8f-57e5-489c-aae7-86493677b380
title: Méthode CBaseControlVideo.get_SourceWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60a78fe647ebf488a47907c058962f13790f2538
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526066"
---
# <a name="cbasecontrolvideoget_sourcewidth-method"></a><span data-ttu-id="21dd4-103">Méthode CBaseControlVideo. obten \_ SourceWidth</span><span class="sxs-lookup"><span data-stu-id="21dd4-103">CBaseControlVideo.get\_SourceWidth method</span></span>

<span data-ttu-id="21dd4-104">La `get_SourceWidth` méthode récupère la largeur du rectangle source actuel.</span><span class="sxs-lookup"><span data-stu-id="21dd4-104">The `get_SourceWidth` method retrieves the width of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="21dd4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21dd4-105">Syntax</span></span>


```C++
HRESULT get_SourceWidth(
   long *pSourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="21dd4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21dd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21dd4-107">*pSourceWidth*</span><span class="sxs-lookup"><span data-stu-id="21dd4-107">*pSourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="21dd4-108">Pointeur vers la largeur du rectangle source actuel.</span><span class="sxs-lookup"><span data-stu-id="21dd4-108">Pointer to the width of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21dd4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21dd4-109">Return value</span></span>

<span data-ttu-id="21dd4-110">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="21dd4-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="21dd4-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="21dd4-111">Return code</span></span>                                                                                           | <span data-ttu-id="21dd4-112">Description</span><span class="sxs-lookup"><span data-stu-id="21dd4-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21dd4-113"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="21dd4-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="21dd4-114">Échec.</span><span class="sxs-lookup"><span data-stu-id="21dd4-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="21dd4-115"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="21dd4-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="21dd4-116">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="21dd4-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="21dd4-117"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="21dd4-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="21dd4-118">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="21dd4-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="21dd4-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="21dd4-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="21dd4-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="21dd4-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="21dd4-121">Notes</span><span class="sxs-lookup"><span data-stu-id="21dd4-121">Remarks</span></span>

<span data-ttu-id="21dd4-122">Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) .</span><span class="sxs-lookup"><span data-stu-id="21dd4-122">This member function implements the [**IBasicVideo::get\_SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) method.</span></span>

<span data-ttu-id="21dd4-123">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="21dd4-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="21dd4-124">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="21dd4-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="21dd4-125">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="21dd4-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="21dd4-126">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="21dd4-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="21dd4-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21dd4-127">Requirements</span></span>



| <span data-ttu-id="21dd4-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21dd4-128">Requirement</span></span> | <span data-ttu-id="21dd4-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="21dd4-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21dd4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="21dd4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="21dd4-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21dd4-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21dd4-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="21dd4-132">Library</span></span><br/> | <dl> <span data-ttu-id="21dd4-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="21dd4-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21dd4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21dd4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21dd4-135">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="21dd4-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




