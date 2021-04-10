---
title: Message WM_CHANGECBCHAIN (winuser. h)
description: Envoyé à la première fenêtre de la chaîne du presse-papiers lorsqu’une fenêtre est supprimée de la chaîne. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN l’échange de données de message
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104089"
---
# <a name="wm_changecbchain-message"></a><span data-ttu-id="6f159-105">\_Message WM CHANGECBCHAIN</span><span class="sxs-lookup"><span data-stu-id="6f159-105">WM\_CHANGECBCHAIN message</span></span>

<span data-ttu-id="6f159-106">Envoyé à la première fenêtre de la chaîne du presse-papiers lorsqu’une fenêtre est supprimée de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="6f159-106">Sent to the first window in the clipboard viewer chain when a window is being removed from the chain.</span></span>

<span data-ttu-id="6f159-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6f159-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a><span data-ttu-id="6f159-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f159-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f159-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f159-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f159-110">Handle de la fenêtre en cours de suppression dans la chaîne du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="6f159-110">A handle to the window being removed from the clipboard viewer chain.</span></span>

</dd> <dt>

<span data-ttu-id="6f159-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f159-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f159-112">Handle vers la fenêtre suivante dans la chaîne après la suppression de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6f159-112">A handle to the next window in the chain following the window being removed.</span></span> <span data-ttu-id="6f159-113">Ce paramètre a la **valeur null** si la fenêtre en cours de suppression est la dernière fenêtre de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="6f159-113">This parameter is **NULL** if the window being removed is the last window in the chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f159-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f159-114">Return value</span></span>

<span data-ttu-id="6f159-115">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6f159-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f159-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6f159-116">Remarks</span></span>

<span data-ttu-id="6f159-117">Chaque fenêtre de la visionneuse du presse-papiers enregistre le descripteur dans la fenêtre suivante dans la chaîne du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="6f159-117">Each clipboard viewer window saves the handle to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="6f159-118">Initialement, ce descripteur est la valeur de retour de la fonction [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="6f159-118">Initially, this handle is the return value of the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="6f159-119">Quand une fenêtre de la visionneuse du presse-papiers reçoit le message **WM \_ CHANGECBCHAIN** , elle doit appeler la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour transmettre le message à la fenêtre suivante dans la chaîne, sauf si la fenêtre suivante est supprimée.</span><span class="sxs-lookup"><span data-stu-id="6f159-119">When a clipboard viewer window receives the **WM\_CHANGECBCHAIN** message, it should call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message to the next window in the chain, unless the next window is the window being removed.</span></span> <span data-ttu-id="6f159-120">Dans ce cas, la visionneuse du presse-papiers doit enregistrer le handle spécifié par le paramètre *lParam* comme fenêtre suivante dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="6f159-120">In this case, the clipboard viewer should save the handle specified by the *lParam* parameter as the next window in the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f159-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f159-121">Requirements</span></span>



| <span data-ttu-id="6f159-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f159-122">Requirement</span></span> | <span data-ttu-id="6f159-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f159-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f159-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f159-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f159-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f159-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6f159-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f159-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f159-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f159-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f159-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f159-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f159-129"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f159-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f159-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f159-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f159-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6f159-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f159-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="6f159-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="6f159-133">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="6f159-133">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

<span data-ttu-id="6f159-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6f159-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f159-135">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="6f159-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

