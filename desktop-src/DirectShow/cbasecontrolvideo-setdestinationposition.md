---
description: La méthode SetDestinationPosition définit le rectangle de destination de la vidéo.
ms.assetid: 397e90ea-7535-4cac-9f47-7a93737b1e3a
title: Méthode CBaseControlVideo. SetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798a65c44dd490587e3ad46fcae2c61a03986df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526892"
---
# <a name="cbasecontrolvideosetdestinationposition-method"></a><span data-ttu-id="f8c98-103">Méthode CBaseControlVideo. SetDestinationPosition</span><span class="sxs-lookup"><span data-stu-id="f8c98-103">CBaseControlVideo.SetDestinationPosition method</span></span>

<span data-ttu-id="f8c98-104">La `SetDestinationPosition` méthode définit le rectangle de destination de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="f8c98-104">The `SetDestinationPosition` method sets the destination rectangle for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8c98-105">Syntax</span></span>


```C++
HRESULT SetDestinationPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="f8c98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8c98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c98-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="f8c98-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c98-108">Nouvelle coordonnée gauche.</span><span class="sxs-lookup"><span data-stu-id="f8c98-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="f8c98-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="f8c98-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c98-110">Nouvelle coordonnée supérieure.</span><span class="sxs-lookup"><span data-stu-id="f8c98-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="f8c98-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="f8c98-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c98-112">Nouvelle largeur.</span><span class="sxs-lookup"><span data-stu-id="f8c98-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="f8c98-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="f8c98-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c98-114">Nouvelle hauteur.</span><span class="sxs-lookup"><span data-stu-id="f8c98-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c98-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8c98-115">Return value</span></span>

<span data-ttu-id="f8c98-116">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="f8c98-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="f8c98-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f8c98-117">Return code</span></span>                                                                                           | <span data-ttu-id="f8c98-118">Description</span><span class="sxs-lookup"><span data-stu-id="f8c98-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8c98-119"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="f8c98-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="f8c98-120">Échec.</span><span class="sxs-lookup"><span data-stu-id="f8c98-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="f8c98-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f8c98-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="f8c98-122">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="f8c98-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="f8c98-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="f8c98-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="f8c98-124">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f8c98-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="f8c98-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="f8c98-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="f8c98-126">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f8c98-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="f8c98-127"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="f8c98-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="f8c98-128">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="f8c98-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8c98-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f8c98-129">Remarks</span></span>

<span data-ttu-id="f8c98-130">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="f8c98-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="f8c98-131">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="f8c98-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="f8c98-132">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="f8c98-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="f8c98-133">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="f8c98-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c98-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8c98-134">Requirements</span></span>



| <span data-ttu-id="f8c98-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8c98-135">Requirement</span></span> | <span data-ttu-id="f8c98-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8c98-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c98-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8c98-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f8c98-138"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8c98-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f8c98-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8c98-139">Library</span></span><br/> | <dl> <span data-ttu-id="f8c98-140"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f8c98-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8c98-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c98-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c98-142">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="f8c98-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




