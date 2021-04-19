---
description: Se produit lorsque la sélection d’encre dans le contrôle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: InkOverlay. SelectionChanged, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523418"
---
# <a name="inkoverlayselectionchanged-event"></a><span data-ttu-id="d9c11-103">InkOverlay. SelectionChanged, événement</span><span class="sxs-lookup"><span data-stu-id="d9c11-103">InkOverlay.SelectionChanged event</span></span>

<span data-ttu-id="d9c11-104">Se produit lorsque la sélection d’encre dans le contrôle a changé, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="d9c11-104">Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c11-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9c11-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="d9c11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9c11-106">Parameters</span></span>

<span data-ttu-id="d9c11-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d9c11-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9c11-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d9c11-108">Return value</span></span>

<span data-ttu-id="d9c11-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d9c11-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9c11-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d9c11-110">Remarks</span></span>

<span data-ttu-id="d9c11-111">Il n’y a aucune donnée d’événement.</span><span class="sxs-lookup"><span data-stu-id="d9c11-111">There are no event data.</span></span>

<span data-ttu-id="d9c11-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOESelectionChanged.</span><span class="sxs-lookup"><span data-stu-id="d9c11-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c11-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9c11-113">Requirements</span></span>



| <span data-ttu-id="d9c11-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9c11-114">Requirement</span></span> | <span data-ttu-id="d9c11-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9c11-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c11-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9c11-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9c11-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9c11-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d9c11-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9c11-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9c11-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9c11-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d9c11-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9c11-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9c11-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d9c11-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d9c11-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d9c11-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9c11-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9c11-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d9c11-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9c11-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c11-125">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="d9c11-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="d9c11-126">**Propriété de sélection**</span><span class="sxs-lookup"><span data-stu-id="d9c11-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 




