---
UID: ''
title: ShellProc fonction de rappel
description: La fonction reçoit des notifications d’événements de Shell du système.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "106509432"
---
# <a name="shellproc-function"></a><span data-ttu-id="ec0f4-103">ShellProc fonction)</span><span class="sxs-lookup"><span data-stu-id="ec0f4-103">ShellProc function</span></span>

## <a name="description"></a><span data-ttu-id="ec0f4-104">Description</span><span class="sxs-lookup"><span data-stu-id="ec0f4-104">Description</span></span>

<span data-ttu-id="ec0f4-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="ec0f4-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="ec0f4-106">La fonction reçoit des notifications d’événements de Shell du système.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-106">The function receives notifications of Shell events from the system.</span></span>

<span data-ttu-id="ec0f4-107">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="ec0f4-108">**ShellProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-108">**ShellProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="ec0f4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec0f4-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="ec0f4-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="ec0f4-110">nCode [in]</span></span>

<span data-ttu-id="ec0f4-111">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-111">Type: **int**</span></span>

<span data-ttu-id="ec0f4-112">Code de raccordement.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-112">The hook code.</span></span>
<span data-ttu-id="ec0f4-113">Si *nCode* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="ec0f4-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="ec0f4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec0f4-115">Value</span></span> | <span data-ttu-id="ec0f4-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ec0f4-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="ec0f4-117">**HSHELL_ACCESSIBILITYSTATE** 11</span><span class="sxs-lookup"><span data-stu-id="ec0f4-117">**HSHELL_ACCESSIBILITYSTATE** 11</span></span> | <span data-ttu-id="ec0f4-118">L’état de l’accessibilité a changé.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-118">The accessibility state has changed.</span></span> |
| <span data-ttu-id="ec0f4-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span><span class="sxs-lookup"><span data-stu-id="ec0f4-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span></span> | <span data-ttu-id="ec0f4-120">L’interpréteur de commandes doit activer sa fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-120">The shell should activate its main window.</span></span> |
| <span data-ttu-id="ec0f4-121">**HSHELL_APPCOMMAND** 12</span><span class="sxs-lookup"><span data-stu-id="ec0f4-121">**HSHELL_APPCOMMAND** 12</span></span> | <span data-ttu-id="ec0f4-122">L’utilisateur a terminé un événement d’entrée (par exemple, j’ai appuyé sur un bouton de commande de l’application sur la souris ou sur une touche de commande de l’application sur le clavier) et l’application n’a pas géré le [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message généré par cette entrée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-122">The user completed an input event (for example, pressed an application command button on the mouse or an application command key on the keyboard), and the application did not handle the [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message generated by that input.</span></span> <span data-ttu-id="ec0f4-123">Si la procédure Shell gère le message [WM_COMMAND](/windows/desktop/menurc/wm-command) , elle ne doit pas appeler **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-123">If the Shell procedure handles the [WM_COMMAND](/windows/desktop/menurc/wm-command) message, it should not call **CallNextHookEx**.</span></span> <span data-ttu-id="ec0f4-124">Pour plus d’informations, consultez la section valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-124">See the Return Value section for more information.</span></span> |
| <span data-ttu-id="ec0f4-125">**HSHELL_GETMINRECT** 5</span><span class="sxs-lookup"><span data-stu-id="ec0f4-125">**HSHELL_GETMINRECT** 5</span></span> | <span data-ttu-id="ec0f4-126">Une fenêtre est réduite ou agrandie.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-126">A window is being minimized or maximized.</span></span> <span data-ttu-id="ec0f4-127">Le système a besoin des coordonnées du rectangle réduit pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-127">The system needs the coordinates of the minimized rectangle for the window.</span></span> |
| <span data-ttu-id="ec0f4-128">**HSHELL_LANGUAGE** 8</span><span class="sxs-lookup"><span data-stu-id="ec0f4-128">**HSHELL_LANGUAGE** 8</span></span> | <span data-ttu-id="ec0f4-129">La langue du clavier a été modifiée ou une nouvelle disposition du clavier a été chargée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-129">Keyboard language was changed or a new keyboard layout was loaded.</span></span> |
| <span data-ttu-id="ec0f4-130">**HSHELL_REDRAW** 6</span><span class="sxs-lookup"><span data-stu-id="ec0f4-130">**HSHELL_REDRAW** 6</span></span> | <span data-ttu-id="ec0f4-131">Le titre d’une fenêtre dans la barre des tâches a été redessiné.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-131">The title of a window in the task bar has been redrawn.</span></span> |
| <span data-ttu-id="ec0f4-132">**HSHELL_TASKMAN** 7</span><span class="sxs-lookup"><span data-stu-id="ec0f4-132">**HSHELL_TASKMAN** 7</span></span> | <span data-ttu-id="ec0f4-133">L’utilisateur a sélectionné la liste des tâches.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-133">The user has selected the task list.</span></span> <span data-ttu-id="ec0f4-134">Une application d’environnement qui fournit une liste de tâches doit retourner la **valeur true** pour empêcher Windows de démarrer sa liste de tâches.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-134">A shell application that provides a task list should return **TRUE** to prevent Windows from starting its task list.</span></span> |
| <span data-ttu-id="ec0f4-135">**HSHELL_WINDOWACTIVATED** 4</span><span class="sxs-lookup"><span data-stu-id="ec0f4-135">**HSHELL_WINDOWACTIVATED** 4</span></span> | <span data-ttu-id="ec0f4-136">L’activation a été remplacée par une nouvelle fenêtre de niveau supérieur, sans propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-136">The activation has changed to a different top-level, unowned window.</span></span> |
| <span data-ttu-id="ec0f4-137">**HSHELL_WINDOWCREATED** 1</span><span class="sxs-lookup"><span data-stu-id="ec0f4-137">**HSHELL_WINDOWCREATED** 1</span></span> | <span data-ttu-id="ec0f4-138">Une fenêtre de niveau supérieur sans propriétaire a été créée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-138">A top-level, unowned window has been created.</span></span> <span data-ttu-id="ec0f4-139">La fenêtre existe lorsque le système appelle ce hook.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-139">The window exists when the system calls this hook.</span></span> |
| <span data-ttu-id="ec0f4-140">**HSHELL_WINDOWDESTROYED** 2</span><span class="sxs-lookup"><span data-stu-id="ec0f4-140">**HSHELL_WINDOWDESTROYED** 2</span></span> | <span data-ttu-id="ec0f4-141">Une fenêtre de niveau supérieur, sans propriétaire, va être détruite.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-141">A top-level, unowned window is about to be destroyed.</span></span> <span data-ttu-id="ec0f4-142">La fenêtre existe toujours lorsque le système appelle ce hook.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-142">The window still exists when the system calls this hook.</span></span> |
| <span data-ttu-id="ec0f4-143">**HSHELL_WINDOWREPLACED** 13</span><span class="sxs-lookup"><span data-stu-id="ec0f4-143">**HSHELL_WINDOWREPLACED** 13</span></span> | <span data-ttu-id="ec0f4-144">Une fenêtre de niveau supérieur est remplacée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-144">A top-level window is being replaced.</span></span> <span data-ttu-id="ec0f4-145">La fenêtre existe lorsque le système appelle ce hook.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-145">The window exists when the system calls this hook.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="ec0f4-146">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="ec0f4-146">wParam [in]</span></span>

<span data-ttu-id="ec0f4-147">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-147">Type: **WPARAM**</span></span>

<span data-ttu-id="ec0f4-148">Ce paramètre dépend de la valeur du paramètre *nCode* , comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-148">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="ec0f4-149">nCode</span><span class="sxs-lookup"><span data-stu-id="ec0f4-149">nCode</span></span> | <span data-ttu-id="ec0f4-150">wParam</span><span class="sxs-lookup"><span data-stu-id="ec0f4-150">wParam</span></span> |
|-------|---------|
| <span data-ttu-id="ec0f4-151">**HSHELL_ACCESSIBILITYSTATE**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-151">**HSHELL_ACCESSIBILITYSTATE**</span></span> | <span data-ttu-id="ec0f4-152">Indique quelle fonctionnalité d’accessibilité a changé d’État.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-152">Indicates which accessibility feature has changed state.</span></span> <span data-ttu-id="ec0f4-153">Cette valeur est l’une des suivantes : **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** ou **ACCESS_STICKYKEYS**.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-153">This value is one of the following: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS**, or **ACCESS_STICKYKEYS**.</span></span> |
| <span data-ttu-id="ec0f4-154">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-154">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="ec0f4-155">Indique où le message de **WM_APPCOMMAND** a été envoyé à l’origine ; par exemple, le handle d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-155">Indicates where the **WM_APPCOMMAND** message was originally sent; for example, the handle to a window.</span></span> <span data-ttu-id="ec0f4-156">Pour plus d’informations, consultez paramètre cmd dans **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-156">For more information, see cmd parameter in **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="ec0f4-157">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-157">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="ec0f4-158">Handle vers la fenêtre réduite ou agrandie.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-158">A handle to the minimized or maximized window.</span></span> |
| <span data-ttu-id="ec0f4-159">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-159">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="ec0f4-160">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-160">A handle to the window.</span></span> |
| <span data-ttu-id="ec0f4-161">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-161">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="ec0f4-162">Handle de la fenêtre redessinée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-162">A handle to the redrawn window.</span></span> |
| <span data-ttu-id="ec0f4-163">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-163">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="ec0f4-164">Handle de la fenêtre activée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-164">A handle to the activated window.</span></span> |
| <span data-ttu-id="ec0f4-165">**HSHELL_WINDOWCREATED**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-165">**HSHELL_WINDOWCREATED**</span></span> | <span data-ttu-id="ec0f4-166">Handle de la fenêtre créée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-166">A handle to the created window.</span></span> |
| <span data-ttu-id="ec0f4-167">**HSHELL_WINDOWDESTROYED**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-167">**HSHELL_WINDOWDESTROYED**</span></span> | <span data-ttu-id="ec0f4-168">Handle vers la fenêtre détruite.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-168">A handle to the destroyed window.</span></span> |
| <span data-ttu-id="ec0f4-169">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-169">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="ec0f4-170">Handle de la fenêtre qui est remplacée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-170">A handle to the window being replaced.</span></span> <span data-ttu-id="ec0f4-171">Windows 2000 : non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-171">Windows 2000:  Not supported.</span></span> |

### <a name="lparam-in"></a><span data-ttu-id="ec0f4-172">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="ec0f4-172">lParam [in]</span></span>

<span data-ttu-id="ec0f4-173">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-173">Type: **LPARAM**</span></span>

<span data-ttu-id="ec0f4-174">Ce paramètre dépend de la valeur du paramètre *nCode* , comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-174">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="ec0f4-175">nCode</span><span class="sxs-lookup"><span data-stu-id="ec0f4-175">nCode</span></span> | <span data-ttu-id="ec0f4-176">lParam</span><span class="sxs-lookup"><span data-stu-id="ec0f4-176">lParam</span></span> |
|-------|---------|
| <span data-ttu-id="ec0f4-177">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-177">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="ec0f4-178">`GET_APPCOMMAND_LPARAM(lParam)` commande d’application correspondant à l’événement d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-178">`GET_APPCOMMAND_LPARAM(lParam)` is the application command corresponding to the input event.</span></span> <span data-ttu-id="ec0f4-179">`GET_DEVICE_LPARAM(lParam)` indique ce qui a généré l’événement d’entrée ; par exemple, la souris ou le clavier.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-179">`GET_DEVICE_LPARAM(lParam)` indicates what generated the input event; for example, the mouse or keyboard.</span></span> <span data-ttu-id="ec0f4-180">Pour plus d’informations, consultez la description du paramètre *uDevice* sous **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-180">For more information, see the *uDevice* parameter description under **WM_APPCOMMAND**.</span></span> <span data-ttu-id="ec0f4-181">`GET_FLAGS_LPARAM(lParam)` dépend de la valeur de *cmd* dans **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-181">`GET_FLAGS_LPARAM(lParam)` depends on the value of *cmd* in **WM_APPCOMMAND**.</span></span> <span data-ttu-id="ec0f4-182">Par exemple, il peut indiquer quelles clés virtuelles ont été conservées lors de l’envoi de l' **WM_APPCOMMAND** message.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-182">For example, it might indicate which virtual keys were held down when the **WM_APPCOMMAND** message was originally sent.</span></span> <span data-ttu-id="ec0f4-183">Pour plus d’informations, consultez le paramètre de description *dwCmdFlags* sous **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-183">For more information, see the *dwCmdFlags* description parameter under **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="ec0f4-184">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-184">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="ec0f4-185">Pointeur vers une structure [Rect](/previous-versions/dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ec0f4-185">A pointer to a [RECT](/previous-versions/dd162897(v=vs.85)) structure.</span></span> |
| <span data-ttu-id="ec0f4-186">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-186">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="ec0f4-187">Handle d’une disposition de clavier.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-187">A handle to a keyboard layout.</span></span> |
| <span data-ttu-id="ec0f4-188">**HSHELL_MONITORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-188">**HSHELL_MONITORCHANGED**</span></span> | <span data-ttu-id="ec0f4-189">Handle vers la fenêtre qui a été déplacée vers un autre moniteur.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-189">A handle to the window that moved to a different monitor.</span></span> |
| <span data-ttu-id="ec0f4-190">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-190">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="ec0f4-191">La valeur est **true** si la fenêtre clignote, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-191">The value is **TRUE** if the window is flashing, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="ec0f4-192">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-192">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="ec0f4-193">La valeur est TRUE si la fenêtre est en mode plein écran, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-193">The value is TRUE if the window is in full-screen mode, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="ec0f4-194">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-194">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="ec0f4-195">Handle de la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-195">A handle to the new window.</span></span> <span data-ttu-id="ec0f4-196">Windows 2000 : non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-196">Windows 2000:  Not supported.</span></span> |

## <a name="returns"></a><span data-ttu-id="ec0f4-197">Retours</span><span class="sxs-lookup"><span data-stu-id="ec0f4-197">Returns</span></span>

<span data-ttu-id="ec0f4-198">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-198">Type: **LRESULT**</span></span>

<span data-ttu-id="ec0f4-199">La valeur de retour doit être égale à zéro, sauf si la valeur de nCode est **HSHELL_APPCOMMAND** et que la procédure Shell gère le message **WM_COMMAND** .</span><span class="sxs-lookup"><span data-stu-id="ec0f4-199">The return value should be zero unless the value of nCode is **HSHELL_APPCOMMAND** and the shell procedure handles the **WM_COMMAND** message.</span></span>
<span data-ttu-id="ec0f4-200">Dans ce cas, le retour doit être différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="ec0f4-200">In this case, the return should be nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0f4-201">Notes</span><span class="sxs-lookup"><span data-stu-id="ec0f4-201">Remarks</span></span>

<span data-ttu-id="ec0f4-202">Installez cette procédure de hook en spécifiant le type de hook [WH_SHELL](about-hooks.md) et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="ec0f4-202">Install this hook procedure by specifying the [WH_SHELL](about-hooks.md) hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec0f4-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec0f4-203">See also</span></span>

[<span data-ttu-id="ec0f4-204">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="ec0f4-204">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="ec0f4-205">SendMessage</span><span class="sxs-lookup"><span data-stu-id="ec0f4-205">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[<span data-ttu-id="ec0f4-206">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="ec0f4-206">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="ec0f4-207">WM_APPCOMMAND</span><span class="sxs-lookup"><span data-stu-id="ec0f4-207">WM_APPCOMMAND</span></span>](/windows/desktop/inputdev/wm-appcommand)

[<span data-ttu-id="ec0f4-208">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="ec0f4-208">WM_COMMAND</span></span>](/windows/desktop/menurc/wm-command)

[<span data-ttu-id="ec0f4-209">Hooks</span><span class="sxs-lookup"><span data-stu-id="ec0f4-209">Hooks</span></span>](hooks.md)
