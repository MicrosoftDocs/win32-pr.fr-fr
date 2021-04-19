---
description: Se produit lorsque la position de la sélection actuelle est sur le point de changer, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: InkOverlay. SelectionMoving, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519494"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="0f115-103">Événement InkOverlay. SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="0f115-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="0f115-104">Se produit lorsque la position de la sélection actuelle est sur le point de changer, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="0f115-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f115-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f115-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="0f115-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f115-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f115-107">*CurSelectionRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f115-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f115-108">Rectangle dans lequel la sélection est déplacée après l’événement **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="0f115-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="0f115-109">Ce rectangle est spécifié dans les coordonnées de la fenêtre cliente, ce qui permet des scénarios tels que la conservation des proportions lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="0f115-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f115-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f115-110">Return value</span></span>

<span data-ttu-id="0f115-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0f115-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f115-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0f115-112">Remarks</span></span>

<span data-ttu-id="0f115-113">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec un ID de DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="0f115-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f115-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f115-114">Requirements</span></span>



| <span data-ttu-id="0f115-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f115-115">Requirement</span></span> | <span data-ttu-id="0f115-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f115-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f115-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f115-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f115-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f115-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0f115-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f115-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f115-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f115-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0f115-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f115-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f115-122"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0f115-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0f115-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0f115-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f115-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f115-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0f115-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f115-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f115-126">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="0f115-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="0f115-127">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="0f115-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="0f115-128">**Propriété de sélection**</span><span class="sxs-lookup"><span data-stu-id="0f115-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="0f115-129">**InkRectangle, classe**</span><span class="sxs-lookup"><span data-stu-id="0f115-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 




