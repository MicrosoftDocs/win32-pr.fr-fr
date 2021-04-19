---
description: Se produit lorsque le pointeur de la souris est déplacé sur l’objet InkCollector ou InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Événement InkCollector. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ad88c35871ed73125be73b66329ede464f0c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515441"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="ce7c2-103">Événement InkCollector. MouseMove</span><span class="sxs-lookup"><span data-stu-id="ce7c2-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="ce7c2-104">Se produit lorsque le pointeur de la souris est déplacé sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="ce7c2-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce7c2-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ce7c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce7c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce7c2-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7c2-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-108">Bouton de la souris sur lequel l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="ce7c2-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7c2-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="ce7c2-111">*PX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7c2-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-112">Coordonnée x, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ce7c2-113">*py* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7c2-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-114">Coordonnée y, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ce7c2-115">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce7c2-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7c2-116">**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce7c2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce7c2-117">Return value</span></span>

<span data-ttu-id="ce7c2-118">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce7c2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ce7c2-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce7c2-120">Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="ce7c2-121">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce7c2-122">Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkcollector-mousedown.md), **MouseMove** et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="ce7c2-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="ce7c2-123">L’annulation de certains de ces événements peut avoir des résultats imprévus.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="ce7c2-124">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="ce7c2-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7c2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce7c2-125">Requirements</span></span>



| <span data-ttu-id="ce7c2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce7c2-126">Requirement</span></span> | <span data-ttu-id="ce7c2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce7c2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7c2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce7c2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ce7c2-129">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce7c2-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ce7c2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce7c2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ce7c2-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce7c2-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ce7c2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce7c2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce7c2-133"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ce7c2-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ce7c2-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce7c2-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce7c2-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce7c2-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ce7c2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce7c2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce7c2-137">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="ce7c2-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="ce7c2-138">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="ce7c2-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ce7c2-139">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="ce7c2-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




