---
description: La méthode GetSourcePosition récupère la position et les dimensions du rectangle source en une seule opération atomique.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: Méthode CBaseControlVideo. GetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2422845a7b5c64bc07b8e8942b2f19cd10a54d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541549"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a><span data-ttu-id="987eb-103">Méthode CBaseControlVideo. GetSourcePosition</span><span class="sxs-lookup"><span data-stu-id="987eb-103">CBaseControlVideo.GetSourcePosition method</span></span>

<span data-ttu-id="987eb-104">La `GetSourcePosition` méthode récupère la position et les dimensions du rectangle source en une seule opération atomique.</span><span class="sxs-lookup"><span data-stu-id="987eb-104">The `GetSourcePosition` method retrieves the position and dimensions of the source rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="987eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="987eb-105">Syntax</span></span>


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="987eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="987eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="987eb-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="987eb-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="987eb-108">Pointeur vers la coordonnée gauche du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="987eb-108">Pointer to the left coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="987eb-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="987eb-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="987eb-110">Pointeur vers la coordonnée supérieure du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="987eb-110">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="987eb-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="987eb-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="987eb-112">Pointeur vers la largeur du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="987eb-112">Pointer to the width of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="987eb-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="987eb-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="987eb-114">Pointeur vers la hauteur du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="987eb-114">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="987eb-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="987eb-115">Return value</span></span>

<span data-ttu-id="987eb-116">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="987eb-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="987eb-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="987eb-117">Return code</span></span>                                                                                           | <span data-ttu-id="987eb-118">Description</span><span class="sxs-lookup"><span data-stu-id="987eb-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="987eb-119"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="987eb-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="987eb-120">Échec.</span><span class="sxs-lookup"><span data-stu-id="987eb-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="987eb-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="987eb-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="987eb-122">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="987eb-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="987eb-123"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="987eb-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="987eb-124">Impossible d’effectuer l’opération, car les broches ne sont pas connectées.</span><span class="sxs-lookup"><span data-stu-id="987eb-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="987eb-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="987eb-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="987eb-126">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="987eb-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="987eb-127">Notes</span><span class="sxs-lookup"><span data-stu-id="987eb-127">Remarks</span></span>

<span data-ttu-id="987eb-128">Une application peut modifier les rectangles source et de destination de la vidéo par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="987eb-128">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="987eb-129">Le rectangle source affecte la section de la source vidéo native qui s’affiche sur l’écran. le rectangle de destination affecte l’emplacement où la vidéo s’affichera lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="987eb-129">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="987eb-130">Le rectangle de destination est relatif à la zone cliente de la fenêtre dans laquelle il est lu.</span><span class="sxs-lookup"><span data-stu-id="987eb-130">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="987eb-131">L’angle supérieur gauche de la fenêtre est coordonnée (0,0).</span><span class="sxs-lookup"><span data-stu-id="987eb-131">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="987eb-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="987eb-132">Requirements</span></span>



| <span data-ttu-id="987eb-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="987eb-133">Requirement</span></span> | <span data-ttu-id="987eb-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="987eb-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="987eb-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="987eb-135">Header</span></span><br/>  | <dl> <span data-ttu-id="987eb-136"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="987eb-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="987eb-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="987eb-137">Library</span></span><br/> | <dl> <span data-ttu-id="987eb-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="987eb-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="987eb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="987eb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987eb-140">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="987eb-140">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




