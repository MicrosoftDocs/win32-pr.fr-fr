---
description: Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: InkOverlay. SelectionResizing, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7debb9461aae39c0549bce863a0513b86c53ffa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209923"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="3c4f9-103">Événement InkOverlay. SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="3c4f9-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="3c4f9-104">Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="3c4f9-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c4f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c4f9-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="3c4f9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c4f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c4f9-107">*CurSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c4f9-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c4f9-108">Rectangle englobant de la sélection après l’événement **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="3c4f9-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="3c4f9-109">Ce rectangle est spécifié dans les coordonnées de la fenêtre cliente, ce qui permet des scénarios tels que la conservation des proportions lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="3c4f9-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c4f9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c4f9-110">Return value</span></span>

<span data-ttu-id="3c4f9-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3c4f9-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c4f9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3c4f9-112">Remarks</span></span>

<span data-ttu-id="3c4f9-113">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="3c4f9-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c4f9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c4f9-114">Requirements</span></span>



| <span data-ttu-id="3c4f9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c4f9-115">Requirement</span></span> | <span data-ttu-id="3c4f9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c4f9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4f9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c4f9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3c4f9-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c4f9-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3c4f9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c4f9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3c4f9-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c4f9-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3c4f9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c4f9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c4f9-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3c4f9-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c4f9-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c4f9-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c4f9-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c4f9-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3c4f9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c4f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c4f9-126">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="3c4f9-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="3c4f9-127">**Propriété de sélection**</span><span class="sxs-lookup"><span data-stu-id="3c4f9-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="3c4f9-128">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="3c4f9-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




