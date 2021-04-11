---
UID: ''
title: LowLevelMouseProc fonction de rappel
description: Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée de la souris est sur le point d’être publié dans une file d’attente d’entrée de thread.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "104032043"
---
# <a name="lowlevelmouseproc-function"></a><span data-ttu-id="6f6a7-103">LowLevelMouseProc fonction)</span><span class="sxs-lookup"><span data-stu-id="6f6a7-103">LowLevelMouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="6f6a7-104">Description</span><span class="sxs-lookup"><span data-stu-id="6f6a7-104">Description</span></span>

<span data-ttu-id="6f6a7-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="6f6a7-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="6f6a7-106">Le système appelle cette fonction chaque fois qu’un nouvel événement d’entrée de la souris est sur le point d’être publié dans une file d’attente d’entrée de thread.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-106">The system calls this function every time a new mouse input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="6f6a7-107">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="6f6a7-108">**LowLevelMouseProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-108">**LowLevelMouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="6f6a7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f6a7-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="6f6a7-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="6f6a7-110">nCode [in]</span></span>

<span data-ttu-id="6f6a7-111">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="6f6a7-111">Type: **int**</span></span>

<span data-ttu-id="6f6a7-112">Code que la procédure de raccordement utilise pour déterminer comment traiter le message.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="6f6a7-113">Si *nCode* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="6f6a7-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="6f6a7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f6a7-115">Value</span></span> | <span data-ttu-id="6f6a7-116">Signification</span><span class="sxs-lookup"><span data-stu-id="6f6a7-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="6f6a7-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="6f6a7-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="6f6a7-118">Les paramètres *wParam* et *lParam* contiennent des informations sur un message de souris.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="6f6a7-119">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="6f6a7-119">wParam [in]</span></span>

<span data-ttu-id="6f6a7-120">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="6f6a7-120">Type: **WPARAM**</span></span>

