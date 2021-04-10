---
description: Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: InkPicture. SelectionResizing, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1b7923810777c6ebe0af3364121cbcee67b18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952917"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="bdb56-103">InkPicture. SelectionResizing, événement</span><span class="sxs-lookup"><span data-stu-id="bdb56-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="bdb56-104">Se produit lorsque la taille de la sélection actuelle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="bdb56-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb56-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdb56-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="bdb56-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdb56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb56-107">*CurSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdb56-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb56-108">Rectangle englobant de la sélection après l’événement **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="bdb56-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="bdb56-109">Ce rectangle est spécifié dans les coordonnées de la fenêtre cliente, ce qui permet des scénarios tels que la conservation des proportions lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="bdb56-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb56-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdb56-110">Return value</span></span>

<span data-ttu-id="bdb56-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bdb56-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb56-112">Notes</span><span class="sxs-lookup"><span data-stu-id="bdb56-112">Remarks</span></span>

<span data-ttu-id="bdb56-113">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="bdb56-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb56-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdb56-114">Requirements</span></span>



| <span data-ttu-id="bdb56-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdb56-115">Requirement</span></span> | <span data-ttu-id="bdb56-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdb56-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb56-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdb56-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb56-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bdb56-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bdb56-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdb56-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb56-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bdb56-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bdb56-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdb56-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb56-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bdb56-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bdb56-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bdb56-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdb56-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb56-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bdb56-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdb56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb56-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="bdb56-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="bdb56-127">[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="bdb56-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="bdb56-128">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="bdb56-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




