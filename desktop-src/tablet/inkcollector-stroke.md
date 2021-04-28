---
description: Événement InkCollector. Stroke-se produit lorsque l’utilisateur dessine un nouveau trait sur une tablette.
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: Événement InkCollector. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49cb90b02ab3fca60a8fa17089b6a76f959a60e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110053"
---
# <a name="inkcollectorstroke-event"></a><span data-ttu-id="1478d-103">InkCollector. Stroke (événement)</span><span class="sxs-lookup"><span data-stu-id="1478d-103">InkCollector.Stroke event</span></span>

<span data-ttu-id="1478d-104">Se produit lorsque l’utilisateur dessine un nouveau trait sur une tablette.</span><span class="sxs-lookup"><span data-stu-id="1478d-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="1478d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1478d-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="1478d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1478d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1478d-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1478d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1478d-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="1478d-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="1478d-109">*Trait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1478d-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1478d-110">Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) collecté.</span><span class="sxs-lookup"><span data-stu-id="1478d-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="1478d-111">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1478d-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1478d-112">**Variante \_ TRUE** pour annuler l’événement ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="1478d-112">**VARIANT\_TRUE** to cancel the event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1478d-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1478d-113">Return value</span></span>

<span data-ttu-id="1478d-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1478d-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1478d-115">Notes </span><span class="sxs-lookup"><span data-stu-id="1478d-115">Remarks</span></span>

<span data-ttu-id="1478d-116">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="1478d-116">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="1478d-117">L’événement **Stroke** est déclenché en mode SELECT ou Erase, pas uniquement lors de l’insertion d’une entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="1478d-117">The **Stroke** event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="1478d-118">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="1478d-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="1478d-119">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="1478d-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="1478d-120">L’événement **Stroke** se déclenche lorsque l’utilisateur termine le dessin d’un trait, et non lorsqu’un trait est ajouté à la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1478d-120">The **Stroke** event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="1478d-121">Lorsque l’utilisateur commence par commencer à dessiner un trait, il est immédiatement ajouté à la collection InkStrokes ; Toutefois, l’événement **Stroke** ne se déclenche pas tant que le trait n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="1478d-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="1478d-122">Par conséquent, les traits peuvent exister dans la collection InkStrokes que le gestionnaire d’événements **Stroke** n’a pas vus.</span><span class="sxs-lookup"><span data-stu-id="1478d-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1478d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1478d-123">Requirements</span></span>



| <span data-ttu-id="1478d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1478d-124">Requirement</span></span> | <span data-ttu-id="1478d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1478d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1478d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1478d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1478d-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1478d-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1478d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1478d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1478d-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1478d-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1478d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="1478d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1478d-131"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1478d-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1478d-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1478d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="1478d-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1478d-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1478d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1478d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1478d-135">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="1478d-135">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

<span data-ttu-id="1478d-136">[**Collection InkStrokes d’événements StrokesAdded \[\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="1478d-136">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="1478d-137">[**Classe d’événement StrokesDeleted \[ InkOverlay\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="1478d-137">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="1478d-138">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="1478d-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="1478d-139">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="1478d-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

