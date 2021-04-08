---
title: Message WM_SETHOTKEY (winuser. h)
description: Envoyé à une fenêtre pour associer une touche d’accès rapide à la fenêtre. Quand l’utilisateur appuie sur la touche d’accès rapide, le système active la fenêtre.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "103761515"
---
# <a name="wm_sethotkey-message"></a><span data-ttu-id="f8c1f-105">\_Message WM SETHOTKEY</span><span class="sxs-lookup"><span data-stu-id="f8c1f-105">WM\_SETHOTKEY message</span></span>

<span data-ttu-id="f8c1f-106">Envoyé à une fenêtre pour associer une touche d’accès rapide à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-106">Sent to a window to associate a hot key with the window.</span></span> <span data-ttu-id="f8c1f-107">Quand l’utilisateur appuie sur la touche d’accès rapide, le système active la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-107">When the user presses the hot key, the system activates the window.</span></span>


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a><span data-ttu-id="f8c1f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8c1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8c1f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c1f-110">Le mot de poids faible spécifie le code de la touche virtuelle à associer à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-110">The low-order word specifies the virtual-key code to associate with the window.</span></span>

<span data-ttu-id="f8c1f-111">Le mot de poids fort peut être une ou plusieurs des valeurs suivantes à partir de CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-111">The high-order word can be one or more of the following values from CommCtrl.h.</span></span>

<span data-ttu-id="f8c1f-112">Le fait de définir *wParam* sur **null** supprime la touche d’accès rapide associée à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-112">Setting *wParam* to **NULL** removes the hot key associated with a window.</span></span>



| <span data-ttu-id="f8c1f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8c1f-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="f8c1f-114">Signification</span><span class="sxs-lookup"><span data-stu-id="f8c1f-114">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <span data-ttu-id="f8c1f-115"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-115"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>             | <span data-ttu-id="f8c1f-116">touche ALT</span><span class="sxs-lookup"><span data-stu-id="f8c1f-116">ALT key</span></span><br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <span data-ttu-id="f8c1f-117"><dt>**HOTKEYF \_ CONTRÔLE**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-117"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="f8c1f-118">Touche CTRL</span><span class="sxs-lookup"><span data-stu-id="f8c1f-118">CTRL key</span></span><br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <span data-ttu-id="f8c1f-119"><dt>**HOTKEYF \_**</dt> <dt>0x08</dt> de l’ext.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-119"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="f8c1f-120">Clé étendue</span><span class="sxs-lookup"><span data-stu-id="f8c1f-120">Extended key</span></span><br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <span data-ttu-id="f8c1f-121"><dt>**HOTKEYF \_ DÉCALAGE**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-121"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>       | <span data-ttu-id="f8c1f-122">Touche Maj</span><span class="sxs-lookup"><span data-stu-id="f8c1f-122">SHIFT key</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="f8c1f-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8c1f-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8c1f-124">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-124">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c1f-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8c1f-125">Return value</span></span>

<span data-ttu-id="f8c1f-126">La valeur de retour est l’une des suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-126">The return value is one of the following.</span></span>



| <span data-ttu-id="f8c1f-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8c1f-127">Return value</span></span>                                                                  | <span data-ttu-id="f8c1f-128">Description</span><span class="sxs-lookup"><span data-stu-id="f8c1f-128">Description</span></span>                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8c1f-129"><dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-129"><dt>-1</dt></span></span> </dl> | <span data-ttu-id="f8c1f-130">La fonction échoue ; la touche d’accès rapide n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-130">The function is unsuccessful; the hot key is invalid.</span></span><br/>                        |
| <dl> <span data-ttu-id="f8c1f-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-131"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="f8c1f-132">La fonction échoue ; la fenêtre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-132">The function is unsuccessful; the window is invalid.</span></span><br/>                         |
| <dl> <span data-ttu-id="f8c1f-133"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-133"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="f8c1f-134">La fonction est réussie et aucune autre fenêtre n’a la même touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-134">The function is successful, and no other window has the same hot key.</span></span><br/>        |
| <dl> <span data-ttu-id="f8c1f-135"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-135"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="f8c1f-136">La fonction réussit, mais une autre fenêtre a déjà la même touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-136">The function is successful, but another window already has the same hot key.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8c1f-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f8c1f-137">Remarks</span></span>

<span data-ttu-id="f8c1f-138">Une touche d’accès rapide ne peut pas être associée à une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-138">A hot key cannot be associated with a child window.</span></span>

<span data-ttu-id="f8c1f-139">**VK \_** Les touches d’accès rapide, d' **\_ espace de VK** et de **VK \_** sont des touches d’accès non valides.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-139">**VK\_ESCAPE**, **VK\_SPACE**, and **VK\_TAB** are invalid hot keys.</span></span>

<span data-ttu-id="f8c1f-140">Quand l’utilisateur appuie sur la touche d’accès rapide, le système génère un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) avec *wParam* égal à **SC \_ Hotkey** et *lParam* égal au handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-140">When the user presses the hot key, the system generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message with *wParam* equal to **SC\_HOTKEY** and *lParam* equal to the window's handle.</span></span> <span data-ttu-id="f8c1f-141">Si ce message est transmis à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), le système affiche la dernière fenêtre active de la fenêtre (si elle existe) ou la fenêtre elle-même (s’il n’y a pas de fenêtre contextuelle) au premier plan.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-141">If this message is passed on to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the system will bring the window's last active popup (if it exists) or the window itself (if there is no popup window) to the foreground.</span></span>

<span data-ttu-id="f8c1f-142">Une fenêtre ne peut avoir qu’une seule touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-142">A window can only have one hot key.</span></span> <span data-ttu-id="f8c1f-143">Si la fenêtre est déjà associée à une touche d’accès rapide, la nouvelle touche d’accès rapide remplace l’ancienne.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-143">If the window already has a hot key associated with it, the new hot key replaces the old one.</span></span> <span data-ttu-id="f8c1f-144">Si plusieurs fenêtres possèdent la même touche d’accès rapide, la fenêtre qui est activée par la touche d’accès rapide est aléatoire.</span><span class="sxs-lookup"><span data-stu-id="f8c1f-144">If more than one window has the same hot key, the window that is activated by the hot key is random.</span></span>

<span data-ttu-id="f8c1f-145">Ces touches d’accès rapide ne sont pas liées aux touches d’accès rapide définies par [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span><span class="sxs-lookup"><span data-stu-id="f8c1f-145">These hot keys are unrelated to the hot keys set by [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c1f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8c1f-146">Requirements</span></span>



| <span data-ttu-id="f8c1f-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8c1f-147">Requirement</span></span> | <span data-ttu-id="f8c1f-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8c1f-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c1f-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8c1f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c1f-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8c1f-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f8c1f-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8c1f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c1f-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8c1f-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8c1f-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8c1f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8c1f-154"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8c1f-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8c1f-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c1f-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8c1f-156">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f8c1f-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8c1f-157">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="f8c1f-157">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="f8c1f-158">**\_GETHOTKEY WM**</span><span class="sxs-lookup"><span data-stu-id="f8c1f-158">**WM\_GETHOTKEY**</span></span>](wm-gethotkey.md)
</dt> <dt>

[<span data-ttu-id="f8c1f-159">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="f8c1f-159">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="f8c1f-160">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f8c1f-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8c1f-161">Entrée au clavier</span><span class="sxs-lookup"><span data-stu-id="f8c1f-161">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

