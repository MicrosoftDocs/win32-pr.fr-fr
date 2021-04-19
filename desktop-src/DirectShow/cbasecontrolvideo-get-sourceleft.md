---
description: La \_ méthode obtenir SourceLeft récupère la coordonnée gauche du rectangle source actuel.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: Méthode CBaseControlVideo.get_SourceLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544437"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a><span data-ttu-id="84663-103">Méthode CBaseControlVideo. obten \_ SourceLeft</span><span class="sxs-lookup"><span data-stu-id="84663-103">CBaseControlVideo.get\_SourceLeft method</span></span>

<span data-ttu-id="84663-104">La `get_SourceLeft` méthode récupère la coordonnée gauche du rectangle source actuel.</span><span class="sxs-lookup"><span data-stu-id="84663-104">The `get_SourceLeft` method retrieves the left coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="84663-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84663-105">Syntax</span></span>


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="84663-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84663-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84663-107">*pSourceLeft*</span><span class="sxs-lookup"><span data-stu-id="84663-107">*pSourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="84663-108">Pointeur vers la coordonnée gauche du rectangle source actuel.</span><span class="sxs-lookup"><span data-stu-id="84663-108">Pointer to the left coordinate of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84663-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84663-109">Return value</span></span>

<span data-ttu-id="84663-110">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="84663-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="84663-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="84663-111">Return code</span></span>                                                                                           | <span data-ttu-id="84663-112">Description</span><span class="sxs-lookup"><span data-stu-id="84663-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84663-113"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="84663-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="84663-114">Échec.</span><span class="sxs-lookup"><span data-stu-id="84663-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="84663-115"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="84663-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="84663-116">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="84663-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="84663-117"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="84663-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="84663-118">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="84663-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="84663-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="84663-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="84663-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="84663-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="84663-121">Notes</span><span class="sxs-lookup"><span data-stu-id="84663-121">Remarks</span></span>

<span data-ttu-id="84663-122">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="84663-122">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="84663-123">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="84663-123">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="84663-124">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="84663-124">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="84663-125">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="84663-125">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="84663-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84663-126">Requirements</span></span>



| <span data-ttu-id="84663-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84663-127">Requirement</span></span> | <span data-ttu-id="84663-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="84663-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84663-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="84663-129">Header</span></span><br/>  | <dl> <span data-ttu-id="84663-130"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84663-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="84663-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84663-131">Library</span></span><br/> | <dl> <span data-ttu-id="84663-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="84663-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84663-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84663-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84663-134">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="84663-134">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




