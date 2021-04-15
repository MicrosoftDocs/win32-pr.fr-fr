---
title: Message WM_GETTITLEBARINFOEX (winuser. h)
description: Envoyé pour demander des informations étendues de barre de titre. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384139"
---
# <a name="wm_gettitlebarinfoex-message"></a><span data-ttu-id="e76a1-105">\_Message WM GETTITLEBARINFOEX</span><span class="sxs-lookup"><span data-stu-id="e76a1-105">WM\_GETTITLEBARINFOEX message</span></span>

<span data-ttu-id="e76a1-106">Envoyé pour demander des informations étendues de barre de titre.</span><span class="sxs-lookup"><span data-stu-id="e76a1-106">Sent to request extended title bar information.</span></span> <span data-ttu-id="e76a1-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e76a1-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a><span data-ttu-id="e76a1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e76a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76a1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e76a1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e76a1-110">Ce paramètre n’est pas utilisé et doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="e76a1-110">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="e76a1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e76a1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e76a1-112">Pointeur vers une structure [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="e76a1-112">A pointer to a [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span> <span data-ttu-id="e76a1-113">L’expéditeur du message est chargé d’allouer de la mémoire pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="e76a1-113">The message sender is responsible for allocating memory for this structure.</span></span> <span data-ttu-id="e76a1-114">Affectez au membre **cbSize** de cette structure la valeur `sizeof(TITLEBARINFOEX)` avant de passer cette structure avec le message.</span><span class="sxs-lookup"><span data-stu-id="e76a1-114">Set the **cbSize** member of this structure to `sizeof(TITLEBARINFOEX)` before passing this structure with the message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e76a1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e76a1-115">Remarks</span></span>

<span data-ttu-id="e76a1-116">L’exemple suivant montre comment le récepteur de message convertit une valeur **lParam** pour récupérer la structure [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="e76a1-116">The following example shows how the message receiver casts an **LPARAM** value to retrieve the [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span>

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a><span data-ttu-id="e76a1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e76a1-117">Requirements</span></span>



| <span data-ttu-id="e76a1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e76a1-118">Requirement</span></span> | <span data-ttu-id="e76a1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e76a1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76a1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e76a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e76a1-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e76a1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e76a1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e76a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e76a1-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e76a1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e76a1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e76a1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76a1-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e76a1-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e76a1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e76a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76a1-127">Vue d’ensemble des menus</span><span class="sxs-lookup"><span data-stu-id="e76a1-127">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

