---
description: Envoyé lorsqu’une application modifie l’état activé d’une fenêtre.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Message WM_ENABLE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518786"
---
# <a name="wm_enable-message"></a><span data-ttu-id="01c91-103">\_Message d’activation WM</span><span class="sxs-lookup"><span data-stu-id="01c91-103">WM\_ENABLE message</span></span>

<span data-ttu-id="01c91-104">Envoyé lorsqu’une application modifie l’état activé d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="01c91-104">Sent when an application changes the enabled state of a window.</span></span> <span data-ttu-id="01c91-105">Il est envoyé à la fenêtre dont l’état activé est modifié.</span><span class="sxs-lookup"><span data-stu-id="01c91-105">It is sent to the window whose enabled state is changing.</span></span> <span data-ttu-id="01c91-106">Ce message est envoyé avant le retour de la fonction [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) , mais après la modification de l’état activé (le bit de style de [**WS \_ désactivé**](window-styles.md) ) de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="01c91-106">This message is sent before the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function returns, but after the enabled state ([**WS\_DISABLED**](window-styles.md) style bit) of the window has changed.</span></span>

<span data-ttu-id="01c91-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="01c91-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a><span data-ttu-id="01c91-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01c91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c91-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01c91-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01c91-110">Indique si la fenêtre a été activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="01c91-110">Indicates whether the window has been enabled or disabled.</span></span> <span data-ttu-id="01c91-111">Ce paramètre a la **valeur true** si la fenêtre a été activée ou **false** si elle a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="01c91-111">This parameter is **TRUE** if the window has been enabled or **FALSE** if the window has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="01c91-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01c91-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01c91-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="01c91-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01c91-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01c91-114">Return value</span></span>

<span data-ttu-id="01c91-115">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="01c91-115">Type: **LRESULT**</span></span>

<span data-ttu-id="01c91-116">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="01c91-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c91-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01c91-117">Requirements</span></span>



| <span data-ttu-id="01c91-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01c91-118">Requirement</span></span> | <span data-ttu-id="01c91-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="01c91-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c91-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01c91-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01c91-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01c91-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="01c91-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01c91-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01c91-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01c91-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01c91-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="01c91-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c91-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01c91-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c91-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01c91-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="01c91-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="01c91-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="01c91-128">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="01c91-128">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

<span data-ttu-id="01c91-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="01c91-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="01c91-130">Windows</span><span class="sxs-lookup"><span data-stu-id="01c91-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
