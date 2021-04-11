---
description: Se produit lorsque la position de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: InkOverlay. SelectionMoved, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320442"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="0d43d-103">Événement InkOverlay. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="0d43d-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="0d43d-104">Se produit lorsque la position de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="0d43d-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d43d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d43d-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="0d43d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d43d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d43d-107">*OldSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d43d-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d43d-108">Rectangle englobant de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sélectionnée telle qu’elle existait avant le déclenchement de l’événement **SelectionMoved** .</span><span class="sxs-lookup"><span data-stu-id="0d43d-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="0d43d-109">Ce rectangle est spécifié dans les coordonnées d’espace d’encre, ce qui permet les scénarios d’annulation.</span><span class="sxs-lookup"><span data-stu-id="0d43d-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d43d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d43d-110">Return value</span></span>

<span data-ttu-id="0d43d-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0d43d-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d43d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0d43d-112">Remarks</span></span>

<span data-ttu-id="0d43d-113">La méthode d’événement TCet est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec un ID de DISPID \_ IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="0d43d-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="0d43d-114">Pour obtenir le nouveau rectangle englobant de la collection de traits qui ont été déplacés, appelez la méthode [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="0d43d-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d43d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d43d-115">Requirements</span></span>



| <span data-ttu-id="0d43d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d43d-116">Requirement</span></span> | <span data-ttu-id="0d43d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d43d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d43d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d43d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0d43d-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d43d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0d43d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d43d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0d43d-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d43d-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0d43d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d43d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d43d-123"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0d43d-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0d43d-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0d43d-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d43d-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d43d-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0d43d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d43d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d43d-127">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="0d43d-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="0d43d-128">**Propriété de sélection**</span><span class="sxs-lookup"><span data-stu-id="0d43d-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="0d43d-129">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="0d43d-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

