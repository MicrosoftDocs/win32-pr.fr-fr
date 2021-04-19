---
description: Se produit lorsque la sélection d’encre dans le contrôle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: InkOverlay. SelectionChanging, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541231"
---
# <a name="inkoverlayselectionchanging-event"></a><span data-ttu-id="dcada-103">Événement InkOverlay. SelectionChanging</span><span class="sxs-lookup"><span data-stu-id="dcada-103">InkOverlay.SelectionChanging event</span></span>

<span data-ttu-id="dcada-104">Se produit lorsque la sélection d’encre dans le contrôle va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="dcada-104">Occurs when the selection of ink within the control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcada-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcada-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="dcada-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcada-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcada-107">*NewSelection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcada-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcada-108">Nouvelle collection de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="dcada-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcada-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcada-109">Return value</span></span>

<span data-ttu-id="dcada-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dcada-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcada-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dcada-111">Remarks</span></span>

<span data-ttu-id="dcada-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOESelectionChanging.</span><span class="sxs-lookup"><span data-stu-id="dcada-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcada-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcada-113">Requirements</span></span>



| <span data-ttu-id="dcada-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcada-114">Requirement</span></span> | <span data-ttu-id="dcada-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcada-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcada-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcada-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dcada-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcada-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dcada-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcada-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dcada-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcada-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="dcada-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcada-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcada-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dcada-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dcada-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcada-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcada-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcada-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dcada-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcada-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcada-125">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="dcada-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="dcada-126">**Propriété de sélection**</span><span class="sxs-lookup"><span data-stu-id="dcada-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

