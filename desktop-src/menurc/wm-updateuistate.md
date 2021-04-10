---
title: Message WM_UPDATEUISTATE (winuser. h)
description: Une application envoie le \_ message WM UPDATEUISTATE pour modifier l’état de l’interface utilisateur pour la fenêtre spécifiée et toutes ses fenêtres enfants.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106453"
---
# <a name="wm_updateuistate-message"></a><span data-ttu-id="e1e5f-104">\_Message WM UPDATEUISTATE</span><span class="sxs-lookup"><span data-stu-id="e1e5f-104">WM\_UPDATEUISTATE message</span></span>

<span data-ttu-id="e1e5f-105">Une application envoie le message **WM \_ UPDATEUISTATE** pour modifier l’état de l’interface utilisateur pour la fenêtre spécifiée et toutes ses fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-105">An application sends the **WM\_UPDATEUISTATE** message to change the UI state for the specified window and all its child windows.</span></span>


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a><span data-ttu-id="e1e5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1e5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1e5f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1e5f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1e5f-108">Le mot de poids faible spécifie l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-108">The low-order word specifies the action to be performed.</span></span> <span data-ttu-id="e1e5f-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e1e5f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e5f-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="e1e5f-111">Signification</span><span class="sxs-lookup"><span data-stu-id="e1e5f-111">Meaning</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="e1e5f-112"><dt>**Interfaces utilisateur \_ EFFACER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1e5f-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="e1e5f-113">L’élément d’état d’interface utilisateur spécifié par le mot de poids fort doit être masqué.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-113">The UI state element specified by the high-order word should be hidden.</span></span><br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="e1e5f-114"><dt>**Interfaces utilisateur \_ INITIALiser**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e1e5f-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e1e5f-115">L’élément d’état d’interface utilisateur spécifié par le mot de poids fort doit être modifié en fonction du dernier événement d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-115">The UI state element specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="e1e5f-116">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="e1e5f-117"><dt>**Interfaces utilisateur \_ DÉFINIR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e1e5f-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="e1e5f-118">L’élément d’état d’interface utilisateur spécifié par le mot de poids fort doit être visible.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-118">The UI state element specified by the high-order word should be visible.</span></span><br/>                                                                  |



 

<span data-ttu-id="e1e5f-119">Le mot de poids fort spécifie les éléments d’état d’interface utilisateur qui sont affectés ou le style du contrôle.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="e1e5f-120">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e1e5f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e5f-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="e1e5f-122">Signification</span><span class="sxs-lookup"><span data-stu-id="e1e5f-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="e1e5f-123"><dt>**UISF \_**</dt> <dt>0x4</dt> actif</span><span class="sxs-lookup"><span data-stu-id="e1e5f-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="e1e5f-124">Un contrôle doit être dessiné dans le style utilisé pour les contrôles actifs.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="e1e5f-125"><dt>**UISF \_ HIDEACCEL**</dt> <dt>0X2</dt></span><span class="sxs-lookup"><span data-stu-id="e1e5f-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="e1e5f-126">Accélérateurs clavier.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-126">Keyboard accelerators.</span></span><br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="e1e5f-127"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="e1e5f-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="e1e5f-128">Indicateurs de focus.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-128">Focus indicators.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="e1e5f-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1e5f-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1e5f-130">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1e5f-131">Notes</span><span class="sxs-lookup"><span data-stu-id="e1e5f-131">Remarks</span></span>

<span data-ttu-id="e1e5f-132">Une fenêtre doit envoyer ce message pour modifier l’état de l’interface utilisateur de toutes ses fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-132">A window should send this message to change the UI state of all its child windows.</span></span> <span data-ttu-id="e1e5f-133">Contrairement au message [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) , qui est une notification, lorsque [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traite le message **WM \_ UPDATEUISTATE** , il modifie l’état de l’interface utilisateur et propage les modifications à toutes les fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-133">In contrast to the [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message, which is a notification, when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processes the **WM\_UPDATEUISTATE** message it changes the UI state and propagates the changes to all child windows.</span></span>

<span data-ttu-id="e1e5f-134">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) met à jour l’état de l’interface utilisateur en fonction de la valeur *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e1e5f-134">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function updates the UI state according to the *wParam* value.</span></span> <span data-ttu-id="e1e5f-135">Si l’état de l’interface utilisateur est modifié, la fonction envoie le message à toutes les fenêtres enfants immédiats.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-135">If the UI state is modified, the function sends the message to all the immediate child windows.</span></span> <span data-ttu-id="e1e5f-136">**DefWindowProc** envoie également ce message lorsqu’il reçoit un message [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) notifiant au système qu’une fenêtre enfant a l’intention de modifier l’état de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1e5f-136">**DefWindowProc** also sends this message when it receives a [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message notifying the system that a child window intends to modify the UI state.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1e5f-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1e5f-137">Requirements</span></span>



| <span data-ttu-id="e1e5f-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1e5f-138">Requirement</span></span> | <span data-ttu-id="e1e5f-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1e5f-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e5f-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e5f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e5f-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1e5f-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e1e5f-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1e5f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e5f-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1e5f-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e1e5f-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1e5f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1e5f-145"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1e5f-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1e5f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1e5f-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="e1e5f-147">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e1e5f-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e1e5f-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e1e5f-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e1e5f-149">**\_CHANGEUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="e1e5f-149">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="e1e5f-150">**\_QUERYUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="e1e5f-150">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="e1e5f-151">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e1e5f-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1e5f-152">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="e1e5f-152">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

