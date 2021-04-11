---
UID: ''
title: LowLevelKeyboardProc fonction de rappel
description: Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée au clavier est sur le point d’être publié dans une file d’attente d’entrée de thread.
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "104030962"
---
# <a name="lowlevelkeyboardproc-function"></a><span data-ttu-id="a01eb-103">LowLevelKeyboardProc fonction)</span><span class="sxs-lookup"><span data-stu-id="a01eb-103">LowLevelKeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="a01eb-104">Description</span><span class="sxs-lookup"><span data-stu-id="a01eb-104">Description</span></span>

<span data-ttu-id="a01eb-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="a01eb-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="a01eb-106">Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée au clavier est sur le point d’être publié dans une file d’attente d’entrée de thread.</span><span class="sxs-lookup"><span data-stu-id="a01eb-106">The system calls this function every time a new keyboard input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="a01eb-107">**Remarque :**  Lorsque cette fonction de rappel est appelée en réponse à une modification de l’état d’une clé, la fonction de rappel est appelée avant que l’état asynchrone de la clé ne soit mis à jour.</span><span class="sxs-lookup"><span data-stu-id="a01eb-107">**Note:**  When this callback function is called in response to a change in the state of a key, the callback function is called before the asynchronous state of the key is updated.</span></span>
<span data-ttu-id="a01eb-108">Par conséquent, l’état asynchrone de la clé ne peut pas être déterminé en appelant [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) à partir de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="a01eb-108">Consequently, the asynchronous state of the key cannot be determined by calling [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) from within the callback function.</span></span>

<span data-ttu-id="a01eb-109">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="a01eb-109">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="a01eb-110">**LowLevelKeyboardProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="a01eb-110">**LowLevelKeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="a01eb-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a01eb-111">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="a01eb-112">Code [in]</span><span class="sxs-lookup"><span data-stu-id="a01eb-112">code [in]</span></span>

<span data-ttu-id="a01eb-113">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="a01eb-113">Type: **int**</span></span>

<span data-ttu-id="a01eb-114">Code que la procédure de raccordement utilise pour déterminer comment traiter le message.</span><span class="sxs-lookup"><span data-stu-id="a01eb-114">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="a01eb-115">Si *nCode* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="a01eb-115">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="a01eb-116">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a01eb-116">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="a01eb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a01eb-117">Value</span></span> | <span data-ttu-id="a01eb-118">Signification</span><span class="sxs-lookup"><span data-stu-id="a01eb-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="a01eb-119">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="a01eb-119">**HC_ACTION** 0</span></span> | <span data-ttu-id="a01eb-120">Les paramètres *wParam* et *lParam* contiennent des informations sur un message de clavier.</span><span class="sxs-lookup"><span data-stu-id="a01eb-120">The *wParam* and *lParam* parameters contain information about a keyboard message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="a01eb-121">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="a01eb-121">wParam [in]</span></span>

<span data-ttu-id="a01eb-122">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="a01eb-122">Type: **WPARAM**</span></span>

