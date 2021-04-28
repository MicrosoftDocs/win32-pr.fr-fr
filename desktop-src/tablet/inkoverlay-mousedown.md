---
description: L’événement InkOverlay. MouseDown se produit lorsque le pointeur de la souris se trouve sur l’objet InkCollector ou InkOverlay et qu’un bouton de la souris est enfoncé.
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: InkOverlay. MouseDown, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff1e4bff715a6585ee607de766c809579f527aa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086817"
---
# <a name="inkoverlaymousedown-event"></a><span data-ttu-id="61933-103">InkOverlay. MouseDown, événement</span><span class="sxs-lookup"><span data-stu-id="61933-103">InkOverlay.MouseDown event</span></span>

<span data-ttu-id="61933-104">Se produit lorsque le pointeur de la souris se trouve sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) et qu’un bouton de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="61933-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="61933-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61933-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="61933-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61933-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61933-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61933-108">Bouton de la souris sur lequel l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="61933-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="61933-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61933-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61933-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="61933-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="61933-111">*PX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61933-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61933-112">Coordonnée X, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="61933-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="61933-113">*py* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61933-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61933-114">Coordonnée Y, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="61933-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="61933-115">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="61933-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61933-116">**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="61933-116">**VARIANT\_TRUE** to cancelt he event forthe parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="61933-117">La valeur par défaut est **Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="61933-117">The default value is **VARIANT\_FALSE**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61933-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="61933-118">Return value</span></span>

<span data-ttu-id="61933-119">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="61933-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61933-120">Notes </span><span class="sxs-lookup"><span data-stu-id="61933-120">Remarks</span></span>

<span data-ttu-id="61933-121">Pour améliorer les performances de l’encre en temps réel, masquez ou affichez le curseur de la souris dans les gestionnaires d’événements [**MouseDown**](inkcollector-mousedown.md) et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="61933-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="61933-122">Les propriétés pX et pY sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="61933-122">The properties pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="61933-123">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.</span><span class="sxs-lookup"><span data-stu-id="61933-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="61933-124">Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="61933-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="61933-125">L’annulation de certains de ces événements peut avoir des résultats imprévus.</span><span class="sxs-lookup"><span data-stu-id="61933-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="61933-126">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="61933-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="61933-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61933-127">Requirements</span></span>



| <span data-ttu-id="61933-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61933-128">Requirement</span></span> | <span data-ttu-id="61933-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="61933-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61933-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61933-130">Minimum supported client</span></span><br/> | <span data-ttu-id="61933-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61933-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="61933-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61933-132">Minimum supported server</span></span><br/> | <span data-ttu-id="61933-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="61933-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="61933-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="61933-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="61933-135"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="61933-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="61933-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="61933-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="61933-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61933-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="61933-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61933-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61933-139">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="61933-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="61933-140">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="61933-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="61933-141">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="61933-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="61933-142">**Événement MouseUp**</span><span class="sxs-lookup"><span data-stu-id="61933-142">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




