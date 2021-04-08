---
description: Envoyé à une fenêtre enfant lorsque l’utilisateur clique sur la barre de titre de la fenêtre ou lorsque la fenêtre est activée, déplacée ou dimensionnée.
ms.assetid: 6e60725d-aa01-48bb-86a5-f17f56b97d35
title: Message WM_CHILDACTIVATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82564a63cfbbbfe5e3693e331c8e990fa934e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757828"
---
# <a name="wm_childactivate-message"></a><span data-ttu-id="54d84-103">\_Message WM CHILDACTIVATE</span><span class="sxs-lookup"><span data-stu-id="54d84-103">WM\_CHILDACTIVATE message</span></span>

<span data-ttu-id="54d84-104">Envoyé à une fenêtre enfant lorsque l’utilisateur clique sur la barre de titre de la fenêtre ou lorsque la fenêtre est activée, déplacée ou dimensionnée.</span><span class="sxs-lookup"><span data-stu-id="54d84-104">Sent to a child window when the user clicks the window's title bar or when the window is activated, moved, or sized.</span></span>

<span data-ttu-id="54d84-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="54d84-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHILDACTIVATE                0x0022
```



## <a name="parameters"></a><span data-ttu-id="54d84-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54d84-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54d84-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="54d84-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="54d84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54d84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54d84-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="54d84-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d84-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54d84-111">Return value</span></span>

<span data-ttu-id="54d84-112">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="54d84-112">Type: **LRESULT**</span></span>

<span data-ttu-id="54d84-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="54d84-113">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d84-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54d84-114">Requirements</span></span>



| <span data-ttu-id="54d84-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54d84-115">Requirement</span></span> | <span data-ttu-id="54d84-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="54d84-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d84-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54d84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54d84-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54d84-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="54d84-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54d84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54d84-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54d84-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54d84-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="54d84-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="54d84-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54d84-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d84-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54d84-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="54d84-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="54d84-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54d84-125">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="54d84-125">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="54d84-126">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="54d84-126">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

<span data-ttu-id="54d84-127">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="54d84-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54d84-128">Windows</span><span class="sxs-lookup"><span data-stu-id="54d84-128">Windows</span></span>](windows.md)
</dt> </dl>

 

 
