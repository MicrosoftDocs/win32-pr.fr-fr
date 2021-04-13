---
title: Modifier les macros de contrôle
description: Modifier les macros de contrôle
ms.assetid: 7c2bb80e-57ca-4d95-a499-b65eefe0352c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795aba77e2f0dc439fdd6bdaab6a4358a15596ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322142"
---
# <a name="edit-control-macros"></a><span data-ttu-id="87cec-103">Modifier les macros de contrôle</span><span class="sxs-lookup"><span data-stu-id="87cec-103">Edit Control Macros</span></span>

## <a name="in-this-section"></a><span data-ttu-id="87cec-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="87cec-104">In this section</span></span>

-   [<span data-ttu-id="87cec-105">**Modifier \_ CanUndo**</span><span class="sxs-lookup"><span data-stu-id="87cec-105">**Edit\_CanUndo**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_canundo)
-   [<span data-ttu-id="87cec-106">**Modifier \_ EmptyUndoBuffer**</span><span class="sxs-lookup"><span data-stu-id="87cec-106">**Edit\_EmptyUndoBuffer**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_emptyundobuffer)
-   [<span data-ttu-id="87cec-107">**Modifier l' \_ activation**</span><span class="sxs-lookup"><span data-stu-id="87cec-107">**Edit\_Enable**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_enable)
-   [<span data-ttu-id="87cec-108">**Modifier \_ FmtLines**</span><span class="sxs-lookup"><span data-stu-id="87cec-108">**Edit\_FmtLines**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_fmtlines)
-   [<span data-ttu-id="87cec-109">**Modifier \_ GetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="87cec-109">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
-   [<span data-ttu-id="87cec-110">**Modifier \_ GetFirstVisibleLine**</span><span class="sxs-lookup"><span data-stu-id="87cec-110">**Edit\_GetFirstVisibleLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getfirstvisibleline)
-   [<span data-ttu-id="87cec-111">**Modifier \_ GetHandle**</span><span class="sxs-lookup"><span data-stu-id="87cec-111">**Edit\_GetHandle**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gethandle)
-   [<span data-ttu-id="87cec-112">**Modifier \_ GetHilite**</span><span class="sxs-lookup"><span data-stu-id="87cec-112">**Edit\_GetHilite**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_gethilite)
-   [<span data-ttu-id="87cec-113">**Modifier \_ getline**</span><span class="sxs-lookup"><span data-stu-id="87cec-113">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
-   [<span data-ttu-id="87cec-114">**Modifier \_ GetLineCount**</span><span class="sxs-lookup"><span data-stu-id="87cec-114">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
-   [<span data-ttu-id="87cec-115">**Modifier \_ GetModify**</span><span class="sxs-lookup"><span data-stu-id="87cec-115">**Edit\_GetModify**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getmodify)
-   [<span data-ttu-id="87cec-116">**Modifier \_ GetPasswordChar**</span><span class="sxs-lookup"><span data-stu-id="87cec-116">**Edit\_GetPasswordChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getpasswordchar)
-   [<span data-ttu-id="87cec-117">**Modifier \_ getRect**</span><span class="sxs-lookup"><span data-stu-id="87cec-117">**Edit\_GetRect**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getrect)
-   [<span data-ttu-id="87cec-118">**Modifier \_ GetSel**</span><span class="sxs-lookup"><span data-stu-id="87cec-118">**Edit\_GetSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getsel)
-   [<span data-ttu-id="87cec-119">**Modifier \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="87cec-119">**Edit\_GetText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gettext)
-   [<span data-ttu-id="87cec-120">**Modifier \_ GetTextLength**</span><span class="sxs-lookup"><span data-stu-id="87cec-120">**Edit\_GetTextLength**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gettextlength)
-   [<span data-ttu-id="87cec-121">**Modifier \_ GetWordBreakProc**</span><span class="sxs-lookup"><span data-stu-id="87cec-121">**Edit\_GetWordBreakProc**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getwordbreakproc)
-   [<span data-ttu-id="87cec-122">**Modifier \_ HideBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="87cec-122">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
-   [<span data-ttu-id="87cec-123">**Modifier \_ LimitText**</span><span class="sxs-lookup"><span data-stu-id="87cec-123">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
-   [<span data-ttu-id="87cec-124">**Modifier \_ LineFromChar**</span><span class="sxs-lookup"><span data-stu-id="87cec-124">**Edit\_LineFromChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_linefromchar)
-   [<span data-ttu-id="87cec-125">**Modifier \_ LineIndex**</span><span class="sxs-lookup"><span data-stu-id="87cec-125">**Edit\_LineIndex**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_lineindex)
-   [<span data-ttu-id="87cec-126">**Modifier \_ LineLength**</span><span class="sxs-lookup"><span data-stu-id="87cec-126">**Edit\_LineLength**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_linelength)
-   [<span data-ttu-id="87cec-127">**Modifier \_ NoSetFocus**</span><span class="sxs-lookup"><span data-stu-id="87cec-127">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
-   [<span data-ttu-id="87cec-128">**Modifier \_ ReplaceSel**</span><span class="sxs-lookup"><span data-stu-id="87cec-128">**Edit\_ReplaceSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_replacesel)
-   [<span data-ttu-id="87cec-129">**Modifier le \_ défilement**</span><span class="sxs-lookup"><span data-stu-id="87cec-129">**Edit\_Scroll**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_scroll)
-   [<span data-ttu-id="87cec-130">**Modifier \_ ScrollCaret**</span><span class="sxs-lookup"><span data-stu-id="87cec-130">**Edit\_ScrollCaret**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_scrollcaret)
-   [<span data-ttu-id="87cec-131">**Modifier \_ SetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="87cec-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
-   [<span data-ttu-id="87cec-132">**Modifier \_ SetCueBannerTextFocused**</span><span class="sxs-lookup"><span data-stu-id="87cec-132">**Edit\_SetCueBannerTextFocused**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertextfocused)
-   [<span data-ttu-id="87cec-133">**Modifier \_ SetHandle**</span><span class="sxs-lookup"><span data-stu-id="87cec-133">**Edit\_SetHandle**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_sethandle)
-   [<span data-ttu-id="87cec-134">**Modifier \_ SetHilite**</span><span class="sxs-lookup"><span data-stu-id="87cec-134">**Edit\_SetHilite**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_sethilite)
-   [<span data-ttu-id="87cec-135">**Modifier \_ SetModify**</span><span class="sxs-lookup"><span data-stu-id="87cec-135">**Edit\_SetModify**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setmodify)
-   [<span data-ttu-id="87cec-136">**Modifier \_ SetPasswordChar**</span><span class="sxs-lookup"><span data-stu-id="87cec-136">**Edit\_SetPasswordChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setpasswordchar)
-   [<span data-ttu-id="87cec-137">**Modifier \_ SetReadOnly**</span><span class="sxs-lookup"><span data-stu-id="87cec-137">**Edit\_SetReadOnly**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setreadonly)
-   [<span data-ttu-id="87cec-138">**Modifier \_ SetRect**</span><span class="sxs-lookup"><span data-stu-id="87cec-138">**Edit\_SetRect**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setrect)
-   [<span data-ttu-id="87cec-139">**Modifier \_ SetRectNoPaint**</span><span class="sxs-lookup"><span data-stu-id="87cec-139">**Edit\_SetRectNoPaint**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setrectnopaint)
-   [<span data-ttu-id="87cec-140">**Modifier \_ SetSel**</span><span class="sxs-lookup"><span data-stu-id="87cec-140">**Edit\_SetSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setsel)
-   [<span data-ttu-id="87cec-141">**Modifier \_ SetTabStops**</span><span class="sxs-lookup"><span data-stu-id="87cec-141">**Edit\_SetTabStops**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_settabstops)
-   [<span data-ttu-id="87cec-142">**Modifier \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="87cec-142">**Edit\_SetText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_settext)
-   [<span data-ttu-id="87cec-143">**Modifier \_ SetWordBreakProc**</span><span class="sxs-lookup"><span data-stu-id="87cec-143">**Edit\_SetWordBreakProc**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setwordbreakproc)
-   [<span data-ttu-id="87cec-144">**Modifier \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="87cec-144">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
-   [<span data-ttu-id="87cec-145">**Modifier \_ TakeFocus**</span><span class="sxs-lookup"><span data-stu-id="87cec-145">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
-   [<span data-ttu-id="87cec-146">**Modifier l' \_ annulation**</span><span class="sxs-lookup"><span data-stu-id="87cec-146">**Edit\_Undo**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_undo)

 

 




