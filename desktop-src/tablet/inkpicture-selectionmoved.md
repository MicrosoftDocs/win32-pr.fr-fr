---
description: L’événement InkPicture. SelectionMoved se produit lorsque la position de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: InkPicture. SelectionMoved, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2006b2580e8732c90187b265576b217cdbad9b02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086447"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="50efe-103">InkPicture. SelectionMoved, événement</span><span class="sxs-lookup"><span data-stu-id="50efe-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="50efe-104">Se produit lorsque la position de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="50efe-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="50efe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50efe-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="50efe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50efe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50efe-107">*OldSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50efe-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50efe-108">Rectangle englobant de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sélectionnée telle qu’elle existait avant le déclenchement de l’événement **SelectionMoved** .</span><span class="sxs-lookup"><span data-stu-id="50efe-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="50efe-109">Ce rectangle est spécifié dans les coordonnées d’espace d’encre, ce qui permet les scénarios d’annulation.</span><span class="sxs-lookup"><span data-stu-id="50efe-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50efe-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="50efe-110">Return value</span></span>

<span data-ttu-id="50efe-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="50efe-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50efe-112">Notes </span><span class="sxs-lookup"><span data-stu-id="50efe-112">Remarks</span></span>

<span data-ttu-id="50efe-113">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="50efe-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="50efe-114">Pour obtenir le nouveau rectangle englobant de la collection de traits qui ont été déplacés, appelez la méthode [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="50efe-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50efe-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50efe-115">Requirements</span></span>



| <span data-ttu-id="50efe-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50efe-116">Requirement</span></span> | <span data-ttu-id="50efe-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="50efe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50efe-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50efe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50efe-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50efe-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="50efe-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50efe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50efe-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="50efe-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="50efe-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="50efe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="50efe-123"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="50efe-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="50efe-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50efe-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="50efe-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50efe-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="50efe-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50efe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50efe-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="50efe-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="50efe-128">[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="50efe-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="50efe-129">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="50efe-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

