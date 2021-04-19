---
title: Message WM_DRAWCLIPBOARD (winuser. h)
description: Envoyé à la première fenêtre de la chaîne du presse-papiers lorsque le contenu du presse-papiers change. Cela permet à une fenêtre de la visionneuse du presse-papiers d’afficher le nouveau contenu du presse-papiers. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513602"
---
# <a name="wm_drawclipboard-message"></a><span data-ttu-id="42e28-106">\_Message WM DRAWCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="42e28-106">WM\_DRAWCLIPBOARD message</span></span>

<span data-ttu-id="42e28-107">Envoyé à la première fenêtre de la chaîne du presse-papiers lorsque le contenu du presse-papiers change.</span><span class="sxs-lookup"><span data-stu-id="42e28-107">Sent to the first window in the clipboard viewer chain when the content of the clipboard changes.</span></span> <span data-ttu-id="42e28-108">Cela permet à une fenêtre de la visionneuse du presse-papiers d’afficher le nouveau contenu du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="42e28-108">This enables a clipboard viewer window to display the new content of the clipboard.</span></span>

<span data-ttu-id="42e28-109">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="42e28-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a><span data-ttu-id="42e28-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42e28-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e28-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42e28-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42e28-112">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="42e28-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="42e28-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42e28-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42e28-114">Ce paramètre n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="42e28-114">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42e28-115">Notes</span><span class="sxs-lookup"><span data-stu-id="42e28-115">Remarks</span></span>

<span data-ttu-id="42e28-116">Seules les fenêtres de la visionneuse du presse-papiers reçoivent ce message.</span><span class="sxs-lookup"><span data-stu-id="42e28-116">Only clipboard viewer windows receive this message.</span></span> <span data-ttu-id="42e28-117">Il s’agit des fenêtres qui ont été ajoutées à la chaîne du presse-papiers à l’aide de la fonction [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="42e28-117">These are windows that have been added to the clipboard viewer chain by using the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="42e28-118">Chaque fenêtre qui reçoit le message **WM \_ DRAWCLIPBOARD** doit appeler la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour transmettre le message à la fenêtre suivante dans la chaîne du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="42e28-118">Each window that receives the **WM\_DRAWCLIPBOARD** message must call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message on to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="42e28-119">Le handle de la fenêtre suivante dans la chaîne est retourné par [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)et peut changer en réponse à un message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="42e28-119">The handle to the next window in the chain is returned by [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer), and may change in response to a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="42e28-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42e28-120">Requirements</span></span>



| <span data-ttu-id="42e28-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42e28-121">Requirement</span></span> | <span data-ttu-id="42e28-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="42e28-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e28-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42e28-123">Minimum supported client</span></span><br/> | <span data-ttu-id="42e28-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42e28-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="42e28-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42e28-125">Minimum supported server</span></span><br/> | <span data-ttu-id="42e28-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42e28-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42e28-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="42e28-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e28-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42e28-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e28-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42e28-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="42e28-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="42e28-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="42e28-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="42e28-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="42e28-132">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="42e28-132">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="42e28-133">**\_CHANGECBCHAIN WM**</span><span class="sxs-lookup"><span data-stu-id="42e28-133">**WM\_CHANGECBCHAIN**</span></span>](wm-changecbchain.md)
</dt> <dt>

<span data-ttu-id="42e28-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="42e28-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="42e28-135">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="42e28-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

