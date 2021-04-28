---
description: L’événement InkOverlay. MouseWheel se produit lorsque la roulette de la souris se déplace alors que l’objet InkCollector ou InkOverlay a le focus.
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: InkOverlay. MouseWheel, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468dbdac09fd40144768e8342791d5712a570bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116887"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="e7716-103">InkOverlay. MouseWheel, événement</span><span class="sxs-lookup"><span data-stu-id="e7716-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="e7716-104">Se produit lorsque la roulette de la souris se déplace alors que l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="e7716-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7716-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7716-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="e7716-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7716-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7716-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7716-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7716-108">Bouton de la souris sur lequel l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="e7716-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="e7716-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7716-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7716-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="e7716-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="e7716-111">*Delta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7716-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7716-112">Décompte signé du nombre de détentes de rotation de la roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="e7716-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="e7716-113">Une détente représente un cran de la roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="e7716-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="e7716-114">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7716-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7716-115">Coordonnée x, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="e7716-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="e7716-116">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7716-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7716-117">Coordonnée y, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="e7716-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="e7716-118">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e7716-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7716-119">Indique si l’événement doit être annulé pour le contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="e7716-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="e7716-120">La valeur par défaut est **false**, ce qui spécifie que l’événement ne doit pas être annulé.</span><span class="sxs-lookup"><span data-stu-id="e7716-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7716-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e7716-121">Return value</span></span>

<span data-ttu-id="e7716-122">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e7716-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7716-123">Notes </span><span class="sxs-lookup"><span data-stu-id="e7716-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e7716-124">Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="e7716-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="e7716-125">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.</span><span class="sxs-lookup"><span data-stu-id="e7716-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="e7716-126">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="e7716-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7716-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7716-127">Requirements</span></span>



| <span data-ttu-id="e7716-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7716-128">Requirement</span></span> | <span data-ttu-id="e7716-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7716-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7716-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7716-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e7716-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7716-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e7716-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7716-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e7716-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7716-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e7716-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7716-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7716-135"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e7716-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7716-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7716-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7716-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7716-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e7716-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7716-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7716-139">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="e7716-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="e7716-140">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="e7716-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="e7716-141">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="e7716-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




