---
description: L’événement InkOverlay. Stroke se produit lorsque l’utilisateur dessine un nouveau trait sur une tablette.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: InkOverlay. Stroke, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408c44cf47ecfbf3ea0cfd0f8306be61efb0f8e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116847"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="72e70-103">InkOverlay. Stroke (événement)</span><span class="sxs-lookup"><span data-stu-id="72e70-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="72e70-104">Se produit lorsque l’utilisateur dessine un nouveau trait sur une tablette.</span><span class="sxs-lookup"><span data-stu-id="72e70-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e70-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72e70-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="72e70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72e70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e70-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72e70-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e70-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="72e70-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="72e70-109">*Trait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72e70-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e70-110">Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) collecté.</span><span class="sxs-lookup"><span data-stu-id="72e70-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="72e70-111">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="72e70-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72e70-112">Spécifie si l’événement doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="72e70-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="72e70-113">Si la **valeur est true**, la collection du trait est annulée.</span><span class="sxs-lookup"><span data-stu-id="72e70-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72e70-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="72e70-114">Return value</span></span>

<span data-ttu-id="72e70-115">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="72e70-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72e70-116">Notes </span><span class="sxs-lookup"><span data-stu-id="72e70-116">Remarks</span></span>

<span data-ttu-id="72e70-117">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="72e70-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="72e70-118">L’événement [**Stroke**](inkcollector-stroke.md) est déclenché en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="72e70-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="72e70-119">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="72e70-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="72e70-120">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="72e70-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="72e70-121">L’événement [**Stroke**](inkcollector-stroke.md) se déclenche lorsque l’utilisateur termine le dessin d’un trait, et non lorsqu’un trait est ajouté à la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="72e70-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="72e70-122">Lorsque l’utilisateur commence par commencer à dessiner un trait, il est immédiatement ajouté à la collection InkStrokes ; Toutefois, l’événement **Stroke** ne se déclenche pas tant que le trait n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="72e70-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="72e70-123">Par conséquent, les traits peuvent exister dans la collection InkStrokes que le gestionnaire d’événements **Stroke** n’a pas vus.</span><span class="sxs-lookup"><span data-stu-id="72e70-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72e70-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72e70-124">Requirements</span></span>



| <span data-ttu-id="72e70-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72e70-125">Requirement</span></span> | <span data-ttu-id="72e70-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="72e70-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e70-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72e70-127">Minimum supported client</span></span><br/> | <span data-ttu-id="72e70-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72e70-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="72e70-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72e70-129">Minimum supported server</span></span><br/> | <span data-ttu-id="72e70-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="72e70-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="72e70-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="72e70-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="72e70-132"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="72e70-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="72e70-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72e70-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="72e70-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72e70-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="72e70-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72e70-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e70-136">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="72e70-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="72e70-137">[**Collection InkStrokes d’événements StrokesAdded \[\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="72e70-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="72e70-138">[**Classe d’événement StrokesDeleted \[ InkOverlay\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="72e70-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="72e70-139">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="72e70-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="72e70-140">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="72e70-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

