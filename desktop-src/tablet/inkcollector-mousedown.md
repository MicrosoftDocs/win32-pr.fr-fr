---
description: Événement InkCollector. MouseDown-se produit lorsque le pointeur de la souris se trouve sur l’objet InkCollector ou InkOverlay et qu’un bouton de la souris est enfoncé.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: Événement InkCollector. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d29c8d3ba19856a8d6bfa038837b592c0b5f2b36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110177"
---
# <a name="inkcollectormousedown-event"></a><span data-ttu-id="580ca-103">Événement InkCollector. MouseDown</span><span class="sxs-lookup"><span data-stu-id="580ca-103">InkCollector.MouseDown event</span></span>

<span data-ttu-id="580ca-104">Se produit lorsque le pointeur de la souris se trouve sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) et qu’un bouton de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="580ca-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="580ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="580ca-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="580ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="580ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="580ca-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="580ca-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="580ca-108">Bouton de la souris sur lequel l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="580ca-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="580ca-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="580ca-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="580ca-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="580ca-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="580ca-111">*PX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="580ca-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="580ca-112">Coordonnée X, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="580ca-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="580ca-113">*py* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="580ca-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="580ca-114">Coordonnée Y, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="580ca-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="580ca-115">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="580ca-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="580ca-116">**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="580ca-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="580ca-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="580ca-117">Return value</span></span>

<span data-ttu-id="580ca-118">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="580ca-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="580ca-119">Notes </span><span class="sxs-lookup"><span data-stu-id="580ca-119">Remarks</span></span>

<span data-ttu-id="580ca-120">Pour améliorer les performances de l’encre en temps réel, masquez ou affichez le curseur de la souris dans les gestionnaires d’événements **MouseDown** et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="580ca-120">To improve real-time ink performance, hide or show the mouse cursor in the **MouseDown** and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="580ca-121">Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="580ca-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="580ca-122">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.</span><span class="sxs-lookup"><span data-stu-id="580ca-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="580ca-123">Certains contrôles s’appuient sur une relation spécifique entre les événements **MouseDown**, [**MouseMove**](inkcollector-mousemove.md)et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="580ca-123">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="580ca-124">L’annulation de certains de ces événements peut avoir des résultats imprévus.</span><span class="sxs-lookup"><span data-stu-id="580ca-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="580ca-125">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="580ca-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="580ca-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="580ca-126">Requirements</span></span>



| <span data-ttu-id="580ca-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="580ca-127">Requirement</span></span> | <span data-ttu-id="580ca-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="580ca-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="580ca-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="580ca-129">Minimum supported client</span></span><br/> | <span data-ttu-id="580ca-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="580ca-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="580ca-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="580ca-131">Minimum supported server</span></span><br/> | <span data-ttu-id="580ca-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="580ca-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="580ca-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="580ca-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="580ca-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="580ca-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="580ca-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="580ca-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="580ca-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="580ca-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="580ca-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="580ca-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580ca-138">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="580ca-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="580ca-139">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="580ca-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="580ca-140">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="580ca-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="580ca-141">**Événement MouseUp**</span><span class="sxs-lookup"><span data-stu-id="580ca-141">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




