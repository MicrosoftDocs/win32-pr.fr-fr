---
description: La méthode PossiblyEatMessage transfère les messages du clavier et de la souris à la fenêtre drain de message.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Méthode CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520889"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a><span data-ttu-id="6cfd4-103">Méthode CBaseControlWindow. PossiblyEatMessage</span><span class="sxs-lookup"><span data-stu-id="6cfd4-103">CBaseControlWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="6cfd4-104">La `PossiblyEatMessage` méthode transfère les messages du clavier et de la souris à la fenêtre drain de message.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-104">The `PossiblyEatMessage` method forwards keyboard and mouse messages to the message-drain window.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfd4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cfd4-105">Syntax</span></span>


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="6cfd4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cfd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cfd4-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="6cfd4-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfd4-108">Message de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-108">Window message.</span></span>

</dd> <dt>

<span data-ttu-id="6cfd4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cfd4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfd4-110">Premier paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6cfd4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cfd4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfd4-112">Deuxième paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cfd4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cfd4-113">Return value</span></span>

<span data-ttu-id="6cfd4-114">Retourne la **valeur true** si le message a été transféré à la fenêtre, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-114">Returns **TRUE** if the message was forwarded to the window, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cfd4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6cfd4-115">Remarks</span></span>

<span data-ttu-id="6cfd4-116">La fenêtre drain de message est une fenêtre conçue pour recevoir certains messages de souris et de clavier.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-116">The message-drain window is a window designated to receive certain mouse and keyboard messages.</span></span> <span data-ttu-id="6cfd4-117">Initialement, la fenêtre a la **valeur null**; Il peut être défini en appelant [**CBaseControlWindow ::p ut \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span><span class="sxs-lookup"><span data-stu-id="6cfd4-117">Initially the window is **NULL**; it can be set by calling [**CBaseControlWindow::put\_MessageDrain**](cbasecontrolwindow-put-messagedrain.md).</span></span>

<span data-ttu-id="6cfd4-118">Si la fenêtre drain de message n’a pas la **valeur null**, `PossiblyEatMessage` publie les messages suivants dans cette fenêtre :</span><span class="sxs-lookup"><span data-stu-id="6cfd4-118">If the message-drain window is non-**NULL**, `PossiblyEatMessage` posts the following messages to that window:</span></span>

-   <span data-ttu-id="6cfd4-119">\_caractère WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-119">WM\_CHAR</span></span>
-   <span data-ttu-id="6cfd4-120">\_DEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-120">WM\_DEADCHAR</span></span>
-   <span data-ttu-id="6cfd4-121">WM- \_ touche</span><span class="sxs-lookup"><span data-stu-id="6cfd4-121">WM\_KEYDOWN</span></span>
-   <span data-ttu-id="6cfd4-122">WM \_ KEYUP</span><span class="sxs-lookup"><span data-stu-id="6cfd4-122">WM\_KEYUP</span></span>
-   <span data-ttu-id="6cfd4-123">\_LBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-123">WM\_LBUTTONDBLCLK</span></span>
-   <span data-ttu-id="6cfd4-124">\_LBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-124">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="6cfd4-125">\_LBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-125">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="6cfd4-126">\_MBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-126">WM\_MBUTTONDBLCLK</span></span>
-   <span data-ttu-id="6cfd4-127">\_MBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-127">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="6cfd4-128">\_MBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-128">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="6cfd4-129">\_MOUSEACTIVATE WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-129">WM\_MOUSEACTIVATE</span></span>
-   <span data-ttu-id="6cfd4-130">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="6cfd4-130">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="6cfd4-131">\_NCLBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-131">WM\_NCLBUTTONDBLCLK</span></span>
-   <span data-ttu-id="6cfd4-132">\_NCLBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-132">WM\_NCLBUTTONDOWN</span></span>
-   <span data-ttu-id="6cfd4-133">\_NCLBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-133">WM\_NCLBUTTONUP</span></span>
-   <span data-ttu-id="6cfd4-134">\_NCMBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-134">WM\_NCMBUTTONDBLCLK</span></span>
-   <span data-ttu-id="6cfd4-135">\_NCMBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-135">WM\_NCMBUTTONDOWN</span></span>
-   <span data-ttu-id="6cfd4-136">\_NCMBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-136">WM\_NCMBUTTONUP</span></span>
-   <span data-ttu-id="6cfd4-137">\_NCMOUSEMOVE WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-137">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="6cfd4-138">\_NCRBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-138">WM\_NCRBUTTONDBLCLK</span></span>
-   <span data-ttu-id="6cfd4-139">\_NCRBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-139">WM\_NCRBUTTONDOWN</span></span>
-   <span data-ttu-id="6cfd4-140">\_NCRBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-140">WM\_NCRBUTTONUP</span></span>
-   <span data-ttu-id="6cfd4-141">\_RBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-141">WM\_RBUTTONDBLCLK</span></span>
-   <span data-ttu-id="6cfd4-142">\_RBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-142">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="6cfd4-143">\_RBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-143">WM\_RBUTTONUP</span></span>
-   <span data-ttu-id="6cfd4-144">\_SYSCHAR WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-144">WM\_SYSCHAR</span></span>
-   <span data-ttu-id="6cfd4-145">\_SYSDEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-145">WM\_SYSDEADCHAR</span></span>
-   <span data-ttu-id="6cfd4-146">\_SYSKEYDOWN WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-146">WM\_SYSKEYDOWN</span></span>
-   <span data-ttu-id="6cfd4-147">\_SYSKEYUP WM</span><span class="sxs-lookup"><span data-stu-id="6cfd4-147">WM\_SYSKEYUP</span></span>

<span data-ttu-id="6cfd4-148">Elle ignore les autres messages.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-148">It ignores other messages.</span></span> <span data-ttu-id="6cfd4-149">Si la fenêtre d’écoulement de message est **null**, la méthode ignore tous les messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-149">If the message-drain window is **NULL**, the method ignores all window messages.</span></span> <span data-ttu-id="6cfd4-150">La méthode retourne la **valeur true** si elle publie le message, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-150">The method returns **TRUE** if it posts the message, or **FALSE** otherwise.</span></span> <span data-ttu-id="6cfd4-151">La classe **CBaseWindow** appelle cette méthode lorsqu’elle reçoit un message de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6cfd4-151">The **CBaseWindow** class calls this method when it receives a window message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cfd4-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cfd4-152">Requirements</span></span>



| <span data-ttu-id="6cfd4-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cfd4-153">Requirement</span></span> | <span data-ttu-id="6cfd4-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cfd4-154">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfd4-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cfd4-155">Header</span></span><br/>  | <dl> <span data-ttu-id="6cfd4-156"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd4-156"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6cfd4-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cfd4-157">Library</span></span><br/> | <dl> <span data-ttu-id="6cfd4-158"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd4-158"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cfd4-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cfd4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cfd4-160">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="6cfd4-160">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




