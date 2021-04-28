---
description: L’événement InkPicture. SelectionResized-se produit lorsque la taille de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: InkPicture. SelectionResized, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dcad4b84cd21ee9b4d385f24033c56913765810
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086467"
---
# <a name="inkpictureselectionresized-event"></a><span data-ttu-id="1cc83-103">InkPicture. SelectionResized, événement</span><span class="sxs-lookup"><span data-stu-id="1cc83-103">InkPicture.SelectionResized event</span></span>

<span data-ttu-id="1cc83-104">Se produit lorsque la taille de la sélection actuelle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="1cc83-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc83-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cc83-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="1cc83-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cc83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc83-107">*OldSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cc83-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc83-108">Rectangle englobant de la collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sélectionnée telle qu’elle existait avant le déclenchement de l’événement **SelectionResized** .</span><span class="sxs-lookup"><span data-stu-id="1cc83-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="1cc83-109">Ce rectangle est spécifié dans les coordonnées d’espace d’encre, ce qui permet les scénarios d’annulation.</span><span class="sxs-lookup"><span data-stu-id="1cc83-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc83-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1cc83-110">Return value</span></span>

<span data-ttu-id="1cc83-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1cc83-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc83-112">Notes </span><span class="sxs-lookup"><span data-stu-id="1cc83-112">Remarks</span></span>

<span data-ttu-id="1cc83-113">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="1cc83-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc83-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cc83-114">Requirements</span></span>



| <span data-ttu-id="1cc83-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cc83-115">Requirement</span></span> | <span data-ttu-id="1cc83-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cc83-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc83-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc83-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cc83-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1cc83-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc83-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc83-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1cc83-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cc83-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc83-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc83-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1cc83-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1cc83-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cc83-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc83-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1cc83-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cc83-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc83-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1cc83-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="1cc83-127">[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="1cc83-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="1cc83-128">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="1cc83-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

