---
description: Envoyé lorsqu’une application demande qu’une fenêtre soit créée en appelant la fonction CreateWindowEx ou CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Message WM_CREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535461"
---
# <a name="wm_create-message"></a><span data-ttu-id="c8872-103">\_Créer un message WM</span><span class="sxs-lookup"><span data-stu-id="c8872-103">WM\_CREATE message</span></span>

<span data-ttu-id="c8872-104">Envoyé lorsqu’une application demande qu’une fenêtre soit créée en appelant la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="c8872-104">Sent when an application requests that a window be created by calling the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="c8872-105">(Le message est envoyé avant le retour de la fonction.) La procédure de fenêtre de la nouvelle fenêtre reçoit ce message après la création de la fenêtre, mais avant que la fenêtre ne devienne visible.</span><span class="sxs-lookup"><span data-stu-id="c8872-105">(The message is sent before the function returns.) The window procedure of the new window receives this message after the window is created, but before the window becomes visible.</span></span>

<span data-ttu-id="c8872-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c8872-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a><span data-ttu-id="c8872-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8872-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8872-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8872-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8872-109">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="c8872-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c8872-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8872-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8872-111">Pointeur vers une structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) qui contient des informations sur la fenêtre en cours de création.</span><span class="sxs-lookup"><span data-stu-id="c8872-111">A pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8872-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8872-112">Return value</span></span>

<span data-ttu-id="c8872-113">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c8872-113">Type: **LRESULT**</span></span>

<span data-ttu-id="c8872-114">Si une application traite ce message, elle doit retourner zéro pour poursuivre la création de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c8872-114">If an application processes this message, it should return zero to continue creation of the window.</span></span> <span data-ttu-id="c8872-115">Si l’application retourne-1, la fenêtre est détruite et la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) retourne un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="c8872-115">If the application returns –1, the window is destroyed and the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function returns a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8872-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8872-116">Requirements</span></span>



| <span data-ttu-id="c8872-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8872-117">Requirement</span></span> | <span data-ttu-id="c8872-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8872-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8872-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8872-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c8872-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8872-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c8872-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8872-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c8872-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8872-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8872-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8872-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8872-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8872-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8872-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8872-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8872-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c8872-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8872-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="c8872-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="c8872-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="c8872-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="c8872-129">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c8872-129">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="c8872-130">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="c8872-130">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="c8872-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c8872-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8872-132">Windows</span><span class="sxs-lookup"><span data-stu-id="c8872-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
