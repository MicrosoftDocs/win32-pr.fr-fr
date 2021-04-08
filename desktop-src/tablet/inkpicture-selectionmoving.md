---
description: Se produit lorsque la position de la sélection actuelle est sur le point de changer, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: InkPicture. SelectionMoving, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2dbc0064e22f21faf80d67f51ca1eeb58b6433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035177"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="37ea3-103">InkPicture. SelectionMoving, événement</span><span class="sxs-lookup"><span data-stu-id="37ea3-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="37ea3-104">Se produit lorsque la position de la sélection actuelle est sur le point de changer, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="37ea3-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ea3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37ea3-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="37ea3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37ea3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ea3-107">*CurSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37ea3-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ea3-108">Rectangle dans lequel la sélection est déplacée après l’événement **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="37ea3-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="37ea3-109">Ce rectangle est spécifié dans les coordonnées de la fenêtre cliente, ce qui permet des scénarios tels que la conservation des proportions lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="37ea3-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ea3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37ea3-110">Return value</span></span>

<span data-ttu-id="37ea3-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="37ea3-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37ea3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="37ea3-112">Remarks</span></span>

<span data-ttu-id="37ea3-113">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="37ea3-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ea3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37ea3-114">Requirements</span></span>



| <span data-ttu-id="37ea3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37ea3-115">Requirement</span></span> | <span data-ttu-id="37ea3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="37ea3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ea3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ea3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="37ea3-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37ea3-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="37ea3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ea3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="37ea3-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ea3-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="37ea3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="37ea3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="37ea3-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="37ea3-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37ea3-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37ea3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="37ea3-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ea3-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="37ea3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37ea3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ea3-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="37ea3-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="37ea3-127">[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="37ea3-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="37ea3-128">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="37ea3-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




