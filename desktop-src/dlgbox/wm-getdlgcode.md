---
title: Message WM_GETDLGCODE (winuser. h)
description: Envoyé à la procédure de fenêtre associée à un contrôle.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Boîtes de dialogue de WM_GETDLGCODE message
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512592"
---
# <a name="wm_getdlgcode-message"></a><span data-ttu-id="5446d-104">\_Message WM GETDLGCODE</span><span class="sxs-lookup"><span data-stu-id="5446d-104">WM\_GETDLGCODE message</span></span>

<span data-ttu-id="5446d-105">Envoyé à la procédure de fenêtre associée à un contrôle.</span><span class="sxs-lookup"><span data-stu-id="5446d-105">Sent to the window procedure associated with a control.</span></span> <span data-ttu-id="5446d-106">Par défaut, le système gère toutes les entrées au clavier du contrôle. le système interprète certains types d’entrée au clavier comme des touches de navigation de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5446d-106">By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys.</span></span> <span data-ttu-id="5446d-107">Pour remplacer ce comportement par défaut, le contrôle peut répondre au message **WM \_ GETDLGCODE** pour indiquer les types d’entrée qu’il souhaite traiter lui-même.</span><span class="sxs-lookup"><span data-stu-id="5446d-107">To override this default behavior, the control can respond to the **WM\_GETDLGCODE** message to indicate the types of input it wants to process itself.</span></span>


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a><span data-ttu-id="5446d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5446d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5446d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5446d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5446d-110">Touche virtuelle, appuyée par l’utilisateur, qui invite Windows à émettre cette notification.</span><span class="sxs-lookup"><span data-stu-id="5446d-110">The virtual key, pressed by the user, that prompted Windows to issue this notification.</span></span> <span data-ttu-id="5446d-111">Le gestionnaire doit gérer ces clés de manière sélective.</span><span class="sxs-lookup"><span data-stu-id="5446d-111">The handler must selectively handle these keys.</span></span> <span data-ttu-id="5446d-112">Par exemple, le gestionnaire peut accepter et traiter **le \_ retour VK** mais **l' \_ onglet VK** délégué à la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="5446d-112">For instance, the handler might accept and process **VK\_RETURN** but delegate **VK\_TAB** to the owner window.</span></span> <span data-ttu-id="5446d-113">Pour obtenir la liste des valeurs, consultez [**la section codes de clé virtuelle**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="5446d-113">For a list of values, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="5446d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5446d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5446d-115">Pointeur vers une structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) (ou **null** si le système exécute une requête).</span><span class="sxs-lookup"><span data-stu-id="5446d-115">A pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure (or **NULL** if the system is performing a query).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5446d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5446d-116">Return value</span></span>

<span data-ttu-id="5446d-117">La valeur de retour est une ou plusieurs des valeurs suivantes, indiquant le type d’entrée traité par l’application.</span><span class="sxs-lookup"><span data-stu-id="5446d-117">The return value is one or more of the following values, indicating which type of input the application processes.</span></span>



