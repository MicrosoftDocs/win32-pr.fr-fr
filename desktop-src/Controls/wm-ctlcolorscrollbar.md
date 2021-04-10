---
title: Message WM_CTLCOLORSCROLLBAR (winuser. h)
description: Le \_ message WM CTLCOLORSCROLLBAR est envoyé à la fenêtre parente d’un contrôle de barre de défilement lorsque le contrôle va être dessiné.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942064"
---
# <a name="wm_ctlcolorscrollbar-message"></a><span data-ttu-id="53da6-104">\_Message WM CTLCOLORSCROLLBAR</span><span class="sxs-lookup"><span data-stu-id="53da6-104">WM\_CTLCOLORSCROLLBAR message</span></span>

<span data-ttu-id="53da6-105">Le message **WM \_ CTLCOLORSCROLLBAR** est envoyé à la fenêtre parente d’un contrôle de barre de défilement lorsque le contrôle va être dessiné.</span><span class="sxs-lookup"><span data-stu-id="53da6-105">The **WM\_CTLCOLORSCROLLBAR** message is sent to the parent window of a scroll bar control when the control is about to be drawn.</span></span> <span data-ttu-id="53da6-106">En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte d’affichage pour définir la couleur d’arrière-plan du contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="53da6-106">By responding to this message, the parent window can use the display context handle to set the background color of the scroll bar control.</span></span>

<span data-ttu-id="53da6-107">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="53da6-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="53da6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53da6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53da6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53da6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53da6-110">Handle vers le contexte de périphérique pour le contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="53da6-110">Handle to the device context for the scroll bar control.</span></span>

</dd> <dt>

<span data-ttu-id="53da6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53da6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53da6-112">Handle de la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="53da6-112">Handle to the scroll bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53da6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53da6-113">Return value</span></span>

<span data-ttu-id="53da6-114">Si une application traite ce message, elle doit retourner le handle à un pinceau.</span><span class="sxs-lookup"><span data-stu-id="53da6-114">If an application processes this message, it must return the handle to a brush.</span></span> <span data-ttu-id="53da6-115">Le système utilise le pinceau pour peindre l’arrière-plan du contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="53da6-115">The system uses the brush to paint the background of the scroll bar control.</span></span>

## <a name="remarks"></a><span data-ttu-id="53da6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="53da6-116">Remarks</span></span>

<span data-ttu-id="53da6-117">Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="53da6-117">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="53da6-118">Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="53da6-118">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="53da6-119">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le contrôle de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="53da6-119">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the scroll bar control.</span></span>

<span data-ttu-id="53da6-120">Le message **WM \_ CTLCOLORSCROLLBAR** n’est jamais envoyé entre les threads ; il n’est envoyé que dans le même thread.</span><span class="sxs-lookup"><span data-stu-id="53da6-120">The **WM\_CTLCOLORSCROLLBAR** message is never sent between threads; it is only sent within the same thread.</span></span>

<span data-ttu-id="53da6-121">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="53da6-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="53da6-122">Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="53da6-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="53da6-123">La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="53da6-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="53da6-124">Le message **WM \_ CTLCOLORSCROLLBAR** est utilisé uniquement par les contrôles de barre de défilement enfants.</span><span class="sxs-lookup"><span data-stu-id="53da6-124">The **WM\_CTLCOLORSCROLLBAR** message is used only by child scroll bar controls.</span></span> <span data-ttu-id="53da6-125">Les barres de défilement attachées à une fenêtre (WS \_ Scroll et WS \_ VSCROLL) ne génèrent pas ce message.</span><span class="sxs-lookup"><span data-stu-id="53da6-125">Scrollbars attached to a window (WS\_SCROLL and WS\_VSCROLL) do not generate this message.</span></span> <span data-ttu-id="53da6-126">Pour personnaliser l’apparence des barres de défilement attachées à une fenêtre, utilisez les fonctions de barre de défilement plat.</span><span class="sxs-lookup"><span data-stu-id="53da6-126">To customize the appearance of scrollbars attached to a window, use the flat scroll bar functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="53da6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53da6-127">Requirements</span></span>



| <span data-ttu-id="53da6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53da6-128">Requirement</span></span> | <span data-ttu-id="53da6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="53da6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53da6-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53da6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53da6-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53da6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53da6-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53da6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53da6-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53da6-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53da6-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="53da6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="53da6-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53da6-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53da6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53da6-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="53da6-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="53da6-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53da6-138">**\_CTLCOLORBTN WM**</span><span class="sxs-lookup"><span data-stu-id="53da6-138">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="53da6-139">**\_CTLCOLOREDIT WM**</span><span class="sxs-lookup"><span data-stu-id="53da6-139">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="53da6-140">**\_CTLCOLORLISTBOX WM**</span><span class="sxs-lookup"><span data-stu-id="53da6-140">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="53da6-141">**\_CTLCOLORSTATIC WM**</span><span class="sxs-lookup"><span data-stu-id="53da6-141">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="53da6-142">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="53da6-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="53da6-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="53da6-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="53da6-144">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="53da6-144">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="53da6-145">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="53da6-145">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="53da6-146">**\_CTLCOLORDLG WM**</span><span class="sxs-lookup"><span data-stu-id="53da6-146">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

