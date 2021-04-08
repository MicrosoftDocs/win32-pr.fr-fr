---
title: Message WM_MENUCHAR (winuser. h)
description: Envoyé lorsqu’un menu est actif et que l’utilisateur appuie sur une touche qui ne correspond à aucun mnémonique ou touche d’accès rapide. Ce message est envoyé à la fenêtre qui possède le menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743829"
---
# <a name="wm_menuchar-message"></a><span data-ttu-id="9066b-105">\_Message WM MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="9066b-105">WM\_MENUCHAR message</span></span>

<span data-ttu-id="9066b-106">Envoyé lorsqu’un menu est actif et que l’utilisateur appuie sur une touche qui ne correspond à aucun mnémonique ou touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="9066b-106">Sent when a menu is active and the user presses a key that does not correspond to any mnemonic or accelerator key.</span></span> <span data-ttu-id="9066b-107">Ce message est envoyé à la fenêtre qui possède le menu.</span><span class="sxs-lookup"><span data-stu-id="9066b-107">This message is sent to the window that owns the menu.</span></span>


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a><span data-ttu-id="9066b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9066b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9066b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9066b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9066b-110">Le mot de poids faible spécifie le code de caractère qui correspond à la touche sur laquelle l’utilisateur a appuyé.</span><span class="sxs-lookup"><span data-stu-id="9066b-110">The low-order word specifies the character code that corresponds to the key the user pressed.</span></span>

<span data-ttu-id="9066b-111">Le mot de poids fort spécifie le type de menu actif.</span><span class="sxs-lookup"><span data-stu-id="9066b-111">The high-order word specifies the active menu type.</span></span> <span data-ttu-id="9066b-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9066b-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9066b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="9066b-113">Value</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="9066b-114">Signification</span><span class="sxs-lookup"><span data-stu-id="9066b-114">Meaning</span></span>                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="9066b-115"><dt>**MF \_**</dt> <dt>0x00000010L</dt> Popup</span><span class="sxs-lookup"><span data-stu-id="9066b-115"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>       | <span data-ttu-id="9066b-116">Menu déroulant, sous-menu ou menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="9066b-116">A drop-down menu, submenu, or shortcut menu.</span></span><br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="9066b-117"><dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="9066b-117"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl> | <span data-ttu-id="9066b-118">Menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9066b-118">The window menu.</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="9066b-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9066b-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9066b-120">Handle vers le menu actif.</span><span class="sxs-lookup"><span data-stu-id="9066b-120">A handle to the active menu.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9066b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9066b-121">Return value</span></span>

<span data-ttu-id="9066b-122">Une application qui traite ce message doit retourner l’une des valeurs suivantes dans le mot de poids fort de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9066b-122">An application that processes this message should return one of the following values in the high-order word of the return value.</span></span>



| <span data-ttu-id="9066b-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9066b-123">Return code/value</span></span>                                                                                                                                  | <span data-ttu-id="9066b-124">Description</span><span class="sxs-lookup"><span data-stu-id="9066b-124">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9066b-125"><dt>**MNC \_ FERMER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9066b-125"><dt>**MNC\_CLOSE**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="9066b-126">Informe le système qu’il doit fermer le menu actif.</span><span class="sxs-lookup"><span data-stu-id="9066b-126">Informs the system that it should close the active menu.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="9066b-127"><dt>**MNC \_ EXÉCUTER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9066b-127"><dt>**MNC\_EXECUTE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="9066b-128">Informe le système qu’il doit choisir l’élément spécifié dans le mot de poids faible de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9066b-128">Informs the system that it should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="9066b-129">La fenêtre propriétaire reçoit un message de [**\_ commande WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="9066b-129">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span><br/> |
| <dl> <span data-ttu-id="9066b-130"><dt>**MNC \_ IGNORER**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9066b-130"><dt>**MNC\_IGNORE**</dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="9066b-131">Informe le système qu’il doit ignorer le caractère que l’utilisateur a appuyé et créer un bref signal sonore sur le haut-parleur du système.</span><span class="sxs-lookup"><span data-stu-id="9066b-131">Informs the system that it should discard the character the user pressed and create a short beep on the system speaker.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="9066b-132"><dt>**MNC \_ SÉLECTIONNER**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9066b-132"><dt>**MNC\_SELECT**</dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="9066b-133">Informe le système qu’il doit sélectionner l’élément spécifié dans le mot de poids faible de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9066b-133">Informs the system that it should select the item specified in the low-order word of the return value.</span></span> <br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="9066b-134">Notes</span><span class="sxs-lookup"><span data-stu-id="9066b-134">Remarks</span></span>

<span data-ttu-id="9066b-135">Le mot de poids faible est ignoré si le mot de poids fort contient 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="9066b-135">The low-order word is ignored if the high-order word contains 0 or 1.</span></span>

<span data-ttu-id="9066b-136">Une application doit traiter ce message lorsqu’un accélérateur est utilisé pour sélectionner un élément de menu qui affiche une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="9066b-136">An application should process this message when an accelerator is used to select a menu item that displays a bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="9066b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9066b-137">Requirements</span></span>



| <span data-ttu-id="9066b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9066b-138">Requirement</span></span> | <span data-ttu-id="9066b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="9066b-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9066b-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9066b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9066b-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9066b-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9066b-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9066b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9066b-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9066b-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9066b-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="9066b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9066b-145"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9066b-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9066b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9066b-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="9066b-147">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9066b-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="9066b-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9066b-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9066b-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9066b-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9066b-150">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9066b-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9066b-151">Raccourcis clavier</span><span class="sxs-lookup"><span data-stu-id="9066b-151">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