| <span data-ttu-id="5446d-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5446d-118">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="5446d-119">Description</span><span class="sxs-lookup"><span data-stu-id="5446d-119">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5446d-120"><dt>**DLGC \_ BOUTON**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-120"><dt>**DLGC\_BUTTON**</dt> <dt>0x2000</dt></span></span> </dl>          | <span data-ttu-id="5446d-121">Bouton.</span><span class="sxs-lookup"><span data-stu-id="5446d-121">Button.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="5446d-122"><dt>**DLGC \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-122"><dt>**DLGC\_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>   | <span data-ttu-id="5446d-123">Bouton de commande par défaut.</span><span class="sxs-lookup"><span data-stu-id="5446d-123">Default push button.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="5446d-124"><dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-124"><dt>**DLGC\_HASSETSEL**</dt> <dt>0x0008</dt></span></span> </dl>       | <span data-ttu-id="5446d-125">[**Em \_ Messages SETSEL**](/windows/desktop/Controls/em-setsel) .</span><span class="sxs-lookup"><span data-stu-id="5446d-125">[**EM\_SETSEL**](/windows/desktop/Controls/em-setsel) messages.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="5446d-126"><dt>**DLGC \_ RadioButton**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-126"><dt>**DLGC\_RADIOBUTTON**</dt> <dt>0x0040</dt></span></span> </dl>     | <span data-ttu-id="5446d-127">Case d’option.</span><span class="sxs-lookup"><span data-stu-id="5446d-127">Radio button.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="5446d-128"><dt>**DLGC \_**</dt> <dt>0x0100</dt> statique</span><span class="sxs-lookup"><span data-stu-id="5446d-128"><dt>**DLGC\_STATIC**</dt> <dt>0x0100</dt></span></span> </dl>          | <span data-ttu-id="5446d-129">Contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="5446d-129">Static control.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="5446d-130"><dt>**DLGC \_ UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-130"><dt>**DLGC\_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="5446d-131">Bouton de commande non défini par défaut.</span><span class="sxs-lookup"><span data-stu-id="5446d-131">Non-default push button.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="5446d-132"><dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-132"><dt>**DLGC\_WANTALLKEYS**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="5446d-133">Toutes les entrées au clavier.</span><span class="sxs-lookup"><span data-stu-id="5446d-133">All keyboard input.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="5446d-134"><dt>**DLGC \_ WANTARROWS**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-134"><dt>**DLGC\_WANTARROWS**</dt> <dt>0x0001</dt></span></span> </dl>      | <span data-ttu-id="5446d-135">Touches de direction.</span><span class="sxs-lookup"><span data-stu-id="5446d-135">Direction keys.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="5446d-136"><dt>**DLGC \_ WANTCHARS**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-136"><dt>**DLGC\_WANTCHARS**</dt> <dt>0x0080</dt></span></span> </dl>       | <span data-ttu-id="5446d-137">[**WM \_ Messages de type CHAR**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="5446d-137">[**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="5446d-138"><dt>**DLGC \_ WANTMESSAGE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-138"><dt>**DLGC\_WANTMESSAGE**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="5446d-139">Toutes les entrées au clavier (l’application transmet ce message dans la structure [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) au contrôle).</span><span class="sxs-lookup"><span data-stu-id="5446d-139">All keyboard input (the application passes this message in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure to the control).</span></span><br/> |
| <dl> <span data-ttu-id="5446d-140"><dt>**DLGC \_ WANTTAB**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-140"><dt>**DLGC\_WANTTAB**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="5446d-141">Touche TAB.</span><span class="sxs-lookup"><span data-stu-id="5446d-141">TAB key.</span></span><br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="5446d-142">Notes</span><span class="sxs-lookup"><span data-stu-id="5446d-142">Remarks</span></span>

<span data-ttu-id="5446d-143">Bien que la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne toujours la valeur zéro en réponse au message **WM \_ GETDLGCODE** , la procédure de fenêtre pour les classes de contrôle prédéfinies retourne un code approprié pour chaque classe.</span><span class="sxs-lookup"><span data-stu-id="5446d-143">Although the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function always returns zero in response to the **WM\_GETDLGCODE** message, the window procedure for the predefined control classes return a code appropriate for each class.</span></span>

<span data-ttu-id="5446d-144">Le message **WM \_ GETDLGCODE** et les valeurs retournées sont utiles uniquement avec les contrôles de boîte de dialogue définis par l’utilisateur ou les contrôles standard modifiés par le sous-classement.</span><span class="sxs-lookup"><span data-stu-id="5446d-144">The **WM\_GETDLGCODE** message and the returned values are useful only with user-defined dialog box controls or standard controls modified by subclassing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5446d-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5446d-145">Requirements</span></span>



| <span data-ttu-id="5446d-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5446d-146">Requirement</span></span> | <span data-ttu-id="5446d-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="5446d-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5446d-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5446d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5446d-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5446d-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5446d-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5446d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5446d-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5446d-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5446d-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="5446d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="5446d-153"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5446d-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5446d-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5446d-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="5446d-155">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5446d-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5446d-156">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5446d-156">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5446d-157">**\_SETSEL em**</span><span class="sxs-lookup"><span data-stu-id="5446d-157">**EM\_SETSEL**</span></span>](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[<span data-ttu-id="5446d-158">**FRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="5446d-158">**MSG**</span></span>](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[<span data-ttu-id="5446d-159">**\_caractère WM**</span><span class="sxs-lookup"><span data-stu-id="5446d-159">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> <dt>

<span data-ttu-id="5446d-160">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5446d-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5446d-161">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="5446d-161">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

