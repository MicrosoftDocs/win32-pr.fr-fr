---
title: Message WM_UNINITMENUPOPUP (winuser. h)
description: Envoyé lorsqu’un menu ou sous-menu déroulant a été détruit.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519193"
---
# <a name="wm_uninitmenupopup-message"></a><span data-ttu-id="a6ea9-104">\_Message WM UNINITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="a6ea9-104">WM\_UNINITMENUPOPUP message</span></span>

<span data-ttu-id="a6ea9-105">Envoyé lorsqu’un menu ou sous-menu déroulant a été détruit.</span><span class="sxs-lookup"><span data-stu-id="a6ea9-105">Sent when a drop-down menu or submenu has been destroyed.</span></span>


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a><span data-ttu-id="a6ea9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6ea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ea9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6ea9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ea9-108">Handle du menu</span><span class="sxs-lookup"><span data-stu-id="a6ea9-108">A handle to the menu</span></span>

</dd> <dt>

<span data-ttu-id="a6ea9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6ea9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ea9-110">Le mot de poids fort identifie le menu qui a été détruit.</span><span class="sxs-lookup"><span data-stu-id="a6ea9-110">The high-order word identifies the menu that was destroyed.</span></span> <span data-ttu-id="a6ea9-111">Actuellement, ce paramètre peut uniquement être **MF \_ SYSMENU** (menu fenêtre).</span><span class="sxs-lookup"><span data-stu-id="a6ea9-111">Currently, this parameter can only be **MF\_SYSMENU** (the window menu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6ea9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a6ea9-112">Remarks</span></span>

<span data-ttu-id="a6ea9-113">Si une application reçoit un message [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) , elle recevra un message **WM \_ UNINITMENUPOPUP** .</span><span class="sxs-lookup"><span data-stu-id="a6ea9-113">If an application receives a [**WM\_INITMENUPOPUP**](wm-initmenupopup.md) message, it will receive a **WM\_UNINITMENUPOPUP** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ea9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6ea9-114">Requirements</span></span>



| <span data-ttu-id="a6ea9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6ea9-115">Requirement</span></span> | <span data-ttu-id="a6ea9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6ea9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ea9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ea9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ea9-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ea9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a6ea9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ea9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ea9-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ea9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a6ea9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6ea9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ea9-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ea9-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ea9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6ea9-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6ea9-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a6ea9-124">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="a6ea9-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a6ea9-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a6ea9-126">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a6ea9-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a6ea9-127">Menus</span><span class="sxs-lookup"><span data-stu-id="a6ea9-127">Menus</span></span>](menus.md)
</dt> </dl>

 

