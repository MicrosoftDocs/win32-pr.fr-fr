---
description: Se produit lorsque le pointeur de la souris est déplacé sur l’objet InkCollector ou InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: InkOverlay. MouseMove, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210298"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="0da5f-103">InkOverlay. MouseMove, événement</span><span class="sxs-lookup"><span data-stu-id="0da5f-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="0da5f-104">Se produit lorsque le pointeur de la souris est déplacé sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5f-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0da5f-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="0da5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0da5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da5f-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0da5f-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0da5f-108">Bouton de la souris sur lequel l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="0da5f-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="0da5f-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0da5f-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0da5f-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="0da5f-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="0da5f-111">*PX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0da5f-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0da5f-112">Coordonnée x, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="0da5f-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="0da5f-113">*py* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0da5f-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0da5f-114">Coordonnée y, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="0da5f-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="0da5f-115">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0da5f-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0da5f-116">Indique si l’événement doit être annulé pour le contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="0da5f-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="0da5f-117">La valeur par défaut est **false**, ce qui spécifie que l’événement ne doit pas être annulé.</span><span class="sxs-lookup"><span data-stu-id="0da5f-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da5f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0da5f-118">Return value</span></span>

<span data-ttu-id="0da5f-119">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0da5f-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0da5f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0da5f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0da5f-121">Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="0da5f-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="0da5f-122">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.</span><span class="sxs-lookup"><span data-stu-id="0da5f-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="0da5f-123">Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="0da5f-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="0da5f-124">L’annulation de certains de ces événements peut avoir des résultats imprévus.</span><span class="sxs-lookup"><span data-stu-id="0da5f-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="0da5f-125">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="0da5f-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da5f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0da5f-126">Requirements</span></span>



| <span data-ttu-id="0da5f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0da5f-127">Requirement</span></span> | <span data-ttu-id="0da5f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0da5f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da5f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0da5f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0da5f-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0da5f-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0da5f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0da5f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0da5f-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0da5f-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0da5f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0da5f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0da5f-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0da5f-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0da5f-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0da5f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="0da5f-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0da5f-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0da5f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0da5f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da5f-138">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="0da5f-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="0da5f-139">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="0da5f-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="0da5f-140">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="0da5f-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




