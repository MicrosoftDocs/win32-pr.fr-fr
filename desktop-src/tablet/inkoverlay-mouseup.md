---
description: L’événement InkOverlay. MouseUp se produit lorsque le pointeur de la souris se trouve sur l’objet InkCollector ou InkOverlay et qu’un bouton de la souris est relâché.
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: InkOverlay. MouseUp, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402083aa677b134ea469980227a482ac5546da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086807"
---
# <a name="inkoverlaymouseup-event"></a><span data-ttu-id="fde6f-103">InkOverlay. MouseUp, événement</span><span class="sxs-lookup"><span data-stu-id="fde6f-103">InkOverlay.MouseUp event</span></span>

<span data-ttu-id="fde6f-104">Se produit lorsque le pointeur de la souris se trouve sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) et qu’un bouton de la souris est relâché.</span><span class="sxs-lookup"><span data-stu-id="fde6f-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde6f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fde6f-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="fde6f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fde6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde6f-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fde6f-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde6f-108">Bouton de la souris qui a été relâché.</span><span class="sxs-lookup"><span data-stu-id="fde6f-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="fde6f-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fde6f-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde6f-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="fde6f-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="fde6f-111">*PX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fde6f-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde6f-112">Coordonnée x, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="fde6f-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fde6f-113">*py* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fde6f-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde6f-114">Coordonnée y, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="fde6f-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fde6f-115">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fde6f-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fde6f-116">Indique si l’événement doit être annulé pour le contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="fde6f-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="fde6f-117">La valeur par défaut est **false**, ce qui spécifie que l’événement ne doit pas être annulé.</span><span class="sxs-lookup"><span data-stu-id="fde6f-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde6f-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fde6f-118">Return value</span></span>

<span data-ttu-id="fde6f-119">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fde6f-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde6f-120">Notes </span><span class="sxs-lookup"><span data-stu-id="fde6f-120">Remarks</span></span>

<span data-ttu-id="fde6f-121">Pour améliorer les performances de l’encre en temps réel, masquez ou affichez le curseur de la souris dans les gestionnaires d’événements [**MouseDown**](inkcollector-mousedown.md) et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="fde6f-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="fde6f-122">Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="fde6f-122">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="fde6f-123">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.</span><span class="sxs-lookup"><span data-stu-id="fde6f-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="fde6f-124">Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="fde6f-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="fde6f-125">L’annulation de certains de ces événements peut avoir des résultats imprévus.</span><span class="sxs-lookup"><span data-stu-id="fde6f-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="fde6f-126">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseUp.</span><span class="sxs-lookup"><span data-stu-id="fde6f-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde6f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fde6f-127">Requirements</span></span>



| <span data-ttu-id="fde6f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fde6f-128">Requirement</span></span> | <span data-ttu-id="fde6f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fde6f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde6f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fde6f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fde6f-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fde6f-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fde6f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fde6f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fde6f-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fde6f-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fde6f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="fde6f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde6f-135"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fde6f-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fde6f-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fde6f-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="fde6f-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde6f-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fde6f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fde6f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde6f-139">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="fde6f-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="fde6f-140">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="fde6f-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="fde6f-141">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="fde6f-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




