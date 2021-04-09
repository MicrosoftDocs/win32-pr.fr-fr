---
title: Message WM_CTLCOLORBTN (winuser. h)
description: Le \_ message WM CTLCOLORBTN est envoyé à la fenêtre parente d’un bouton avant de dessiner le bouton. La fenêtre parente peut modifier le texte du bouton et les couleurs d’arrière-plan. Toutefois, seuls les boutons owner-drawn répondent à la fenêtre parente qui traite ce message.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941657"
---
# <a name="wm_ctlcolorbtn-message"></a><span data-ttu-id="cef43-106">\_Message WM CTLCOLORBTN</span><span class="sxs-lookup"><span data-stu-id="cef43-106">WM\_CTLCOLORBTN message</span></span>

<span data-ttu-id="cef43-107">Le message **WM \_ CTLCOLORBTN** est envoyé à la fenêtre parente d’un bouton avant de dessiner le bouton.</span><span class="sxs-lookup"><span data-stu-id="cef43-107">The **WM\_CTLCOLORBTN** message is sent to the parent window of a button before drawing the button.</span></span> <span data-ttu-id="cef43-108">La fenêtre parente peut modifier le texte du bouton et les couleurs d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="cef43-108">The parent window can change the button's text and background colors.</span></span> <span data-ttu-id="cef43-109">Toutefois, seuls les boutons owner-drawn répondent à la fenêtre parente qui traite ce message.</span><span class="sxs-lookup"><span data-stu-id="cef43-109">However, only owner-drawn buttons respond to the parent window processing this message.</span></span>


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cef43-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cef43-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef43-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cef43-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cef43-112">**HDC** qui spécifie le handle du contexte d’affichage du bouton.</span><span class="sxs-lookup"><span data-stu-id="cef43-112">An **HDC** that specifies the handle to the display context for the button.</span></span>

</dd> <dt>

<span data-ttu-id="cef43-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cef43-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cef43-114">**HWND** qui spécifie le handle du bouton.</span><span class="sxs-lookup"><span data-stu-id="cef43-114">An **HWND** that specifies the handle to the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cef43-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cef43-115">Return value</span></span>

<span data-ttu-id="cef43-116">Si une application traite ce message, elle doit retourner un handle à un pinceau.</span><span class="sxs-lookup"><span data-stu-id="cef43-116">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="cef43-117">Le système utilise le pinceau pour peindre l’arrière-plan du bouton.</span><span class="sxs-lookup"><span data-stu-id="cef43-117">The system uses the brush to paint the background of the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="cef43-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cef43-118">Remarks</span></span>

<span data-ttu-id="cef43-119">Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="cef43-119">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="cef43-120">Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="cef43-120">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="cef43-121">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="cef43-121">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the button.</span></span> <span data-ttu-id="cef43-122">Les boutons avec les styles- [**\_ PUSHBUTTON BS**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)ou [**BS \_ PUSHLIKE**](button-styles.md) n’utilisent pas le pinceau retourné.</span><span class="sxs-lookup"><span data-stu-id="cef43-122">Buttons with the [**BS\_PUSHBUTTON**](button-styles.md), [**BS\_DEFPUSHBUTTON**](button-styles.md), or [**BS\_PUSHLIKE**](button-styles.md) styles do not use the returned brush.</span></span> <span data-ttu-id="cef43-123">Les boutons avec ces styles sont toujours dessinés avec les couleurs système par défaut.</span><span class="sxs-lookup"><span data-stu-id="cef43-123">Buttons with these styles are always drawn with the default system colors.</span></span> <span data-ttu-id="cef43-124">Le dessin de boutons de commande requiert plusieurs pinceaux, mise en surbrillance et ombre, mais le message **WM \_ CTLCOLORBTN** permet de retourner un seul pinceau.</span><span class="sxs-lookup"><span data-stu-id="cef43-124">Drawing push buttons requires several different brushes-face, highlight, and shadow-but the **WM\_CTLCOLORBTN** message allows only one brush to be returned.</span></span> <span data-ttu-id="cef43-125">Pour fournir une apparence personnalisée pour les boutons de commande, utilisez un bouton owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="cef43-125">To provide a custom appearance for push buttons, use an owner-drawn button.</span></span> <span data-ttu-id="cef43-126">Pour plus d’informations, consultez [création de contrôles Owner-Drawn](user-controls-intro.md).</span><span class="sxs-lookup"><span data-stu-id="cef43-126">For more information, see [Creating Owner-Drawn Controls](user-controls-intro.md).</span></span>

<span data-ttu-id="cef43-127">Le message **WM \_ CTLCOLORBTN** n’est jamais envoyé entre les threads.</span><span class="sxs-lookup"><span data-stu-id="cef43-127">The **WM\_CTLCOLORBTN** message is never sent between threads.</span></span> <span data-ttu-id="cef43-128">Elle est envoyée uniquement au sein d’un thread.</span><span class="sxs-lookup"><span data-stu-id="cef43-128">It is sent only within one thread.</span></span>

<span data-ttu-id="cef43-129">La couleur de texte d’une case à cocher ou d’une case d’option s’applique à la zone ou au bouton, à sa coche et au texte.</span><span class="sxs-lookup"><span data-stu-id="cef43-129">The text color of a check box or radio button applies to the box or button, its check mark, and the text.</span></span> <span data-ttu-id="cef43-130">Le rectangle de focus de ces boutons reste la couleur système par défaut (généralement le noir).</span><span class="sxs-lookup"><span data-stu-id="cef43-130">The focus rectangle for these buttons remains the system default color (typically black).</span></span> <span data-ttu-id="cef43-131">La couleur de texte d’une zone de groupe s’applique au texte, mais pas à la ligne qui définit la zone.</span><span class="sxs-lookup"><span data-stu-id="cef43-131">The text color of a group box applies to the text but not to the line that defines the box.</span></span> <span data-ttu-id="cef43-132">La couleur de texte d’un bouton de commande s’applique uniquement à son rectangle de focus. elle n’affecte pas la couleur du texte.</span><span class="sxs-lookup"><span data-stu-id="cef43-132">The text color of a push button applies only to its focus rectangle; it does not affect the color of the text.</span></span>

<span data-ttu-id="cef43-133">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="cef43-133">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="cef43-134">Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="cef43-134">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="cef43-135">La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="cef43-135">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef43-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cef43-136">Requirements</span></span>



| <span data-ttu-id="cef43-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cef43-137">Requirement</span></span> | <span data-ttu-id="cef43-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="cef43-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef43-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cef43-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cef43-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cef43-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cef43-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cef43-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cef43-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cef43-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cef43-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="cef43-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="cef43-144"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cef43-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cef43-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cef43-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="cef43-146">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="cef43-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cef43-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="cef43-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="cef43-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="cef43-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

