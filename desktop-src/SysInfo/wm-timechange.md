---
description: Message envoyé chaque fois qu’une modification est apportée à l’heure système.
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: Message WM_TIMECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d43bb5cd4284813c45ab074a93a9cd9699883aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534467"
---
# <a name="wm_timechange-message"></a><span data-ttu-id="89a2c-103">\_Message WM TIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="89a2c-103">WM\_TIMECHANGE message</span></span>

<span data-ttu-id="89a2c-104">Message envoyé chaque fois qu’une modification est apportée à l’heure système.</span><span class="sxs-lookup"><span data-stu-id="89a2c-104">A message that is sent whenever there is a change in the system time.</span></span>

<span data-ttu-id="89a2c-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="89a2c-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a><span data-ttu-id="89a2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89a2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89a2c-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="89a2c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="89a2c-108">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="89a2c-108">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="89a2c-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="89a2c-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="89a2c-110">**WM \_ Identificateur TIMECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="89a2c-110">**WM\_TIMECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="89a2c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89a2c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89a2c-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="89a2c-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="89a2c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89a2c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89a2c-114">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="89a2c-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89a2c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89a2c-115">Return value</span></span>

<span data-ttu-id="89a2c-116">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="89a2c-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="89a2c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="89a2c-117">Remarks</span></span>

<span data-ttu-id="89a2c-118">Une application ne doit pas diffuser ce message, car le système diffuse ce message lorsque l’application modifie l’heure système.</span><span class="sxs-lookup"><span data-stu-id="89a2c-118">An application should not broadcast this message, because the system will broadcast this message when the application changes the system time.</span></span>

## <a name="requirements"></a><span data-ttu-id="89a2c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89a2c-119">Requirements</span></span>



| <span data-ttu-id="89a2c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89a2c-120">Requirement</span></span> | <span data-ttu-id="89a2c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="89a2c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a2c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89a2c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89a2c-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89a2c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="89a2c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89a2c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89a2c-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89a2c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89a2c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="89a2c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89a2c-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89a2c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89a2c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89a2c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a2c-129">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="89a2c-129">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

