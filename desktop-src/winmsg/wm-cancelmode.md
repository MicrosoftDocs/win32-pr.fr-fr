---
description: Envoyé pour annuler certains modes, tels que la capture de la souris.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Message WM_CANCELMODE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530100"
---
# <a name="wm_cancelmode-message"></a><span data-ttu-id="452c6-103">\_Message WM CANCELMODE</span><span class="sxs-lookup"><span data-stu-id="452c6-103">WM\_CANCELMODE message</span></span>

<span data-ttu-id="452c6-104">Envoyé pour annuler certains modes, tels que la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="452c6-104">Sent to cancel certain modes, such as mouse capture.</span></span> <span data-ttu-id="452c6-105">Par exemple, le système envoie ce message à la fenêtre active lorsqu’une boîte de dialogue ou une boîte de message s’affiche.</span><span class="sxs-lookup"><span data-stu-id="452c6-105">For example, the system sends this message to the active window when a dialog box or message box is displayed.</span></span> <span data-ttu-id="452c6-106">Certaines fonctions envoient également ce message explicitement à la fenêtre spécifiée, qu’il s’agisse de la fenêtre active ou non.</span><span class="sxs-lookup"><span data-stu-id="452c6-106">Certain functions also send this message explicitly to the specified window regardless of whether it is the active window.</span></span> <span data-ttu-id="452c6-107">Par exemple, la fonction [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) envoie ce message lors de la désactivation de la fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="452c6-107">For example, the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function sends this message when disabling the specified window.</span></span>

<span data-ttu-id="452c6-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="452c6-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a><span data-ttu-id="452c6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="452c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="452c6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="452c6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="452c6-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="452c6-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="452c6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="452c6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="452c6-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="452c6-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="452c6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="452c6-114">Return value</span></span>

<span data-ttu-id="452c6-115">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="452c6-115">Type: **LRESULT**</span></span>

<span data-ttu-id="452c6-116">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="452c6-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="452c6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="452c6-117">Remarks</span></span>

<span data-ttu-id="452c6-118">Lorsque le message **WM \_ CANCELMODE** est envoyé, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) annule le traitement interne de l’entrée de la barre de défilement standard, annule le traitement du menu interne et libère la capture de la souris.</span><span class="sxs-lookup"><span data-stu-id="452c6-118">When the **WM\_CANCELMODE** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function cancels internal processing of standard scroll bar input, cancels internal menu processing, and releases the mouse capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="452c6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="452c6-119">Requirements</span></span>



| <span data-ttu-id="452c6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="452c6-120">Requirement</span></span> | <span data-ttu-id="452c6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="452c6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="452c6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="452c6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="452c6-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="452c6-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="452c6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="452c6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="452c6-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="452c6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="452c6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="452c6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="452c6-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="452c6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452c6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="452c6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="452c6-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="452c6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="452c6-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="452c6-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="452c6-131">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="452c6-131">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[<span data-ttu-id="452c6-132">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="452c6-132">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

<span data-ttu-id="452c6-133">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="452c6-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="452c6-134">Windows</span><span class="sxs-lookup"><span data-stu-id="452c6-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
