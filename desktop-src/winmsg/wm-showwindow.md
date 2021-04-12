---
description: Envoyé à une fenêtre lorsque la fenêtre va être masquée ou affichée.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Message WM_SHOWWINDOW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319205"
---
# <a name="wm_showwindow-message"></a><span data-ttu-id="47871-103">\_Message ShowWindow WM</span><span class="sxs-lookup"><span data-stu-id="47871-103">WM\_SHOWWINDOW message</span></span>

<span data-ttu-id="47871-104">Envoyé à une fenêtre lorsque la fenêtre va être masquée ou affichée.</span><span class="sxs-lookup"><span data-stu-id="47871-104">Sent to a window when the window is about to be hidden or shown.</span></span>

<span data-ttu-id="47871-105">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="47871-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a><span data-ttu-id="47871-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47871-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="47871-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47871-108">Indique si une fenêtre est affichée.</span><span class="sxs-lookup"><span data-stu-id="47871-108">Indicates whether a window is being shown.</span></span> <span data-ttu-id="47871-109">Si *wParam* a la **valeur true**, la fenêtre est affichée.</span><span class="sxs-lookup"><span data-stu-id="47871-109">If *wParam* is **TRUE**, the window is being shown.</span></span> <span data-ttu-id="47871-110">Si *wParam* a la **valeur false**, la fenêtre est masquée.</span><span class="sxs-lookup"><span data-stu-id="47871-110">If *wParam* is **FALSE**, the window is being hidden.</span></span>

</dd> <dt>

<span data-ttu-id="47871-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47871-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47871-112">État de la fenêtre affichée.</span><span class="sxs-lookup"><span data-stu-id="47871-112">The status of the window being shown.</span></span> <span data-ttu-id="47871-113">Si *lParam* est égal à zéro, le message a été envoyé en raison d’un appel à la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ; dans le cas contraire, *lParam* est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="47871-113">If *lParam* is zero, the message was sent because of a call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function; otherwise, *lParam* is one of the following values.</span></span>



| <span data-ttu-id="47871-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="47871-114">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="47871-115">Signification</span><span class="sxs-lookup"><span data-stu-id="47871-115">Meaning</span></span>                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <span data-ttu-id="47871-116"><dt>**Logiciels \_ OTHERUNZOOM**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="47871-116"><dt>**SW\_OTHERUNZOOM**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="47871-117">La fenêtre est en cours de récupération, car une fenêtre agrandie a été restaurée ou réduite.</span><span class="sxs-lookup"><span data-stu-id="47871-117">The window is being uncovered because a maximize window was restored or minimized.</span></span><br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <span data-ttu-id="47871-118"><dt>**Logiciels \_ OTHERZOOM**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="47871-118"><dt>**SW\_OTHERZOOM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="47871-119">La fenêtre est couverte par une autre fenêtre qui a été agrandie.</span><span class="sxs-lookup"><span data-stu-id="47871-119">The window is being covered by another window that has been maximized.</span></span><br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <span data-ttu-id="47871-120"><dt>**Logiciels \_ PARENTCLOSING**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="47871-120"><dt>**SW\_PARENTCLOSING**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="47871-121">La fenêtre propriétaire de la fenêtre est réduite.</span><span class="sxs-lookup"><span data-stu-id="47871-121">The window's owner window is being minimized.</span></span><br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <span data-ttu-id="47871-122"><dt>**Logiciels \_ PARENTOPENING**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="47871-122"><dt>**SW\_PARENTOPENING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="47871-123">La fenêtre propriétaire de la fenêtre est en cours de restauration.</span><span class="sxs-lookup"><span data-stu-id="47871-123">The window's owner window is being restored.</span></span><br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47871-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47871-124">Return value</span></span>

<span data-ttu-id="47871-125">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="47871-125">Type: **LRESULT**</span></span>

<span data-ttu-id="47871-126">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="47871-126">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="47871-127">Notes</span><span class="sxs-lookup"><span data-stu-id="47871-127">Remarks</span></span>

<span data-ttu-id="47871-128">La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) masque ou affiche la fenêtre, comme spécifié par le message.</span><span class="sxs-lookup"><span data-stu-id="47871-128">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function hides or shows the window, as specified by the message.</span></span> <span data-ttu-id="47871-129">Si une fenêtre a le style [**WS \_ visible**](window-styles.md) lors de sa création, la fenêtre reçoit ce message après sa création, mais avant son affichage.</span><span class="sxs-lookup"><span data-stu-id="47871-129">If a window has the [**WS\_VISIBLE**](window-styles.md) style when it is created, the window receives this message after it is created, but before it is displayed.</span></span> <span data-ttu-id="47871-130">Une fenêtre reçoit également ce message lorsque son état de visibilité est modifié par la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ou [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) .</span><span class="sxs-lookup"><span data-stu-id="47871-130">A window also receives this message when its visibility state is changed by the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) or [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) function.</span></span>

<span data-ttu-id="47871-131">Le message **WM \_ ShowWindow** n’est pas envoyé dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="47871-131">The **WM\_SHOWWINDOW** message is not sent under the following circumstances:</span></span>

-   <span data-ttu-id="47871-132">Quand une fenêtre de niveau supérieur, avec chevauchement est créée avec le style [**WS \_ Maximize**](window-styles.md) ou **WS \_ Minimize** .</span><span class="sxs-lookup"><span data-stu-id="47871-132">When a top-level, overlapped window is created with the [**WS\_MAXIMIZE**](window-styles.md) or **WS\_MINIMIZE** style.</span></span>
-   <span data-ttu-id="47871-133">Lorsque l’indicateur **SW \_ SHOWNORMAL** est spécifié dans l’appel à la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="47871-133">When the **SW\_SHOWNORMAL** flag is specified in the call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="47871-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47871-134">Requirements</span></span>



| <span data-ttu-id="47871-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47871-135">Requirement</span></span> | <span data-ttu-id="47871-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="47871-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47871-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47871-137">Minimum supported client</span></span><br/> | <span data-ttu-id="47871-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47871-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="47871-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47871-139">Minimum supported server</span></span><br/> | <span data-ttu-id="47871-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47871-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="47871-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="47871-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="47871-142"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47871-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47871-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47871-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="47871-144">**Référence**</span><span class="sxs-lookup"><span data-stu-id="47871-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="47871-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="47871-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="47871-146">**ShowOwnedPopups**</span><span class="sxs-lookup"><span data-stu-id="47871-146">**ShowOwnedPopups**</span></span>](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[<span data-ttu-id="47871-147">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="47871-147">**ShowWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

<span data-ttu-id="47871-148">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="47871-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="47871-149">Windows</span><span class="sxs-lookup"><span data-stu-id="47871-149">Windows</span></span>](windows.md)
</dt> </dl>

 

 
