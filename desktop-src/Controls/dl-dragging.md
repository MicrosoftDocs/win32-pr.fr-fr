---
title: DL_DRAGGING le code de notification (commctrl. h)
description: Signale que l’utilisateur a déplacé la souris tout en faisant glisser un élément.
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- Contrôles Windows de code de notification DL_DRAGGING
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519337"
---
# <a name="dl_dragging-notification-code"></a><span data-ttu-id="20108-104">DL- \_ glissement du code de notification</span><span class="sxs-lookup"><span data-stu-id="20108-104">DL\_DRAGGING notification code</span></span>

<span data-ttu-id="20108-105">Signale que l’utilisateur a déplacé la souris tout en faisant glisser un élément.</span><span class="sxs-lookup"><span data-stu-id="20108-105">Signals that the user has moved the mouse while dragging an item.</span></span> <span data-ttu-id="20108-106">\_La fonction de glisser-déplacer est également envoyée périodiquement lors du glissement, même si la souris n’est pas déplacée.</span><span class="sxs-lookup"><span data-stu-id="20108-106">DL\_DRAGGING is also sent periodically during dragging even if the mouse is not moved.</span></span> <span data-ttu-id="20108-107">Une zone de liste de glissement envoie ce code de notification à sa fenêtre parente sous la forme d’un message de liste de glissement.</span><span class="sxs-lookup"><span data-stu-id="20108-107">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="20108-108">Pour plus d’informations, consultez [faire glisser des messages de zone de liste](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="20108-108">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="20108-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20108-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20108-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20108-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20108-111">Identificateur de contrôle de la zone de liste de glissement.</span><span class="sxs-lookup"><span data-stu-id="20108-111">The control identifier of the drag list box.</span></span>

</dd> <dt>

<span data-ttu-id="20108-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20108-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20108-113">Pointeur vers une structure [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) qui contient la liste de distribution \_ faisant glisser le code de notification, le handle vers la zone de liste de glissement et la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="20108-113">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_DRAGGING notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20108-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20108-114">Return value</span></span>

<span data-ttu-id="20108-115">La valeur de retour détermine le type de curseur de la souris que doit définir la liste de glissement. Il peut s’agir de la \_ valeur DL STOPCURSOR, DL \_ COPYCURSOR ou DL \_ MOVECURSOR.</span><span class="sxs-lookup"><span data-stu-id="20108-115">The return value determines the type of mouse cursor that the drag list should set; it can be the DL\_STOPCURSOR, DL\_COPYCURSOR, or DL\_MOVECURSOR value.</span></span> <span data-ttu-id="20108-116">Si une autre valeur est retournée, le curseur ne change pas.</span><span class="sxs-lookup"><span data-stu-id="20108-116">If any other value is returned, the cursor does not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="20108-117">Notes</span><span class="sxs-lookup"><span data-stu-id="20108-117">Remarks</span></span>

<span data-ttu-id="20108-118">Une procédure de fenêtre traite généralement la LD \_ en faisant glisser le code de notification en déterminant l’élément sous le curseur, puis en dessinant une icône d’insertion.</span><span class="sxs-lookup"><span data-stu-id="20108-118">A window procedure typically processes the DL\_DRAGGING notification code by determining the item under the cursor and then drawing an insert icon.</span></span> <span data-ttu-id="20108-119">Pour récupérer l’élément sous le curseur, utilisez la fonction [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) , en spécifiant **true** pour le paramètre *bAutoScroll* .</span><span class="sxs-lookup"><span data-stu-id="20108-119">To retrieve the item under the cursor, use the [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) function, specifying **TRUE** for the *bAutoScroll* parameter.</span></span> <span data-ttu-id="20108-120">Cette option permet de faire défiler régulièrement la zone de liste glisser si le curseur se trouve au-dessus ou au-dessous de sa zone cliente.</span><span class="sxs-lookup"><span data-stu-id="20108-120">This option causes the drag list box to scroll periodically if the cursor is above or below its client area.</span></span> <span data-ttu-id="20108-121">Pour dessiner l’icône d’insertion, utilisez la fonction [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) .</span><span class="sxs-lookup"><span data-stu-id="20108-121">To draw the insert icon, use the [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="20108-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20108-122">Requirements</span></span>



| <span data-ttu-id="20108-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20108-123">Requirement</span></span> | <span data-ttu-id="20108-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="20108-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20108-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20108-125">Minimum supported client</span></span><br/> | <span data-ttu-id="20108-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20108-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20108-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20108-127">Minimum supported server</span></span><br/> | <span data-ttu-id="20108-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20108-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20108-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="20108-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="20108-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="20108-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





