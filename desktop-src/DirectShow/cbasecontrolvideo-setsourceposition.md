---
description: La méthode SetSourcePosition définit une nouvelle position source pour la vidéo.
ms.assetid: e3c9ce31-9c24-4ef5-9526-ef6b890f5109
title: Méthode CBaseControlVideo. SetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5493779b623108f713f8da252e8696140883395b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537900"
---
# <a name="cbasecontrolvideosetsourceposition-method"></a><span data-ttu-id="2d831-103">Méthode CBaseControlVideo. SetSourcePosition</span><span class="sxs-lookup"><span data-stu-id="2d831-103">CBaseControlVideo.SetSourcePosition method</span></span>

<span data-ttu-id="2d831-104">La `SetSourcePosition` méthode définit une nouvelle position source pour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="2d831-104">The `SetSourcePosition` method sets a new source position for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d831-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d831-105">Syntax</span></span>


```C++
HRESULT SetSourcePosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="2d831-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d831-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="2d831-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="2d831-108">Nouvelle coordonnée gauche.</span><span class="sxs-lookup"><span data-stu-id="2d831-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="2d831-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="2d831-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="2d831-110">Nouvelle coordonnée supérieure.</span><span class="sxs-lookup"><span data-stu-id="2d831-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="2d831-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="2d831-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="2d831-112">Nouvelle largeur.</span><span class="sxs-lookup"><span data-stu-id="2d831-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="2d831-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="2d831-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="2d831-114">Nouvelle hauteur.</span><span class="sxs-lookup"><span data-stu-id="2d831-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d831-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d831-115">Return value</span></span>

<span data-ttu-id="2d831-116">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="2d831-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="2d831-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2d831-117">Return code</span></span>                                                                                           | <span data-ttu-id="2d831-118">Description</span><span class="sxs-lookup"><span data-stu-id="2d831-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d831-119"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="2d831-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="2d831-120">Échec.</span><span class="sxs-lookup"><span data-stu-id="2d831-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="2d831-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2d831-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="2d831-122">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="2d831-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="2d831-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="2d831-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="2d831-124">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="2d831-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2d831-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="2d831-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="2d831-126">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2d831-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="2d831-127"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="2d831-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2d831-128">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="2d831-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d831-129">Notes</span><span class="sxs-lookup"><span data-stu-id="2d831-129">Remarks</span></span>

<span data-ttu-id="2d831-130">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="2d831-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="2d831-131">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="2d831-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="2d831-132">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="2d831-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="2d831-133">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="2d831-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d831-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d831-134">Requirements</span></span>



| <span data-ttu-id="2d831-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d831-135">Requirement</span></span> | <span data-ttu-id="2d831-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d831-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d831-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d831-137">Header</span></span><br/>  | <dl> <span data-ttu-id="2d831-138"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d831-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d831-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d831-139">Library</span></span><br/> | <dl> <span data-ttu-id="2d831-140"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2d831-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d831-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d831-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d831-142">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="2d831-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




