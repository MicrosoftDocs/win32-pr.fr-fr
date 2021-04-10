---
description: Définit le texte d’une fenêtre.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Message WM_SETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759495"
---
# <a name="wm_settext-message"></a><span data-ttu-id="05dce-103">\_Message WM SETTEXT</span><span class="sxs-lookup"><span data-stu-id="05dce-103">WM\_SETTEXT message</span></span>

<span data-ttu-id="05dce-104">Définit le texte d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="05dce-104">Sets the text of a window.</span></span>


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a><span data-ttu-id="05dce-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05dce-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05dce-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05dce-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05dce-107">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="05dce-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="05dce-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05dce-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05dce-109">Pointeur vers une chaîne se terminant par null qui est le texte de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="05dce-109">A pointer to a null-terminated string that is the window text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05dce-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05dce-110">Return value</span></span>

<span data-ttu-id="05dce-111">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="05dce-111">Type: **LRESULT**</span></span>

<span data-ttu-id="05dce-112">La valeur de retour est **true** si le texte est défini.</span><span class="sxs-lookup"><span data-stu-id="05dce-112">The return value is **TRUE** if the text is set.</span></span> <span data-ttu-id="05dce-113">Il a la **valeur false** (pour un contrôle d’édition), **lb \_ ERRSPACE** (pour une zone de liste) ou **CB \_ ERRSPACE** (pour une zone de liste déroulante) si l’espace disponible est insuffisant pour définir le texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="05dce-113">It is **FALSE** (for an edit control), **LB\_ERRSPACE** (for a list box), or **CB\_ERRSPACE** (for a combo box) if insufficient space is available to set the text in the edit control.</span></span> <span data-ttu-id="05dce-114">Il est **CB \_ Err** si ce message est envoyé à une zone de liste déroulante sans contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="05dce-114">It is **CB\_ERR** if this message is sent to a combo box without an edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="05dce-115">Notes</span><span class="sxs-lookup"><span data-stu-id="05dce-115">Remarks</span></span>

<span data-ttu-id="05dce-116">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) définit et affiche le texte de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="05dce-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets and displays the window text.</span></span> <span data-ttu-id="05dce-117">Pour un contrôle d’édition, le texte est le contenu du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="05dce-117">For an edit control, the text is the contents of the edit control.</span></span> <span data-ttu-id="05dce-118">Pour une zone de liste modifiable, le texte est le contenu de la partie de contrôle de modification de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="05dce-118">For a combo box, the text is the contents of the edit-control portion of the combo box.</span></span> <span data-ttu-id="05dce-119">Pour un bouton, le texte est le nom du bouton.</span><span class="sxs-lookup"><span data-stu-id="05dce-119">For a button, the text is the button name.</span></span> <span data-ttu-id="05dce-120">Pour les autres fenêtres, le texte est le titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="05dce-120">For other windows, the text is the window title.</span></span>

<span data-ttu-id="05dce-121">Ce message ne modifie pas la sélection actuelle dans la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="05dce-121">This message does not change the current selection in the list box of a combo box.</span></span> <span data-ttu-id="05dce-122">Une application doit utiliser le message [**CB \_ SELECTSTRING**](../controls/cb-selectstring.md) pour sélectionner l’élément dans une zone de liste qui correspond au texte du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="05dce-122">An application should use the [**CB\_SELECTSTRING**](../controls/cb-selectstring.md) message to select the item in a list box that matches the text in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="05dce-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05dce-123">Requirements</span></span>



| <span data-ttu-id="05dce-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05dce-124">Requirement</span></span> | <span data-ttu-id="05dce-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="05dce-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05dce-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05dce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="05dce-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05dce-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="05dce-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05dce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="05dce-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05dce-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05dce-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="05dce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="05dce-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05dce-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05dce-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05dce-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="05dce-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="05dce-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05dce-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="05dce-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="05dce-135">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="05dce-135">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="05dce-136">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="05dce-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05dce-137">Windows</span><span class="sxs-lookup"><span data-stu-id="05dce-137">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="05dce-138">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="05dce-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="05dce-139">**\_SELECTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="05dce-139">**CB\_SELECTSTRING**</span></span>](../controls/cb-selectstring.md)
</dt> </dl>

 

 
