---
description: Se produit lorsque la roulette de la souris se déplace alors que l’objet InkCollector ou InkOverlay a le focus.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Événement InkCollector. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e6a6728bfcbe058ff5eab56499f6c8e885351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514008"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="2ce64-103">Événement InkCollector. MouseWheel</span><span class="sxs-lookup"><span data-stu-id="2ce64-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="2ce64-104">Se produit lorsque la roulette de la souris se déplace alors que l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="2ce64-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ce64-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2ce64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ce64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce64-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ce64-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce64-108">Bouton de la souris sur lequel l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="2ce64-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="2ce64-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ce64-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce64-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="2ce64-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="2ce64-111">*Delta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ce64-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce64-112">Décompte signé du nombre de détentes de rotation de la roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="2ce64-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="2ce64-113">Une détente représente un cran de la roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="2ce64-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="2ce64-114">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ce64-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce64-115">Coordonnée x, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="2ce64-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="2ce64-116">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ce64-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce64-117">Coordonnée y, en pixels, d’un clic de souris.</span><span class="sxs-lookup"><span data-stu-id="2ce64-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="2ce64-118">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2ce64-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce64-119">**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="2ce64-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="2ce64-120">La valeur par défaut **est \_ false**.</span><span class="sxs-lookup"><span data-stu-id="2ce64-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce64-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ce64-121">Return value</span></span>

<span data-ttu-id="2ce64-122">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2ce64-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce64-123">Notes</span><span class="sxs-lookup"><span data-stu-id="2ce64-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2ce64-124">Les propriétés *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées à l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="2ce64-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="2ce64-125">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application ne prenant pas en charge le stylet et que ce type d’application comprend uniquement des pixels.</span><span class="sxs-lookup"><span data-stu-id="2ce64-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="2ce64-126">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="2ce64-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce64-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ce64-127">Requirements</span></span>



| <span data-ttu-id="2ce64-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ce64-128">Requirement</span></span> | <span data-ttu-id="2ce64-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ce64-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce64-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ce64-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce64-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ce64-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2ce64-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ce64-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce64-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ce64-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2ce64-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ce64-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ce64-135"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce64-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2ce64-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2ce64-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ce64-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce64-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2ce64-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ce64-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce64-139">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="2ce64-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="2ce64-140">**Énumération InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="2ce64-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="2ce64-141">**Énumération InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="2ce64-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




