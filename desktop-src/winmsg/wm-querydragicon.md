---
description: Envoyé à une fenêtre réduite (sous forme).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Message WM_QUERYDRAGICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319209"
---
# <a name="wm_querydragicon-message"></a><span data-ttu-id="a75bf-103">\_Message WM QUERYDRAGICON</span><span class="sxs-lookup"><span data-stu-id="a75bf-103">WM\_QUERYDRAGICON message</span></span>

<span data-ttu-id="a75bf-104">Envoyé à une fenêtre réduite (sous forme).</span><span class="sxs-lookup"><span data-stu-id="a75bf-104">Sent to a minimized (iconic) window.</span></span> <span data-ttu-id="a75bf-105">La fenêtre va être déplacée par l’utilisateur mais n’a pas d’icône définie pour sa classe.</span><span class="sxs-lookup"><span data-stu-id="a75bf-105">The window is about to be dragged by the user but does not have an icon defined for its class.</span></span> <span data-ttu-id="a75bf-106">Une application peut retourner un handle à une icône ou un curseur.</span><span class="sxs-lookup"><span data-stu-id="a75bf-106">An application can return a handle to an icon or cursor.</span></span> <span data-ttu-id="a75bf-107">Le système affiche ce curseur ou cette icône lorsque l’utilisateur fait glisser l’icône.</span><span class="sxs-lookup"><span data-stu-id="a75bf-107">The system displays this cursor or icon while the user drags the icon.</span></span>

<span data-ttu-id="a75bf-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a75bf-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a><span data-ttu-id="a75bf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a75bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75bf-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a75bf-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a75bf-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a75bf-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a75bf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a75bf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a75bf-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="a75bf-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75bf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a75bf-114">Return value</span></span>

<span data-ttu-id="a75bf-115">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a75bf-115">Type: **LRESULT**</span></span>

<span data-ttu-id="a75bf-116">Une application doit retourner un handle à un curseur ou une icône que le système doit afficher lorsque l’utilisateur fait glisser l’icône.</span><span class="sxs-lookup"><span data-stu-id="a75bf-116">An application should return a handle to a cursor or icon that the system is to display while the user drags the icon.</span></span> <span data-ttu-id="a75bf-117">Le curseur ou l’icône doit être compatible avec la résolution du pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a75bf-117">The cursor or icon must be compatible with the display driver's resolution.</span></span> <span data-ttu-id="a75bf-118">Si l’application retourne la **valeur null**, le système affiche le curseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a75bf-118">If the application returns **NULL**, the system displays the default cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75bf-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a75bf-119">Remarks</span></span>

<span data-ttu-id="a75bf-120">Quand l’utilisateur fait glisser l’icône d’une fenêtre sans icône de classe, le système remplace l’icône par un curseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a75bf-120">When the user drags the icon of a window without a class icon, the system replaces the icon with a default cursor.</span></span> <span data-ttu-id="a75bf-121">Si l’application requiert un curseur différent pour être affichée pendant le déplacement, elle doit retourner un handle au curseur ou à une icône compatible avec la résolution du pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a75bf-121">If the application requires a different cursor to be displayed during dragging, it must return a handle to the cursor or icon compatible with the display driver's resolution.</span></span> <span data-ttu-id="a75bf-122">Si une application retourne un handle à un curseur ou une icône de couleur, le système convertit le curseur ou l’icône en noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="a75bf-122">If an application returns a handle to a color cursor or icon, the system converts the cursor or icon to black and white.</span></span> <span data-ttu-id="a75bf-123">L’application peut appeler la fonction [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) ou [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) pour charger un curseur ou une icône à partir des ressources dans son fichier exécutable (. exe) et pour récupérer ce handle.</span><span class="sxs-lookup"><span data-stu-id="a75bf-123">The application can call the [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) or [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to load a cursor or icon from the resources in its executable (.exe) file and to retrieve this handle.</span></span>

<span data-ttu-id="a75bf-124">Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement.</span><span class="sxs-lookup"><span data-stu-id="a75bf-124">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="a75bf-125">La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a75bf-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75bf-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a75bf-126">Requirements</span></span>



| <span data-ttu-id="a75bf-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a75bf-127">Requirement</span></span> | <span data-ttu-id="a75bf-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a75bf-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a75bf-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a75bf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a75bf-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a75bf-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a75bf-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a75bf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a75bf-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a75bf-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a75bf-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a75bf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a75bf-134"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a75bf-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a75bf-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a75bf-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a75bf-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a75bf-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a75bf-137">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="a75bf-137">**LoadCursor**</span></span>](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[<span data-ttu-id="a75bf-138">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="a75bf-138">**LoadIcon**</span></span>](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

<span data-ttu-id="a75bf-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a75bf-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a75bf-140">Windows</span><span class="sxs-lookup"><span data-stu-id="a75bf-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
