---
description: L’événement InkPicture. SelectionResizing-se produit lorsque la taille de la sélection actuelle est sur le paragraphe de la modification, par exemple par le biais des modifications apportées à l’interface utilisateur, aux procédures couper-coller ou à la propriété de sélection.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: InkPicture. SelectionResizing, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8f70b0b502fe426cfd94ce9002e8bbfc5260a88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086417"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="40170-103">InkPicture. SelectionResizing, événement</span><span class="sxs-lookup"><span data-stu-id="40170-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="40170-104">Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="40170-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="40170-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40170-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="40170-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40170-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40170-107">*CurSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40170-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40170-108">Rectangle englobant de la sélection après l’événement **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="40170-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="40170-109">Ce rectangle est spécifié dans les coordonnées de la fenêtre cliente, ce qui permet des scénarios tels que la conservation des proportions lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="40170-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40170-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40170-110">Return value</span></span>

<span data-ttu-id="40170-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="40170-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40170-112">Notes </span><span class="sxs-lookup"><span data-stu-id="40170-112">Remarks</span></span>

<span data-ttu-id="40170-113">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="40170-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="40170-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40170-114">Requirements</span></span>



| <span data-ttu-id="40170-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40170-115">Requirement</span></span> | <span data-ttu-id="40170-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="40170-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40170-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40170-117">Minimum supported client</span></span><br/> | <span data-ttu-id="40170-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40170-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="40170-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40170-119">Minimum supported server</span></span><br/> | <span data-ttu-id="40170-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40170-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="40170-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="40170-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="40170-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="40170-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="40170-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40170-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="40170-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40170-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="40170-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40170-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40170-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="40170-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="40170-127">[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="40170-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="40170-128">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="40170-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




