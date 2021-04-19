---
description: La \_ méthode put DestinationLeft définit la coordonnée gauche du rectangle de destination.
ms.assetid: 5d61d41c-3935-4637-b092-f508ea0508d3
title: Méthode CBaseControlVideo.put_DestinationLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c2421250e638ad05c545978ca7649285b01836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532653"
---
# <a name="cbasecontrolvideoput_destinationleft-method"></a><span data-ttu-id="81beb-103">CBaseControlVideo. put \_ DestinationLeft, méthode</span><span class="sxs-lookup"><span data-stu-id="81beb-103">CBaseControlVideo.put\_DestinationLeft method</span></span>

<span data-ttu-id="81beb-104">La `put_DestinationLeft` méthode définit la coordonnée gauche du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="81beb-104">The `put_DestinationLeft` method sets the left coordinate of the destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="81beb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81beb-105">Syntax</span></span>


```C++
HRESULT put_DestinationLeft(
   long DestinationLeft
);
```



## <a name="parameters"></a><span data-ttu-id="81beb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81beb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81beb-107">*DestinationLeft*</span><span class="sxs-lookup"><span data-stu-id="81beb-107">*DestinationLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="81beb-108">Nouvelle coordonnée gauche du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="81beb-108">New left coordinate of destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81beb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81beb-109">Return value</span></span>

<span data-ttu-id="81beb-110">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="81beb-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="81beb-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="81beb-111">Return code</span></span>                                                                                           | <span data-ttu-id="81beb-112">Description</span><span class="sxs-lookup"><span data-stu-id="81beb-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81beb-113"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="81beb-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="81beb-114">Échec.</span><span class="sxs-lookup"><span data-stu-id="81beb-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="81beb-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="81beb-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="81beb-116">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="81beb-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="81beb-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="81beb-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="81beb-118">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="81beb-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="81beb-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="81beb-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="81beb-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="81beb-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="81beb-121"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="81beb-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="81beb-122">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="81beb-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81beb-123">Notes</span><span class="sxs-lookup"><span data-stu-id="81beb-123">Remarks</span></span>

<span data-ttu-id="81beb-124">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="81beb-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="81beb-125">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="81beb-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="81beb-126">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="81beb-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="81beb-127">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="81beb-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="81beb-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81beb-128">Requirements</span></span>



| <span data-ttu-id="81beb-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81beb-129">Requirement</span></span> | <span data-ttu-id="81beb-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="81beb-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81beb-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="81beb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="81beb-132"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81beb-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81beb-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81beb-133">Library</span></span><br/> | <dl> <span data-ttu-id="81beb-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="81beb-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81beb-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81beb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81beb-136">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="81beb-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




