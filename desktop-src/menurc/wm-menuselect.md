---
title: Message WM_MENUSELECT (winuser. h)
description: Envoyé à la fenêtre propriétaire d’un menu lorsque l’utilisateur sélectionne un élément de menu.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514259"
---
# <a name="wm_menuselect-message"></a><span data-ttu-id="713db-104">\_Message WM MENUSELECT</span><span class="sxs-lookup"><span data-stu-id="713db-104">WM\_MENUSELECT message</span></span>

<span data-ttu-id="713db-105">Envoyé à la fenêtre propriétaire d’un menu lorsque l’utilisateur sélectionne un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="713db-105">Sent to a menu's owner window when the user selects a menu item.</span></span>


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a><span data-ttu-id="713db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="713db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="713db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="713db-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="713db-108">Le mot de poids faible spécifie l’index de l’élément de menu ou du sous-menu.</span><span class="sxs-lookup"><span data-stu-id="713db-108">The low-order word specifies the menu item or submenu index.</span></span> <span data-ttu-id="713db-109">Si l’élément sélectionné est un élément de commande, ce paramètre contient l’identificateur de l’élément de menu.</span><span class="sxs-lookup"><span data-stu-id="713db-109">If the selected item is a command item, this parameter contains the identifier of the menu item.</span></span> <span data-ttu-id="713db-110">Si l’élément sélectionné ouvre un menu déroulant ou un sous-menu, ce paramètre contient l’index du menu déroulant ou du sous-menu du menu principal, et le paramètre *lParam* contient le handle du menu principal (clic). Utilisez la fonction [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) pour récupérer la poignée de menu du menu déroulant ou du sous-menu.</span><span class="sxs-lookup"><span data-stu-id="713db-110">If the selected item opens a drop-down menu or submenu, this parameter contains the index of the drop-down menu or submenu in the main menu, and the *lParam* parameter contains the handle to the main (clicked) menu; use the [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) function to get the menu handle to the drop-down menu or submenu.</span></span>

<span data-ttu-id="713db-111">Le mot de poids fort spécifie un ou plusieurs indicateurs de menu.</span><span class="sxs-lookup"><span data-stu-id="713db-111">The high-order word specifies one or more menu flags.</span></span> <span data-ttu-id="713db-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="713db-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="713db-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="713db-113">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="713db-114">Signification</span><span class="sxs-lookup"><span data-stu-id="713db-114">Meaning</span></span>                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <span data-ttu-id="713db-115"><dt>**MF \_**</dt> <dt>0x00000004L</dt> bitmap</span><span class="sxs-lookup"><span data-stu-id="713db-115"><dt>**MF\_BITMAP**</dt> <dt>0x00000004L</dt></span></span> </dl>                | <span data-ttu-id="713db-116">Item affiche une bitmap.</span><span class="sxs-lookup"><span data-stu-id="713db-116">Item displays a bitmap.</span></span><br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <span data-ttu-id="713db-117"><dt>**MF \_**</dt> <dt>0x00000008L</dt> activé</span><span class="sxs-lookup"><span data-stu-id="713db-117"><dt>**MF\_CHECKED**</dt> <dt>0x00000008L</dt></span></span> </dl>             | <span data-ttu-id="713db-118">L’élément est activé.</span><span class="sxs-lookup"><span data-stu-id="713db-118">Item is checked.</span></span><br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <span data-ttu-id="713db-119"><dt>**MF \_ Désactivation**</dt> de <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="713db-119"><dt>**MF\_DISABLED**</dt> <dt>0x00000002L</dt></span></span> </dl>          | <span data-ttu-id="713db-120">L'élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="713db-120">Item is disabled.</span></span><br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <span data-ttu-id="713db-121"><dt>**MF \_ 0x00000001L GRISés**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="713db-121"><dt>**MF\_GRAYED**</dt> <dt>0x00000001L</dt></span></span> </dl>                | <span data-ttu-id="713db-122">L’élément est grisé.</span><span class="sxs-lookup"><span data-stu-id="713db-122">Item is grayed.</span></span><br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <span data-ttu-id="713db-123"><dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt></span><span class="sxs-lookup"><span data-stu-id="713db-123"><dt>**MF\_HILITE**</dt> <dt>0x00000080L</dt></span></span> </dl>                | <span data-ttu-id="713db-124">L’élément est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="713db-124">Item is highlighted.</span></span><br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <span data-ttu-id="713db-125"><dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt></span><span class="sxs-lookup"><span data-stu-id="713db-125"><dt>**MF\_MOUSESELECT**</dt> <dt>0x00008000L</dt></span></span> </dl> | <span data-ttu-id="713db-126">L’élément est sélectionné avec la souris.</span><span class="sxs-lookup"><span data-stu-id="713db-126">Item is selected with the mouse.</span></span><br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <span data-ttu-id="713db-127"><dt>**MF \_ OWNERDRAW**</dt> <dt>0x00000100L</dt></span><span class="sxs-lookup"><span data-stu-id="713db-127"><dt>**MF\_OWNERDRAW**</dt> <dt>0x00000100L</dt></span></span> </dl>       | <span data-ttu-id="713db-128">L’élément est un élément owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="713db-128">Item is an owner-drawn item.</span></span><br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="713db-129"><dt>**MF \_**</dt> <dt>0x00000010L</dt> Popup</span><span class="sxs-lookup"><span data-stu-id="713db-129"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>                   | <span data-ttu-id="713db-130">Élément ouvre un menu déroulant ou un sous-menu.</span><span class="sxs-lookup"><span data-stu-id="713db-130">Item opens a drop-down menu or submenu.</span></span><br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="713db-131"><dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="713db-131"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl>             | <span data-ttu-id="713db-132">L’élément est contenu dans le menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="713db-132">Item is contained in the window menu.</span></span> <span data-ttu-id="713db-133">Le paramètre *lParam* contient un handle vers le menu associé au message.</span><span class="sxs-lookup"><span data-stu-id="713db-133">The *lParam* parameter contains a handle to the menu associated with the message.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="713db-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="713db-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="713db-135">Handle vers le menu sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="713db-135">A handle to the menu that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="713db-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="713db-136">Return value</span></span>