<span data-ttu-id="6f6a7-121">Identificateur du message de la souris.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-121">The identifier of the mouse message.</span></span>
<span data-ttu-id="6f6a7-122">Ce paramètre peut être l’un des messages suivants : [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) ou [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span><span class="sxs-lookup"><span data-stu-id="6f6a7-122">This parameter can be one of the following messages: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) or [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="6f6a7-123">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="6f6a7-123">lParam [in]</span></span>

<span data-ttu-id="6f6a7-124">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="6f6a7-124">Type: **LPARAM**</span></span>

<span data-ttu-id="6f6a7-125">Pointeur vers une structure [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="6f6a7-125">A pointer to an [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="6f6a7-126">Retours</span><span class="sxs-lookup"><span data-stu-id="6f6a7-126">Returns</span></span>

<span data-ttu-id="6f6a7-127">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f6a7-127">Type: **LRESULT**</span></span>

<span data-ttu-id="6f6a7-128">Si *nCode* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-128">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="6f6a7-129">Si *nCode* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est vivement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_MOUSE_LL](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-129">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="6f6a7-130">Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message au reste de la chaîne de raccordement ou à la procédure de fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-130">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6a7-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6f6a7-131">Remarks</span></span>

<span data-ttu-id="6f6a7-132">Une application installe la procédure de raccordement en spécifiant le type de hook **WH_MOUSE_LL** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="6f6a7-132">An application installs the hook procedure by specifying the **WH_MOUSE_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="6f6a7-133">Ce hook est appelé dans le contexte du thread qui l’a installé.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-133">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="6f6a7-134">L’appel est effectué en envoyant un message au thread qui a installé le hook.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-134">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="6f6a7-135">Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-135">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="6f6a7-136">L’entrée de la souris peut provenir du pilote de souris local ou d’appels à la fonction [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .</span><span class="sxs-lookup"><span data-stu-id="6f6a7-136">The mouse input can come from the local mouse driver or from calls to the [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) function.</span></span>
<span data-ttu-id="6f6a7-137">Si l’entrée provient d’un appel à **mouse_event**, l’entrée était « injectée ».</span><span class="sxs-lookup"><span data-stu-id="6f6a7-137">If the input comes from a call to **mouse_event**, the input was "injected".</span></span>
<span data-ttu-id="6f6a7-138">Toutefois, le hook **WH_MOUSE_LL** n’est pas injecté dans un autre processus.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-138">However, the **WH_MOUSE_LL** hook is not injected into another process.</span></span>
<span data-ttu-id="6f6a7-139">Au lieu de cela, le contexte revient au processus qui a installé le hook et il est appelé dans son contexte d’origine.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-139">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="6f6a7-140">Ensuite, le contexte revient à l’application qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-140">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="6f6a7-141">La procédure de raccordement doit traiter un message en moins de temps que l’entrée de données spécifiée dans la valeur **LowLevelHooksTimeout** de la clé de Registre suivante : **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-141">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="6f6a7-142">Cette valeur est exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-142">The value is in milliseconds.</span></span>
<span data-ttu-id="6f6a7-143">Si la procédure de raccordement expire, le système transmet le message au Hook suivant.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-143">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="6f6a7-144">Toutefois, sur Windows 7 et versions ultérieures, le hook est supprimé en mode silencieux sans être appelé.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-144">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="6f6a7-145">L’application n’a aucun moyen de savoir si le hook est supprimé.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-145">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="6f6a7-146">**Remarque :**  Les raccordements de débogage ne peuvent pas suivre ce type de crochets de souris de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-146">**Note:**  Debug hooks cannot track this type of low level mouse hooks.</span></span>
<span data-ttu-id="6f6a7-147">Si l’application doit utiliser des raccordements de bas niveau, elle doit exécuter les raccordements sur un thread dédié qui transmet le travail à un thread de travail, puis retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-147">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="6f6a7-148">Dans la plupart des cas où l’application doit utiliser des raccordements de bas niveau, elle doit surveiller l’entrée brute à la place.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-148">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="6f6a7-149">Cela est dû au fait que l’entrée brute peut surveiller de façon asynchrone les messages de souris et de clavier ciblés pour d’autres threads plus efficacement que les raccordements de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="6f6a7-149">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="6f6a7-150">Pour plus d’informations sur les entrées brutes, consultez [entrée brute](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="6f6a7-150">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="6f6a7-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f6a7-151">See also</span></span>

[<span data-ttu-id="6f6a7-152">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="6f6a7-152">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="6f6a7-153">mouse_event</span><span class="sxs-lookup"><span data-stu-id="6f6a7-153">mouse_event</span></span>](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[<span data-ttu-id="6f6a7-154">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="6f6a7-154">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="6f6a7-155">MSLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="6f6a7-155">MSLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[<span data-ttu-id="6f6a7-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="6f6a7-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="6f6a7-157">WM_LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="6f6a7-157">WM_LBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-lbuttondown)

[<span data-ttu-id="6f6a7-158">WM_LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="6f6a7-158">WM_LBUTTONUP</span></span>](/windows/desktop/inputdev/wm-lbuttonup)

[<span data-ttu-id="6f6a7-159">WM_MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="6f6a7-159">WM_MOUSEMOVE</span></span>](/windows/desktop/inputdev/wm-mousemove)

[<span data-ttu-id="6f6a7-160">WM_MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="6f6a7-160">WM_MOUSEWHEEL</span></span>](/windows/desktop/inputdev/wm-mousewheel)

[<span data-ttu-id="6f6a7-161">WM_RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="6f6a7-161">WM_RBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-rbuttondown)

[<span data-ttu-id="6f6a7-162">WM_RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="6f6a7-162">WM_RBUTTONUP</span></span>](/windows/desktop/inputdev/wm-rbuttonup)

[<span data-ttu-id="6f6a7-163">Hooks</span><span class="sxs-lookup"><span data-stu-id="6f6a7-163">Hooks</span></span>](hooks.md)

[<span data-ttu-id="6f6a7-164">À propos des hooks</span><span class="sxs-lookup"><span data-stu-id="6f6a7-164">About Hooks</span></span>](about-hooks.md)
