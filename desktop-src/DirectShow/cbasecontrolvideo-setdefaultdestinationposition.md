---
description: La méthode SetDefaultDestinationPosition rétablit le convertisseur à l’aide de la position de destination par défaut (en général, la zone cliente de la fenêtre entière).
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: Méthode CBaseControlVideo. SetDefaultDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528646"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a><span data-ttu-id="140a4-103">Méthode CBaseControlVideo. SetDefaultDestinationPosition</span><span class="sxs-lookup"><span data-stu-id="140a4-103">CBaseControlVideo.SetDefaultDestinationPosition method</span></span>

<span data-ttu-id="140a4-104">La `SetDefaultDestinationPosition` méthode rétablit le convertisseur à l’aide de la position de destination par défaut (en général, la zone cliente de la fenêtre entière).</span><span class="sxs-lookup"><span data-stu-id="140a4-104">The `SetDefaultDestinationPosition` method sets the renderer back to using the default destination position (typically the entire window client area).</span></span>

## <a name="syntax"></a><span data-ttu-id="140a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="140a4-105">Syntax</span></span>


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a><span data-ttu-id="140a4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="140a4-106">Parameters</span></span>

<span data-ttu-id="140a4-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="140a4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="140a4-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="140a4-108">Return value</span></span>

<span data-ttu-id="140a4-109">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="140a4-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="140a4-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="140a4-110">Return code</span></span>                                                                                           | <span data-ttu-id="140a4-111">Description</span><span class="sxs-lookup"><span data-stu-id="140a4-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="140a4-112"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="140a4-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="140a4-113">Échec.</span><span class="sxs-lookup"><span data-stu-id="140a4-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="140a4-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="140a4-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="140a4-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="140a4-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="140a4-116"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="140a4-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="140a4-117">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="140a4-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="140a4-118">Notes</span><span class="sxs-lookup"><span data-stu-id="140a4-118">Remarks</span></span>

<span data-ttu-id="140a4-119">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="140a4-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="140a4-120">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="140a4-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="140a4-121">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="140a4-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="140a4-122">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="140a4-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="140a4-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="140a4-123">Requirements</span></span>



| <span data-ttu-id="140a4-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="140a4-124">Requirement</span></span> | <span data-ttu-id="140a4-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="140a4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140a4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="140a4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="140a4-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="140a4-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="140a4-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="140a4-128">Library</span></span><br/> | <dl> <span data-ttu-id="140a4-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="140a4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140a4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="140a4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140a4-131">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="140a4-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