<span data-ttu-id="713db-137">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="713db-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="713db-138">Notes</span><span class="sxs-lookup"><span data-stu-id="713db-138">Remarks</span></span>

<span data-ttu-id="713db-139">Si le mot de poids fort de *wParam* contient 0xFFFF et que le paramètre *lParam* contient la **valeur null**, le système a fermé le menu.</span><span class="sxs-lookup"><span data-stu-id="713db-139">If the high-order word of *wParam* contains 0xFFFF and the *lParam* parameter contains **NULL**, the system has closed the menu.</span></span>

<span data-ttu-id="713db-140">N’utilisez pas la valeur 1 pour le mot de poids fort de *wParam*, car cette valeur est spécifiée sous la forme (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span><span class="sxs-lookup"><span data-stu-id="713db-140">Do not use the value  1 for the high-order word of *wParam*, because this value is specified as (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span></span> <span data-ttu-id="713db-141">Si la valeur est 0xFFFF, elle est interprétée comme 0x0000FFFF, et non pas par 1, en raison de la conversion en **uint**.</span><span class="sxs-lookup"><span data-stu-id="713db-141">If the value is 0xFFFF, it would be interpreted as 0x0000FFFF, not  1, because of the cast to a **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="713db-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="713db-142">Requirements</span></span>



| <span data-ttu-id="713db-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="713db-143">Requirement</span></span> | <span data-ttu-id="713db-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="713db-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="713db-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="713db-145">Minimum supported client</span></span><br/> | <span data-ttu-id="713db-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="713db-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="713db-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="713db-147">Minimum supported server</span></span><br/> | <span data-ttu-id="713db-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="713db-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="713db-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="713db-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="713db-150"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="713db-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="713db-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="713db-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="713db-152">**Référence**</span><span class="sxs-lookup"><span data-stu-id="713db-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="713db-153">**GetSubMenu**</span><span class="sxs-lookup"><span data-stu-id="713db-153">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

<span data-ttu-id="713db-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="713db-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="713db-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="713db-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="713db-156">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="713db-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="713db-157">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="713db-157">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

