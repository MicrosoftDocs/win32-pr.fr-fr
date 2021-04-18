---
description: La méthode GetDestinationPosition récupère le rectangle de destination dans une opération atomique.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Méthode CBaseControlVideo. GetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526901"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a><span data-ttu-id="ef2d0-103">Méthode CBaseControlVideo. GetDestinationPosition</span><span class="sxs-lookup"><span data-stu-id="ef2d0-103">CBaseControlVideo.GetDestinationPosition method</span></span>

<span data-ttu-id="ef2d0-104">La `GetDestinationPosition` méthode récupère le rectangle de destination dans une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-104">The `GetDestinationPosition` method retrieves the destination rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef2d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef2d0-105">Syntax</span></span>


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="ef2d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef2d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef2d0-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="ef2d0-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="ef2d0-108">Pointeur vers la coordonnée gauche du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ef2d0-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="ef2d0-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="ef2d0-110">Pointeur vers la coordonnée supérieure du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-110">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ef2d0-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="ef2d0-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="ef2d0-112">Pointeur vers la largeur du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-112">Pointer to the width of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ef2d0-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="ef2d0-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="ef2d0-114">Pointeur vers la hauteur du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-114">Pointer to the height of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef2d0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef2d0-115">Return value</span></span>

<span data-ttu-id="ef2d0-116">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="ef2d0-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef2d0-117">Return code</span></span>                                                                                           | <span data-ttu-id="ef2d0-118">Description</span><span class="sxs-lookup"><span data-stu-id="ef2d0-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef2d0-119"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="ef2d0-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="ef2d0-120">Échec.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="ef2d0-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ef2d0-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="ef2d0-122">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="ef2d0-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="ef2d0-123"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="ef2d0-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ef2d0-124">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="ef2d0-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="ef2d0-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="ef2d0-126">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="ef2d0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="ef2d0-127">Remarks</span></span>

<span data-ttu-id="ef2d0-128">Cette fonction membre peut être utilisée à la place d’appels séparés aux fonctions membres [**CBaseControlVideo :: obten \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo :: obten \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo :: obten \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)et [**CBaseControlVideo :: obtient \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) .</span><span class="sxs-lookup"><span data-stu-id="ef2d0-128">This member function can be used in place of separate calls to the [**CBaseControlVideo::get\_DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get\_DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get\_DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md), and [**CBaseControlVideo::get\_DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) member functions.</span></span> <span data-ttu-id="ef2d0-129">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="ef2d0-129">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="ef2d0-130">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-130">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="ef2d0-131">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="ef2d0-131">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="ef2d0-132">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="ef2d0-132">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2d0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef2d0-133">Requirements</span></span>



| <span data-ttu-id="ef2d0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef2d0-134">Requirement</span></span> | <span data-ttu-id="ef2d0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef2d0-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2d0-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef2d0-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ef2d0-137"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef2d0-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef2d0-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef2d0-138">Library</span></span><br/> | <dl> <span data-ttu-id="ef2d0-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ef2d0-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef2d0-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef2d0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2d0-141">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="ef2d0-141">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




