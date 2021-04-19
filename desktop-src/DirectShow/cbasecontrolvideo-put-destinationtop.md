---
description: La \_ méthode put DestinationTop définit la coordonnée supérieure du rectangle de destination.
ms.assetid: d18996ac-85f2-4778-b0aa-1bc0c4d5f7d9
title: Méthode CBaseControlVideo.put_DestinationTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c89e4693d424412a43869509e046a5023e76341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526744"
---
# <a name="cbasecontrolvideoput_destinationtop-method"></a><span data-ttu-id="b3f16-103">CBaseControlVideo. put \_ DestinationTop, méthode</span><span class="sxs-lookup"><span data-stu-id="b3f16-103">CBaseControlVideo.put\_DestinationTop method</span></span>

<span data-ttu-id="b3f16-104">La `put_DestinationTop` méthode définit la coordonnée supérieure du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="b3f16-104">The `put_DestinationTop` method sets the top coordinate of the destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f16-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3f16-105">Syntax</span></span>


```C++
HRESULT put_DestinationTop(
   long DestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="b3f16-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f16-107">*DestinationTop*</span><span class="sxs-lookup"><span data-stu-id="b3f16-107">*DestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="b3f16-108">Nouvelle coordonnée supérieure du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="b3f16-108">New top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f16-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3f16-109">Return value</span></span>

<span data-ttu-id="b3f16-110">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="b3f16-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="b3f16-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b3f16-111">Return code</span></span>                                                                                           | <span data-ttu-id="b3f16-112">Description</span><span class="sxs-lookup"><span data-stu-id="b3f16-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3f16-113"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f16-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="b3f16-114">Échec.</span><span class="sxs-lookup"><span data-stu-id="b3f16-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b3f16-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f16-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="b3f16-116">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="b3f16-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="b3f16-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f16-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="b3f16-118">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="b3f16-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b3f16-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f16-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="b3f16-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b3f16-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b3f16-121"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f16-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b3f16-122">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="b3f16-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3f16-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b3f16-123">Remarks</span></span>

<span data-ttu-id="b3f16-124">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="b3f16-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="b3f16-125">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="b3f16-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="b3f16-126">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="b3f16-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="b3f16-127">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="b3f16-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f16-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3f16-128">Requirements</span></span>



| <span data-ttu-id="b3f16-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3f16-129">Requirement</span></span> | <span data-ttu-id="b3f16-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3f16-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f16-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3f16-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b3f16-132"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3f16-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b3f16-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3f16-133">Library</span></span><br/> | <dl> <span data-ttu-id="b3f16-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b3f16-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3f16-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3f16-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f16-136">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="b3f16-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




