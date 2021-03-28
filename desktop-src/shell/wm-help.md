---
description: Indique que l’utilisateur a appuyé sur la touche F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Message WM_HELP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973103"
---
# <a name="wm_help-message"></a><span data-ttu-id="7405b-103">\_Message d’aide WM</span><span class="sxs-lookup"><span data-stu-id="7405b-103">WM\_HELP message</span></span>

<span data-ttu-id="7405b-104">Indique que l’utilisateur a appuyé sur la touche F1.</span><span class="sxs-lookup"><span data-stu-id="7405b-104">Indicates that the user pressed the F1 key.</span></span> <span data-ttu-id="7405b-105">Si un menu est actif lorsque la touche F1 est enfoncée, l' **\_ aide WM** est envoyée à la fenêtre associée au menu ; sinon, l' **\_ aide WM** est envoyée à la fenêtre qui a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="7405b-105">If a menu is active when F1 is pressed, **WM\_HELP** is sent to the window associated with the menu; otherwise, **WM\_HELP** is sent to the window that has the keyboard focus.</span></span> <span data-ttu-id="7405b-106">Si aucune fenêtre n’a le focus clavier, l' **\_ aide WM** est envoyée à la fenêtre actuellement active.</span><span class="sxs-lookup"><span data-stu-id="7405b-106">If no window has the keyboard focus, **WM\_HELP** is sent to the currently active window.</span></span>

## <a name="parameters"></a><span data-ttu-id="7405b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7405b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7405b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7405b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7405b-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7405b-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7405b-110">*lphi*</span><span class="sxs-lookup"><span data-stu-id="7405b-110">*lphi*</span></span> 
</dt> <dd>

<span data-ttu-id="7405b-111">Adresse d’une structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) qui contient des informations sur l’élément de menu, le contrôle, la boîte de dialogue ou la fenêtre pour laquelle l’aide est demandée.</span><span class="sxs-lookup"><span data-stu-id="7405b-111">The address of a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains information about the menu item, control, dialog box, or window for which Help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7405b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7405b-112">Return value</span></span>

<span data-ttu-id="7405b-113">Retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="7405b-113">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7405b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7405b-114">Remarks</span></span>

<span data-ttu-id="7405b-115">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) transmet **l' \_ aide WM** à la fenêtre parente d’une fenêtre enfant ou au propriétaire d’une fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="7405b-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes **WM\_HELP** to the parent window of a child window or to the owner of a top-level window.</span></span>

## <a name="requirements"></a><span data-ttu-id="7405b-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7405b-116">Requirements</span></span>



| <span data-ttu-id="7405b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7405b-117">Requirement</span></span> | <span data-ttu-id="7405b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7405b-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7405b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7405b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7405b-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7405b-120">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7405b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7405b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7405b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7405b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7405b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7405b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7405b-124"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="7405b-124"><dt>Winuser.h</dt></span></span> </dl> |



 

 
