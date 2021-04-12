---
title: Message WM_NEXTDLGCTL (winuser. h)
description: Envoyé à une procédure de boîte de dialogue pour définir le focus clavier sur un autre contrôle dans la boîte de dialogue.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Boîtes de dialogue de WM_NEXTDLGCTL message
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508953"
---
# <a name="wm_nextdlgctl-message"></a><span data-ttu-id="e6ec4-104">\_Message WM NEXTDLGCTL</span><span class="sxs-lookup"><span data-stu-id="e6ec4-104">WM\_NEXTDLGCTL message</span></span>

<span data-ttu-id="e6ec4-105">Envoyé à une procédure de boîte de dialogue pour définir le focus clavier sur un autre contrôle dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-105">Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box.</span></span>


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a><span data-ttu-id="e6ec4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6ec4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ec4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6ec4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6ec4-108">Si *lParam* a la **valeur true**, ce paramètre identifie le contrôle qui reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-108">If *lParam* is **TRUE**, this parameter identifies the control that receives the focus.</span></span> <span data-ttu-id="e6ec4-109">Si *lParam* a la **valeur false**, ce paramètre indique si le contrôle suivant ou précédent avec le style **WS \_ TABSTOP** reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-109">If *lParam* is **FALSE**, this parameter indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span> <span data-ttu-id="e6ec4-110">Si *wParam* est égal à zéro, le contrôle suivant reçoit le focus ; Sinon, le contrôle précédent avec le style **WS \_ TABSTOP** reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-110">If *wParam* is zero, the next control receives the focus; otherwise, the previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> <dt>

<span data-ttu-id="e6ec4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6ec4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6ec4-112">Le mot de poids faible indique comment le système utilise *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-112">The low-order word indicates how the system uses *wParam*.</span></span> <span data-ttu-id="e6ec4-113">Si le mot de poids faible est **true**, *wParam* est un handle associé au contrôle qui reçoit le focus. Sinon, *wParam* est un indicateur qui indique si le contrôle suivant ou précédent avec le style **WS \_ TABSTOP** reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-113">If the low-order word is **TRUE**, *wParam* is a handle associated with the control that receives the focus; otherwise, *wParam* is a flag that indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ec4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6ec4-114">Return value</span></span>

<span data-ttu-id="e6ec4-115">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-115">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6ec4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e6ec4-116">Remarks</span></span>

<span data-ttu-id="e6ec4-117">Ce message effectue des opérations de gestion de boîte de dialogue supplémentaires au-delà de celles effectuées par la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **WM \_ NEXTDLGCTL** met à jour la bordure du bouton de commande par défaut, définit l’identificateur de contrôle par défaut et sélectionne automatiquement le texte d’un contrôle d’édition (si la fenêtre cible est un contrôle d’édition).</span><span class="sxs-lookup"><span data-stu-id="e6ec4-117">This message performs additional dialog box management operations beyond those performed by the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function **WM\_NEXTDLGCTL** updates the default pushbutton border, sets the default control identifier, and automatically selects the text of an edit control (if the target window is an edit control).</span></span>

<span data-ttu-id="e6ec4-118">N’utilisez pas la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour envoyer un message **WM \_ NEXTDLGCTL** si votre application traite de façon simultanée d’autres messages qui définissent le focus.</span><span class="sxs-lookup"><span data-stu-id="e6ec4-118">Do not use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to send a **WM\_NEXTDLGCTL** message if your application will concurrently process other messages that set the focus.</span></span> <span data-ttu-id="e6ec4-119">Utilisez à la place la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .</span><span class="sxs-lookup"><span data-stu-id="e6ec4-119">Use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ec4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6ec4-120">Requirements</span></span>



| <span data-ttu-id="e6ec4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6ec4-121">Requirement</span></span> | <span data-ttu-id="e6ec4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6ec4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ec4-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6ec4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ec4-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6ec4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e6ec4-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6ec4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ec4-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6ec4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6ec4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6ec4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6ec4-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6ec4-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ec4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6ec4-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6ec4-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e6ec4-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6ec4-131">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="e6ec4-131">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="e6ec4-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="e6ec4-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="e6ec4-133">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="e6ec4-133">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="e6ec4-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="e6ec4-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6ec4-135">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="e6ec4-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

