---
description: Envoyé à une fenêtre pour récupérer un handle vers la grande ou la petite icône associée à une fenêtre. Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Message WM_GETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536744"
---
# <a name="wm_geticon-message"></a><span data-ttu-id="7b26f-104">\_Message WM GETICON</span><span class="sxs-lookup"><span data-stu-id="7b26f-104">WM\_GETICON message</span></span>

<span data-ttu-id="7b26f-105">Envoyé à une fenêtre pour récupérer un handle vers la grande ou la petite icône associée à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b26f-105">Sent to a window to retrieve a handle to the large or small icon associated with a window.</span></span> <span data-ttu-id="7b26f-106">Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b26f-106">The system displays the large icon in the ALT+TAB dialog, and the small icon in the window caption.</span></span>

<span data-ttu-id="7b26f-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7b26f-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a><span data-ttu-id="7b26f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b26f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b26f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b26f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b26f-110">Type d’icône récupéré.</span><span class="sxs-lookup"><span data-stu-id="7b26f-110">The type of icon being retrieved.</span></span> <span data-ttu-id="7b26f-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b26f-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7b26f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b26f-112">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="7b26f-113">Signification</span><span class="sxs-lookup"><span data-stu-id="7b26f-113">Meaning</span></span>                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="7b26f-114"><dt>**Icône \_ BIG**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7b26f-114"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="7b26f-115">Récupérez la grande icône pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b26f-115">Retrieve the large icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="7b26f-116"><dt>**Icône \_ PETIT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7b26f-116"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="7b26f-117">Récupérez la petite icône pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b26f-117">Retrieve the small icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <span data-ttu-id="7b26f-118"><dt>**Icône \_ SMALL2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7b26f-118"><dt>**ICON\_SMALL2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7b26f-119">Récupère la petite icône fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="7b26f-119">Retrieves the small icon provided by the application.</span></span> <span data-ttu-id="7b26f-120">Si l’application n’en fournit pas, le système utilise l’icône générée par le système pour cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b26f-120">If the application does not provide one, the system uses the system-generated icon for that window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7b26f-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b26f-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b26f-122">PPP de l’icône en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="7b26f-122">The DPI of the icon being retrieved.</span></span> <span data-ttu-id="7b26f-123">Cela peut être utilisé pour fournir des icônes différentes en fonction de la taille de l’icône.</span><span class="sxs-lookup"><span data-stu-id="7b26f-123">This can be used to provide different icons depending on the icon size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b26f-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b26f-124">Return value</span></span>

<span data-ttu-id="7b26f-125">Type : **HICON**</span><span class="sxs-lookup"><span data-stu-id="7b26f-125">Type: **HICON**</span></span>

<span data-ttu-id="7b26f-126">La valeur de retour est un handle vers la grande ou la petite icône, en fonction de la valeur de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7b26f-126">The return value is a handle to the large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="7b26f-127">Lorsqu’une application reçoit ce message, elle peut renvoyer un descripteur à une grande ou petite icône, ou passer le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="7b26f-127">When an application receives this message, it can return a handle to a large or small icon, or pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b26f-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7b26f-128">Remarks</span></span>

<span data-ttu-id="7b26f-129">Lorsqu’une application reçoit ce message, elle peut renvoyer un descripteur à une grande ou petite icône, ou transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="7b26f-129">When an application receives this message, it can return a handle to a large or small icon, or pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="7b26f-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne un handle vers la grande ou la petite icône associée à la fenêtre, en fonction de la valeur de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7b26f-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns a handle to the large or small icon associated with the window, depending on the value of *wParam*.</span></span>

<span data-ttu-id="7b26f-131">Une fenêtre qui n’a pas d’icône définie explicitement (avec **WM \_ SETICON**) utilise l’icône de la classe de fenêtre inscrite. dans ce cas, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne 0 pour un message **WM \_ GETICON** .</span><span class="sxs-lookup"><span data-stu-id="7b26f-131">A window that has no icon explicitly set (with **WM\_SETICON**) uses the icon for the registered window class, and in this case [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) will return 0 for a **WM\_GETICON** message.</span></span> <span data-ttu-id="7b26f-132">Si l’envoi d’un message **WM \_ GETICON** à une fenêtre retourne 0, essayez ensuite d’appeler la fonction [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7b26f-132">If sending a **WM\_GETICON** message to a window returns 0, next try calling the [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) function for the window.</span></span> <span data-ttu-id="7b26f-133">Si la valeur renvoyée est 0, essayez la fonction [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) .</span><span class="sxs-lookup"><span data-stu-id="7b26f-133">If that returns 0 then try the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b26f-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b26f-134">Requirements</span></span>



| <span data-ttu-id="7b26f-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b26f-135">Requirement</span></span> | <span data-ttu-id="7b26f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b26f-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b26f-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b26f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7b26f-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b26f-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7b26f-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b26f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7b26f-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b26f-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b26f-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b26f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b26f-142"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b26f-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b26f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b26f-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="7b26f-144">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7b26f-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7b26f-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7b26f-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7b26f-146">**\_SETICON WM**</span><span class="sxs-lookup"><span data-stu-id="7b26f-146">**WM\_SETICON**</span></span>](wm-seticon.md)
</dt> <dt>

<span data-ttu-id="7b26f-147">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="7b26f-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7b26f-148">Windows</span><span class="sxs-lookup"><span data-stu-id="7b26f-148">Windows</span></span>](windows.md)
</dt> </dl>

 

 
