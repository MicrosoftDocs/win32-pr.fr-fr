---
title: Message WM_NOTIFY (winuser. h)
description: Envoyé par un contrôle commun à sa fenêtre parente lorsqu’un événement s’est produit ou que le contrôle requiert des informations.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- WM_NOTIFY les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942371"
---
# <a name="wm_notify-message"></a><span data-ttu-id="c8091-104">\_Message de notification WM</span><span class="sxs-lookup"><span data-stu-id="c8091-104">WM\_NOTIFY message</span></span>

<span data-ttu-id="c8091-105">Envoyé par un contrôle commun à sa fenêtre parente lorsqu’un événement s’est produit ou que le contrôle requiert des informations.</span><span class="sxs-lookup"><span data-stu-id="c8091-105">Sent by a common control to its parent window when an event has occurred or the control requires some information.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8091-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8091-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8091-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8091-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8091-108">Identificateur du contrôle commun qui envoie le message.</span><span class="sxs-lookup"><span data-stu-id="c8091-108">The identifier of the common control sending the message.</span></span> <span data-ttu-id="c8091-109">Il n’est pas garanti que cet identificateur soit unique.</span><span class="sxs-lookup"><span data-stu-id="c8091-109">This identifier is not guaranteed to be unique.</span></span> <span data-ttu-id="c8091-110">Une application doit utiliser le membre **hwndFrom** ou **idFrom** de la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (passé comme paramètre *lParam* ) pour identifier le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8091-110">An application should use the **hwndFrom** or **idFrom** member of the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure (passed as the *lParam* parameter) to identify the control.</span></span>

</dd> <dt>

<span data-ttu-id="c8091-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8091-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8091-112">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient le code de notification et des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c8091-112">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains the notification code and additional information.</span></span> <span data-ttu-id="c8091-113">Pour certains messages de notification, ce paramètre pointe vers une structure plus grande qui a la structure **NMHDR** comme premier membre.</span><span class="sxs-lookup"><span data-stu-id="c8091-113">For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8091-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8091-114">Return value</span></span>

<span data-ttu-id="c8091-115">La valeur de retour est ignorée, à l’exception des messages de notification qui le définissent autrement.</span><span class="sxs-lookup"><span data-stu-id="c8091-115">The return value is ignored except for notification messages that specify otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8091-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c8091-116">Remarks</span></span>

<span data-ttu-id="c8091-117">La destination du message doit être le **HWND** du parent du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8091-117">The destination of the message must be the **HWND** of the parent of the control.</span></span> <span data-ttu-id="c8091-118">Cette valeur peut être obtenue à l’aide de [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), comme illustré dans l’exemple suivant, où *m \_ controlHwnd* est le **HWND** du contrôle lui-même.</span><span class="sxs-lookup"><span data-stu-id="c8091-118">This value can be obtained by using [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), as shown in the following example, where *m\_controlHwnd* is the **HWND** of the control itself.</span></span>


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



<span data-ttu-id="c8091-119">Les applications gèrent le message dans la procédure de fenêtre de la fenêtre parente, comme illustré dans l’exemple suivant, qui gère le message de notification envoyé par le contrôle personnalisé dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="c8091-119">Applications handle the message in the window procedure of the parent window, as shown in the following example, which handles the notification message sent by the custom control in the previous example.</span></span>


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



<span data-ttu-id="c8091-120">Certaines notifications, essentiellement celles qui se trouvent dans l’API pendant une longue période, sont envoyées en tant que messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c8091-120">Some notifications, chiefly those that have been in the API for a long time, are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="c8091-121">Pour plus d’informations, consultez [contrôle des messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="c8091-121">For more information, see [Control Messages](control-messages.md).</span></span>

<span data-ttu-id="c8091-122">Si le gestionnaire de messages est dans une procédure de boîte de dialogue, vous devez utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec DWL \_ MSGRESULT pour définir une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c8091-122">If the message handler is in a dialog box procedure, you must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set a return value.</span></span>

<span data-ttu-id="c8091-123">Pour les systèmes Windows Vista et versions ultérieures, le message **WM \_ Notify** ne peut pas être envoyé entre les processus.</span><span class="sxs-lookup"><span data-stu-id="c8091-123">For Windows Vista and later systems, the **WM\_NOTIFY** message cannot be sent between processes.</span></span>

<span data-ttu-id="c8091-124">De nombreuses notifications sont disponibles à la fois dans les formats ANSI et Unicode.</span><span class="sxs-lookup"><span data-stu-id="c8091-124">Many notifications are available in both ANSI and Unicode formats.</span></span> <span data-ttu-id="c8091-125">La fenêtre qui envoie le message **WM \_ Notify** utilise le message [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) pour déterminer le format à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c8091-125">The window sending the **WM\_NOTIFY** message uses the [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message to determine which format should be used.</span></span> <span data-ttu-id="c8091-126">Pour plus d’informations, consultez **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="c8091-126">See **WM\_NOTIFYFORMAT** for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8091-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8091-127">Requirements</span></span>



| <span data-ttu-id="c8091-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8091-128">Requirement</span></span> | <span data-ttu-id="c8091-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8091-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c8091-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8091-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c8091-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8091-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c8091-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8091-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c8091-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8091-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c8091-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8091-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8091-135"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8091-135"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8091-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8091-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8091-137">**\_NOTIFYFORMAT WM**</span><span class="sxs-lookup"><span data-stu-id="c8091-137">**WM\_NOTIFYFORMAT**</span></span>](wm-notifyformat.md)
</dt> </dl>

 

