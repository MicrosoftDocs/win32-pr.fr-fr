---
title: Message WM_CTLCOLORSTATIC (winuser. h)
description: Un contrôle statique, ou un contrôle d’édition qui est en lecture seule ou qui est désactivé, envoie le \_ message WM CTLCOLORSTATIC à sa fenêtre parente lorsque le contrôle va être dessiné.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741365"
---
# <a name="wm_ctlcolorstatic-message"></a><span data-ttu-id="06504-104">\_Message WM CTLCOLORSTATIC</span><span class="sxs-lookup"><span data-stu-id="06504-104">WM\_CTLCOLORSTATIC message</span></span>

<span data-ttu-id="06504-105">Un contrôle statique, ou un contrôle d’édition qui est en lecture seule ou qui est désactivé, envoie le message **WM \_ CTLCOLORSTATIC** à sa fenêtre parente lorsque le contrôle va être dessiné.</span><span class="sxs-lookup"><span data-stu-id="06504-105">A static control, or an edit control that is read-only or disabled, sends the **WM\_CTLCOLORSTATIC** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="06504-106">En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte de périphérique spécifié pour définir les couleurs de premier plan et d’arrière-plan du texte du contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="06504-106">By responding to this message, the parent window can use the specified device context handle to set the text foreground and background colors of the static control.</span></span>

<span data-ttu-id="06504-107">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="06504-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="06504-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06504-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06504-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06504-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06504-110">Handle vers le contexte de périphérique pour la fenêtre de contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="06504-110">Handle to the device context for the static control window.</span></span>

</dd> <dt>

<span data-ttu-id="06504-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06504-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06504-112">Handle vers le contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="06504-112">Handle to the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06504-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06504-113">Return value</span></span>

<span data-ttu-id="06504-114">Si une application traite ce message, la valeur de retour est un handle vers un pinceau que le système utilise pour peindre l’arrière-plan du contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="06504-114">If an application processes this message, the return value is a handle to a brush that the system uses to paint the background of the static control.</span></span>

## <a name="remarks"></a><span data-ttu-id="06504-115">Notes</span><span class="sxs-lookup"><span data-stu-id="06504-115">Remarks</span></span>

<span data-ttu-id="06504-116">Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="06504-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="06504-117">Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.</span><span class="sxs-lookup"><span data-stu-id="06504-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="06504-118">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le contrôle statique.</span><span class="sxs-lookup"><span data-stu-id="06504-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the static control.</span></span>

<span data-ttu-id="06504-119">Vous pouvez définir la couleur d’arrière-plan du texte d’un contrôle d’édition désactivé, mais vous ne pouvez pas définir la couleur de premier plan du texte.</span><span class="sxs-lookup"><span data-stu-id="06504-119">You can set the text background color of a disabled edit control, but you cannot set the text foreground color.</span></span> <span data-ttu-id="06504-120">Le système utilise toujours la couleur \_ GRAYTEXT.</span><span class="sxs-lookup"><span data-stu-id="06504-120">The system always uses COLOR\_GRAYTEXT.</span></span>

<span data-ttu-id="06504-121">Les contrôles d’édition qui ne sont pas en lecture seule ou désactivés n’envoient pas le message **WM \_ CTLCOLORSTATIC** ; à la place, ils envoient le message [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .</span><span class="sxs-lookup"><span data-stu-id="06504-121">Edit controls that are not read-only or disabled do not send the **WM\_CTLCOLORSTATIC** message; instead, they send the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

<span data-ttu-id="06504-122">Le message **WM \_ CTLCOLORSTATIC** n’est jamais envoyé entre les threads ; il est envoyé uniquement dans le même thread.</span><span class="sxs-lookup"><span data-stu-id="06504-122">The **WM\_CTLCOLORSTATIC** message is never sent between threads; it is sent only within the same thread.</span></span>

<span data-ttu-id="06504-123">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="06504-123">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="06504-124">Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="06504-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="06504-125">La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="06504-125">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="06504-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="06504-126">Examples</span></span>

<span data-ttu-id="06504-127">L’exemple C++ suivant montre comment définir les couleurs de premier plan et d’arrière-plan du texte d’un contrôle statique en réponse au message **WM \_ CTLCOLORSTATIC** .</span><span class="sxs-lookup"><span data-stu-id="06504-127">The following C++ example shows how to set the text foreground and background colors of a static control in response to the **WM\_CTLCOLORSTATIC** message.</span></span> <span data-ttu-id="06504-128">La `hbrBkgnd` variable est une variable **HBRUSH** statique qui est initialisée à la valeur null et stocke le pinceau d’arrière-plan entre les appels à **WM \_ CTLCOLORSTATIC**.</span><span class="sxs-lookup"><span data-stu-id="06504-128">The `hbrBkgnd` variable is a static **HBRUSH** variable that is initialized to NULL, and stores the background brush between calls to **WM\_CTLCOLORSTATIC**.</span></span> <span data-ttu-id="06504-129">Le pinceau doit être détruit par un appel à la fonction [**SupprimerObjet**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) lorsqu’il n’est plus nécessaire, en général lorsque la boîte de dialogue associée est détruite.</span><span class="sxs-lookup"><span data-stu-id="06504-129">The brush must be destroyed by a call to the [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) function when it is no longer needed, typically when the associated dialog box is destroyed.</span></span>


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a><span data-ttu-id="06504-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06504-130">Requirements</span></span>



| <span data-ttu-id="06504-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06504-131">Requirement</span></span> | <span data-ttu-id="06504-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="06504-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06504-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06504-133">Minimum supported client</span></span><br/> | <span data-ttu-id="06504-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06504-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="06504-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06504-135">Minimum supported server</span></span><br/> | <span data-ttu-id="06504-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06504-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06504-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="06504-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="06504-138"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06504-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06504-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06504-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="06504-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="06504-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06504-141">**\_CTLCOLORBTN WM**</span><span class="sxs-lookup"><span data-stu-id="06504-141">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="06504-142">**\_CTLCOLOREDIT WM**</span><span class="sxs-lookup"><span data-stu-id="06504-142">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="06504-143">**\_CTLCOLORLISTBOX WM**</span><span class="sxs-lookup"><span data-stu-id="06504-143">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="06504-144">**\_CTLCOLORSCROLLBAR WM**</span><span class="sxs-lookup"><span data-stu-id="06504-144">**WM\_CTLCOLORSCROLLBAR**</span></span>](wm-ctlcolorscrollbar.md)
</dt> <dt>

<span data-ttu-id="06504-145">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="06504-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="06504-146">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="06504-146">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="06504-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="06504-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="06504-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="06504-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="06504-149">**\_CTLCOLORDLG WM**</span><span class="sxs-lookup"><span data-stu-id="06504-149">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

