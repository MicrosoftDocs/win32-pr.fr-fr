---
description: L’événement InkOverlay. SelectionResizing-se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: InkOverlay. SelectionResizing, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b5577f83c14ccc2e998fb4257344729e2219a2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086677"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="eb627-103">Événement InkOverlay. SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="eb627-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="eb627-104">Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="eb627-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb627-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb627-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="eb627-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb627-107">*CurSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb627-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb627-108">Rectangle englobant de la sélection après l’événement **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="eb627-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="eb627-109">Ce rectangle est spécifié dans les coordonnées de la fenêtre cliente, ce qui permet des scénarios tels que la conservation des proportions lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="eb627-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb627-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb627-110">Return value</span></span>

<span data-ttu-id="eb627-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="eb627-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb627-112">Notes </span><span class="sxs-lookup"><span data-stu-id="eb627-112">Remarks</span></span>

<span data-ttu-id="eb627-113">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="eb627-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb627-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb627-114">Requirements</span></span>



| <span data-ttu-id="eb627-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb627-115">Requirement</span></span> | <span data-ttu-id="eb627-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb627-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb627-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb627-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eb627-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb627-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="eb627-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb627-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eb627-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb627-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="eb627-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb627-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb627-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eb627-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eb627-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb627-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb627-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb627-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="eb627-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb627-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb627-126">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="eb627-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="eb627-127">**Propriété de sélection**</span><span class="sxs-lookup"><span data-stu-id="eb627-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="eb627-128">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="eb627-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




