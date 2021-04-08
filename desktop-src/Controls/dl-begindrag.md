---
title: DL_BEGINDRAG le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la zone de liste de glissement que l’utilisateur a cliqué avec le bouton gauche de la souris sur un élément. Une zone de liste de glissement envoie ce code de notification sous la forme d’un message de liste de glissement. Pour plus d’informations, consultez faire glisser des messages de zone de liste.
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- Contrôles Windows de code de notification DL_BEGINDRAG
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844494"
---
# <a name="dl_begindrag-notification-code"></a><span data-ttu-id="d6335-106">\_Code de notification DL BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="d6335-106">DL\_BEGINDRAG notification code</span></span>

<span data-ttu-id="d6335-107">Avertit la fenêtre parente de la zone de liste de glissement que l’utilisateur a cliqué avec le bouton gauche de la souris sur un élément.</span><span class="sxs-lookup"><span data-stu-id="d6335-107">Notifies the drag list box's parent window that the user has clicked the left mouse button on an item.</span></span> <span data-ttu-id="d6335-108">Une zone de liste de glissement envoie ce code de notification sous la forme d’un message de liste de glissement.</span><span class="sxs-lookup"><span data-stu-id="d6335-108">A drag list box sends this notification code in the form of a drag list message.</span></span> <span data-ttu-id="d6335-109">Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="d6335-109">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d6335-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6335-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6335-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6335-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6335-112">Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient le code de \_ notification DL BEGINDRAG, le handle de la zone de liste de glissement et la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="d6335-112">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_BEGINDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6335-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6335-113">Return value</span></span>

<span data-ttu-id="d6335-114">Retourne **true** pour commencer l’opération glisser ou **false** pour empêcher l’opération glisser.</span><span class="sxs-lookup"><span data-stu-id="d6335-114">Return **TRUE** to begin the drag operation, or **FALSE** to prevent the drag operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6335-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d6335-115">Remarks</span></span>

<span data-ttu-id="d6335-116">Lors du traitement de ce code de notification, une procédure de fenêtre détermine généralement l’élément de liste à la position de curseur spécifiée à l’aide de la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .</span><span class="sxs-lookup"><span data-stu-id="d6335-116">When processing this notification code, a window procedure typically determines the list item at the specified cursor position by using the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function.</span></span> <span data-ttu-id="d6335-117">Elle retourne ensuite **true** ou **false**, selon que l’élément doit ou non être glissé.</span><span class="sxs-lookup"><span data-stu-id="d6335-117">It then returns **TRUE** or **FALSE**, depending on whether the item should be dragged.</span></span> <span data-ttu-id="d6335-118">Avant de retourner **true**, la procédure de fenêtre doit enregistrer l’index de l’élément de liste afin que l’application sache quel élément déplacer ou copier lorsque l’opération glisser est terminée.</span><span class="sxs-lookup"><span data-stu-id="d6335-118">Before returning **TRUE**, the window procedure should save the index of the list item so the application knows which item to move or copy when the drag operation is completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6335-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6335-119">Requirements</span></span>



| <span data-ttu-id="d6335-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6335-120">Requirement</span></span> | <span data-ttu-id="d6335-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6335-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6335-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6335-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6335-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6335-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6335-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6335-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6335-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6335-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6335-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6335-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6335-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6335-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





