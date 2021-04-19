---
title: Message WM_COMMAND (winuser. h)
description: Envoyé lorsque l’utilisateur sélectionne un élément de commande dans un menu, lorsqu’un contrôle envoie un message de notification à sa fenêtre parente, ou lorsqu’une touche d’accès rapide est traduite.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535298"
---
# <a name="wm_command-message"></a><span data-ttu-id="fac56-104">\_Message de commande WM</span><span class="sxs-lookup"><span data-stu-id="fac56-104">WM\_COMMAND message</span></span>

<span data-ttu-id="fac56-105">Envoyé lorsque l’utilisateur sélectionne un élément de commande dans un menu, lorsqu’un contrôle envoie un message de notification à sa fenêtre parente, ou lorsqu’une touche d’accès rapide est traduite.</span><span class="sxs-lookup"><span data-stu-id="fac56-105">Sent when the user selects a command item from a menu, when a control sends a notification message to its parent window, or when an accelerator keystroke is translated.</span></span>


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a><span data-ttu-id="fac56-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fac56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac56-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fac56-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fac56-108">Pour obtenir une description de ce paramètre, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fac56-108">For a description of this parameter, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fac56-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fac56-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fac56-110">Pour obtenir une description de ce paramètre, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fac56-110">For a description of this parameter, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac56-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fac56-111">Return value</span></span>

<span data-ttu-id="fac56-112">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="fac56-112">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="fac56-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="fac56-113">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="fac56-114">Exemple tiré des [exemples Windows classiques](https://github.com/microsoft/Windows-classic-samples) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="fac56-114">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="fac56-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fac56-115">Remarks</span></span>

<span data-ttu-id="fac56-116">L’utilisation des paramètres *wParam* et *lParam* est résumée ici.</span><span class="sxs-lookup"><span data-stu-id="fac56-116">Use of the *wParam* and *lParam* parameters are summarized here.</span></span>



| <span data-ttu-id="fac56-117">Source du message</span><span class="sxs-lookup"><span data-stu-id="fac56-117">Message Source</span></span> | <span data-ttu-id="fac56-118">wParam (mot élevé)</span><span class="sxs-lookup"><span data-stu-id="fac56-118">wParam (high word)</span></span>                | <span data-ttu-id="fac56-119">wParam (mot bas)</span><span class="sxs-lookup"><span data-stu-id="fac56-119">wParam (low word)</span></span>                | <span data-ttu-id="fac56-120">lParam</span><span class="sxs-lookup"><span data-stu-id="fac56-120">lParam</span></span>                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| <span data-ttu-id="fac56-121">Menu</span><span class="sxs-lookup"><span data-stu-id="fac56-121">Menu</span></span>           | <span data-ttu-id="fac56-122">0</span><span class="sxs-lookup"><span data-stu-id="fac56-122">0</span></span>                                 | <span data-ttu-id="fac56-123">Identificateur de menu (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="fac56-123">Menu identifier (IDM\_\*)</span></span>        | <span data-ttu-id="fac56-124">0</span><span class="sxs-lookup"><span data-stu-id="fac56-124">0</span></span>                            |
| <span data-ttu-id="fac56-125">Accélérateur</span><span class="sxs-lookup"><span data-stu-id="fac56-125">Accelerator</span></span>    | <span data-ttu-id="fac56-126">1</span><span class="sxs-lookup"><span data-stu-id="fac56-126">1</span></span>                                 | <span data-ttu-id="fac56-127">Identificateur d’accélérateur (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="fac56-127">Accelerator identifier (IDM\_\*)</span></span> | <span data-ttu-id="fac56-128">0</span><span class="sxs-lookup"><span data-stu-id="fac56-128">0</span></span>                            |
| <span data-ttu-id="fac56-129">Contrôler</span><span class="sxs-lookup"><span data-stu-id="fac56-129">Control</span></span>        | <span data-ttu-id="fac56-130">Code de notification défini par le contrôle</span><span class="sxs-lookup"><span data-stu-id="fac56-130">Control-defined notification code</span></span> | <span data-ttu-id="fac56-131">Identificateur de contrôle</span><span class="sxs-lookup"><span data-stu-id="fac56-131">Control identifier</span></span>               | <span data-ttu-id="fac56-132">Handle vers la fenêtre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fac56-132">Handle to the control window</span></span> |



 

### <a name="menus"></a><span data-ttu-id="fac56-133">Menus</span><span class="sxs-lookup"><span data-stu-id="fac56-133">Menus</span></span>

<span data-ttu-id="fac56-134">Si une application active un séparateur de menu, le système envoie un message de **\_ commande WM** avec le mot de poids faible du paramètre *wParam* défini sur zéro lorsque l’utilisateur sélectionne le séparateur.</span><span class="sxs-lookup"><span data-stu-id="fac56-134">If an application enables a menu separator, the system sends a **WM\_COMMAND** message with the low-word of the *wParam* parameter set to zero when the user selects the separator.</span></span>

<span data-ttu-id="fac56-135">Si un menu est défini avec une valeur [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) de **MNS \_ NOTIFYBYPOS**, [**WM \_ MENUCOMMAND**](wm-menucommand.md) est envoyé à la place de la **\_ commande WM**.</span><span class="sxs-lookup"><span data-stu-id="fac56-135">If a menu is defined with a [**MENUINFO.dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) value of **MNS\_NOTIFYBYPOS**, [**WM\_MENUCOMMAND**](wm-menucommand.md) is sent instead of **WM\_COMMAND**.</span></span>

### <a name="accelerators"></a><span data-ttu-id="fac56-136">Accélérateurs</span><span class="sxs-lookup"><span data-stu-id="fac56-136">Accelerators</span></span>

<span data-ttu-id="fac56-137">Les séquences de touches d’accélérateur qui sélectionnent des éléments dans le menu fenêtre sont traduites en messages [**WM \_ SYSCOMMAND**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="fac56-137">Accelerator keystrokes that select items from the window menu are translated into [**WM\_SYSCOMMAND**](wm-syscommand.md) messages.</span></span>

<span data-ttu-id="fac56-138">Si une touche d’accès rapide qui correspond à un élément de menu se produit lorsque la fenêtre qui possède le menu est réduite, aucun message de **\_ commande WM** n’est envoyé.</span><span class="sxs-lookup"><span data-stu-id="fac56-138">If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, no **WM\_COMMAND** message is sent.</span></span> <span data-ttu-id="fac56-139">Toutefois, si une frappe de touche d’accès rapide ne correspond à aucun des éléments du menu de la fenêtre ou du menu fenêtre, un message de **\_ commande WM** est envoyé, même si la fenêtre est réduite.</span><span class="sxs-lookup"><span data-stu-id="fac56-139">However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the window menu, a **WM\_COMMAND** message is sent, even if the window is minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac56-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fac56-140">Requirements</span></span>



| <span data-ttu-id="fac56-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fac56-141">Requirement</span></span> | <span data-ttu-id="fac56-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="fac56-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac56-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fac56-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fac56-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fac56-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fac56-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fac56-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fac56-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fac56-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fac56-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="fac56-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="fac56-148"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fac56-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac56-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fac56-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="fac56-150">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fac56-150">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="fac56-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fac56-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fac56-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fac56-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fac56-153">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fac56-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fac56-154">Menus</span><span class="sxs-lookup"><span data-stu-id="fac56-154">Menus</span></span>](menus.md)
</dt> </dl>

 