<span data-ttu-id="a01eb-123">Identificateur du message du clavier.</span><span class="sxs-lookup"><span data-stu-id="a01eb-123">The identifier of the keyboard message.</span></span>
<span data-ttu-id="a01eb-124">Ce paramètre peut être l’un des messages suivants : [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)ou [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span><span class="sxs-lookup"><span data-stu-id="a01eb-124">This parameter can be one of the following messages: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="a01eb-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="a01eb-125">lParam [in]</span></span>

<span data-ttu-id="a01eb-126">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="a01eb-126">Type: **LPARAM**</span></span>

<span data-ttu-id="a01eb-127">Pointeur vers une structure [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="a01eb-127">A pointer to a [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="a01eb-128">Retours</span><span class="sxs-lookup"><span data-stu-id="a01eb-128">Returns</span></span>

<span data-ttu-id="a01eb-129">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a01eb-129">Type: **LRESULT**</span></span>

<span data-ttu-id="a01eb-130">Si *nCode* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="a01eb-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="a01eb-131">Si *nCode* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est vivement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_KEYBOARD_LL](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="a01eb-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="a01eb-132">Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message au reste de la chaîne de raccordement ou à la procédure de fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="a01eb-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01eb-133">Notes</span><span class="sxs-lookup"><span data-stu-id="a01eb-133">Remarks</span></span>

<span data-ttu-id="a01eb-134">Une application installe la procédure de raccordement en spécifiant le type de hook **WH_KEYBOARD_LL** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="a01eb-134">An application installs the hook procedure by specifying the **WH_KEYBOARD_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="a01eb-135">Ce hook est appelé dans le contexte du thread qui l’a installé.</span><span class="sxs-lookup"><span data-stu-id="a01eb-135">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="a01eb-136">L’appel est effectué en envoyant un message au thread qui a installé le hook.</span><span class="sxs-lookup"><span data-stu-id="a01eb-136">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="a01eb-137">Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="a01eb-137">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="a01eb-138">L’entrée au clavier peut provenir du pilote de clavier local ou d’appels à la fonction [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .</span><span class="sxs-lookup"><span data-stu-id="a01eb-138">The keyboard input can come from the local keyboard driver or from calls to the [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) function.</span></span>
<span data-ttu-id="a01eb-139">Si l’entrée provient d’un appel à **keybd_event**, l’entrée était « injectée ».</span><span class="sxs-lookup"><span data-stu-id="a01eb-139">If the input comes from a call to **keybd_event**, the input was "injected".</span></span>
<span data-ttu-id="a01eb-140">Toutefois, le hook WH_KEYBOARD_LL n’est pas injecté dans un autre processus.</span><span class="sxs-lookup"><span data-stu-id="a01eb-140">However, the WH_KEYBOARD_LL hook is not injected into another process.</span></span>
<span data-ttu-id="a01eb-141">Au lieu de cela, le contexte revient au processus qui a installé le hook et il est appelé dans son contexte d’origine.</span><span class="sxs-lookup"><span data-stu-id="a01eb-141">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="a01eb-142">Ensuite, le contexte revient à l’application qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="a01eb-142">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="a01eb-143">La procédure de raccordement doit traiter un message en moins de temps que l’entrée de données spécifiée dans la valeur **LowLevelHooksTimeout** de la clé de Registre suivante : **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="a01eb-143">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="a01eb-144">Cette valeur est exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="a01eb-144">The value is in milliseconds.</span></span>
<span data-ttu-id="a01eb-145">Si la procédure de raccordement expire, le système transmet le message au Hook suivant.</span><span class="sxs-lookup"><span data-stu-id="a01eb-145">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="a01eb-146">Toutefois, sur Windows 7 et versions ultérieures, le hook est supprimé en mode silencieux sans être appelé.</span><span class="sxs-lookup"><span data-stu-id="a01eb-146">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="a01eb-147">L’application n’a aucun moyen de savoir si le hook est supprimé.</span><span class="sxs-lookup"><span data-stu-id="a01eb-147">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="a01eb-148">Remarque : les raccordements de débogage ne peuvent pas suivre ce type de hook de clavier de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="a01eb-148">Note:  Debug hooks cannot track this type of low level keyboard hooks.</span></span>
<span data-ttu-id="a01eb-149">Si l’application doit utiliser des raccordements de bas niveau, elle doit exécuter les raccordements sur un thread dédié qui transmet le travail à un thread de travail, puis retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="a01eb-149">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="a01eb-150">Dans la plupart des cas où l’application doit utiliser des raccordements de bas niveau, elle doit surveiller l’entrée brute à la place.</span><span class="sxs-lookup"><span data-stu-id="a01eb-150">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="a01eb-151">Cela est dû au fait que l’entrée brute peut surveiller de façon asynchrone les messages de souris et de clavier ciblés pour d’autres threads plus efficacement que les raccordements de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="a01eb-151">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="a01eb-152">Pour plus d’informations sur les entrées brutes, consultez [entrée brute](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="a01eb-152">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="a01eb-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a01eb-153">See also</span></span>

[<span data-ttu-id="a01eb-154">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="a01eb-154">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="a01eb-155">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="a01eb-155">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="a01eb-156">keybd_event</span><span class="sxs-lookup"><span data-stu-id="a01eb-156">keybd_event</span></span>](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[<span data-ttu-id="a01eb-157">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="a01eb-157">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="a01eb-158">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="a01eb-158">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="a01eb-159">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="a01eb-159">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="a01eb-160">WM_SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="a01eb-160">WM_SYSKEYDOWN</span></span>](/windows/desktop/inputdev/wm-syskeydown)

[<span data-ttu-id="a01eb-161">WM_SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="a01eb-161">WM_SYSKEYUP</span></span>](/windows/desktop/inputdev/wm-syskeyup)

[<span data-ttu-id="a01eb-162">Hooks</span><span class="sxs-lookup"><span data-stu-id="a01eb-162">Hooks</span></span>](hooks.md)

[<span data-ttu-id="a01eb-163">À propos des hooks</span><span class="sxs-lookup"><span data-stu-id="a01eb-163">About Hooks</span></span>](about-hooks.md)
