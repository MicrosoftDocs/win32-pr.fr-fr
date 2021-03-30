---
description: Le \_ message WM DEVMODECHANGE est envoyé à toutes les fenêtres de niveau supérieur chaque fois que l’utilisateur modifie les paramètres du mode de l’appareil.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Message WM_DEVMODECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973518"
---
# <a name="wm_devmodechange-message"></a><span data-ttu-id="c8185-103">\_Message WM DEVMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="c8185-103">WM\_DEVMODECHANGE message</span></span>

<span data-ttu-id="c8185-104">Le message **WM \_ DEVMODECHANGE** est envoyé à toutes les fenêtres de niveau supérieur chaque fois que l’utilisateur modifie les paramètres du mode de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c8185-104">The **WM\_DEVMODECHANGE** message is sent to all top-level windows whenever the user changes device-mode settings.</span></span>

<span data-ttu-id="c8185-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c8185-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="c8185-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8185-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8185-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c8185-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c8185-108">Handle d'une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c8185-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="c8185-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="c8185-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="c8185-110">\_DEVMODECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="c8185-110">WM\_DEVMODECHANGE</span></span>

</dd> <dt>

<span data-ttu-id="c8185-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8185-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8185-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c8185-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c8185-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8185-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8185-114">Pointeur vers une chaîne qui spécifie le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c8185-114">A pointer to a string that specifies the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8185-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8185-115">Return value</span></span>

<span data-ttu-id="c8185-116">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="c8185-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8185-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c8185-117">Remarks</span></span>

<span data-ttu-id="c8185-118">Ce message ne peut pas être envoyé directement à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c8185-118">This message cannot be sent directly to a window.</span></span> <span data-ttu-id="c8185-119">Pour envoyer le message **WM \_ DEVMODECHANGE** à toutes les fenêtres de niveau supérieur, utilisez la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) avec le paramètre *HWND* défini sur \_ Broadcast HWND.</span><span class="sxs-lookup"><span data-stu-id="c8185-119">To send the **WM\_DEVMODECHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hWnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8185-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c8185-120">Requirements</span></span>



| <span data-ttu-id="c8185-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8185-121">Requirement</span></span> | <span data-ttu-id="c8185-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8185-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8185-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8185-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8185-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8185-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c8185-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8185-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8185-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8185-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8185-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8185-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8185-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8185-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8185-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8185-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8185-130">Vue d’ensemble des contextes de périphérique</span><span class="sxs-lookup"><span data-stu-id="c8185-130">Device Contexts Overview</span></span>](device-contexts.md)
</dt> <dt>

[<span data-ttu-id="c8185-131">Messages de contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="c8185-131">Device Context Messages</span></span>](device-context-messages.md)
</dt> </dl>

 

 
