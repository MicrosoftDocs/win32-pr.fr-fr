---
UID: ''
title: KeyboardProc fonction de rappel
description: Le système appelle cette fonction pour obtenir une fonction de message et un message clavier à traiter.
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
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "106509645"
---
# <a name="keyboardproc-function"></a><span data-ttu-id="4f9d2-103">KeyboardProc fonction)</span><span class="sxs-lookup"><span data-stu-id="4f9d2-103">KeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="4f9d2-104">Description</span><span class="sxs-lookup"><span data-stu-id="4f9d2-104">Description</span></span>

<span data-ttu-id="4f9d2-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="4f9d2-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="4f9d2-106">Le système appelle cette fonction chaque fois qu’une application appelle la fonction [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) et qu’un message de clavier ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) ou [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) doit être traité.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a keyboard message ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) or [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) to be processed.</span></span>

<span data-ttu-id="4f9d2-107">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="4f9d2-108">**KeyboardProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-108">**KeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="4f9d2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f9d2-109">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="4f9d2-110">Code [in]</span><span class="sxs-lookup"><span data-stu-id="4f9d2-110">code [in]</span></span>

<span data-ttu-id="4f9d2-111">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="4f9d2-111">Type: **int**</span></span>

<span data-ttu-id="4f9d2-112">Code que la procédure de raccordement utilise pour déterminer comment traiter le message.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="4f9d2-113">Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-113">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="4f9d2-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="4f9d2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f9d2-115">Value</span></span> | <span data-ttu-id="4f9d2-116">Signification</span><span class="sxs-lookup"><span data-stu-id="4f9d2-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="4f9d2-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="4f9d2-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="4f9d2-118">Les paramètres *wParam* et *lParam* contiennent des informations sur un message de séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-118">The *wParam* and *lParam* parameters contain information about a keystroke message.</span></span> |
| <span data-ttu-id="4f9d2-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="4f9d2-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="4f9d2-120">Les paramètres *wParam* et *lParam* contiennent des informations sur un message de frappe de touche et le message de frappe n’a pas été supprimé de la file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-120">The *wParam* and *lParam* parameters contain information about a keystroke message, and the keystroke message has not been removed from the message queue.</span></span> <span data-ttu-id="4f9d2-121">(Une application appelée fonction **PeekMessage** , en spécifiant l’indicateur **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="4f9d2-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="4f9d2-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="4f9d2-122">wParam [in]</span></span>

<span data-ttu-id="4f9d2-123">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="4f9d2-123">Type: **WPARAM**</span></span>

<span data-ttu-id="4f9d2-124">Code de la clé [virtuelle](/windows/desktop/inputdev/virtual-key-codes) de la clé qui a généré le message de frappe.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-124">The [virtual-key code](/windows/desktop/inputdev/virtual-key-codes) of the key that generated the keystroke message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="4f9d2-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="4f9d2-125">lParam [in]</span></span>

<span data-ttu-id="4f9d2-126">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="4f9d2-126">Type: **LPARAM**</span></span>

<span data-ttu-id="4f9d2-127">Le nombre de répétitions, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de clé précédent et l’indicateur d’état de transition.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-127">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span>
<span data-ttu-id="4f9d2-128">Pour plus d’informations sur le paramètre *lParam* , consultez [indicateurs de message de frappe](/windows/desktop/inputdev/about-keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="4f9d2-128">For more information about The *lParam* parameter, see [Keystroke Message Flags](/windows/desktop/inputdev/about-keyboard-input).</span></span>
<span data-ttu-id="4f9d2-129">Le tableau suivant décrit les bits de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-129">The following table describes the bits of this value.</span></span>

| <span data-ttu-id="4f9d2-130">Bits</span><span class="sxs-lookup"><span data-stu-id="4f9d2-130">Bits</span></span> | <span data-ttu-id="4f9d2-131">Description</span><span class="sxs-lookup"><span data-stu-id="4f9d2-131">Description</span></span> |
|-------|---------|
| <span data-ttu-id="4f9d2-132">0-15</span><span class="sxs-lookup"><span data-stu-id="4f9d2-132">0-15</span></span> | <span data-ttu-id="4f9d2-133">Nombre de répétitions.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-133">The repeat count.</span></span> <span data-ttu-id="4f9d2-134">La valeur est le nombre de fois où la frappe est répétée à la suite de la touche de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-134">The value is the number of times the keystroke is repeated as a result of the user's holding down the key.</span></span> |
| <span data-ttu-id="4f9d2-135">16-23</span><span class="sxs-lookup"><span data-stu-id="4f9d2-135">16-23</span></span> | <span data-ttu-id="4f9d2-136">Code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-136">The scan code.</span></span> <span data-ttu-id="4f9d2-137">La valeur dépend du fabricant d’ordinateurs OEM.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-137">The value depends on the OEM.</span></span> |
| <span data-ttu-id="4f9d2-138">24</span><span class="sxs-lookup"><span data-stu-id="4f9d2-138">24</span></span> | <span data-ttu-id="4f9d2-139">Indique si la touche est une touche étendue, telle qu’une touche de fonction ou une touche du pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-139">Indicates whether the key is an extended key, such as a function key or a key on the numeric keypad.</span></span> <span data-ttu-id="4f9d2-140">La valeur est 1 si la clé est une clé étendue ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-140">The value is 1 if the key is an extended key; otherwise, it is 0.</span></span> |
| <span data-ttu-id="4f9d2-141">25-28</span><span class="sxs-lookup"><span data-stu-id="4f9d2-141">25-28</span></span> | <span data-ttu-id="4f9d2-142">Réservé.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-142">Reserved.</span></span> |
| <span data-ttu-id="4f9d2-143">29</span><span class="sxs-lookup"><span data-stu-id="4f9d2-143">29</span></span> | <span data-ttu-id="4f9d2-144">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-144">The context code.</span></span> <span data-ttu-id="4f9d2-145">La valeur est 1 si la touche ALT est enfoncée ; Sinon, la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-145">The value is 1 if the ALT key is down; otherwise, it is 0.</span></span> |
| <span data-ttu-id="4f9d2-146">30</span><span class="sxs-lookup"><span data-stu-id="4f9d2-146">30</span></span> | <span data-ttu-id="4f9d2-147">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-147">The previous key state.</span></span> <span data-ttu-id="4f9d2-148">La valeur est 1 si la touche est enfoncée avant l’envoi du message ; la valeur est 0 si la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-148">The value is 1 if the key is down before the message is sent; it is 0 if the key is up.</span></span> |
| <span data-ttu-id="4f9d2-149">31</span><span class="sxs-lookup"><span data-stu-id="4f9d2-149">31</span></span> | <span data-ttu-id="4f9d2-150">État de transition.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-150">The transition state.</span></span> <span data-ttu-id="4f9d2-151">La valeur est 0 si la touche est enfoncée et 1 si elle est libérée.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-151">The value is 0 if the key is being pressed and 1 if it is being released.</span></span> |

## <a name="returns"></a><span data-ttu-id="4f9d2-152">Retours</span><span class="sxs-lookup"><span data-stu-id="4f9d2-152">Returns</span></span>

<span data-ttu-id="4f9d2-153">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="4f9d2-153">Type: **LRESULT**</span></span>

<span data-ttu-id="4f9d2-154">Si le *code* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-154">If *code* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="4f9d2-155">Si le *code* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est fortement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_KEYBOARD](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-155">If *code* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="4f9d2-156">Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message au reste de la chaîne de raccordement ou à la procédure de fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-156">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f9d2-157">Notes</span><span class="sxs-lookup"><span data-stu-id="4f9d2-157">Remarks</span></span>

<span data-ttu-id="4f9d2-158">Une application installe la procédure de raccordement en spécifiant le type de hook **WH_KEYBOARD** et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="4f9d2-158">An application installs the hook procedure by specifying the **WH_KEYBOARD** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="4f9d2-159">Ce hook peut être appelé dans le contexte du thread qui l’a installé.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-159">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="4f9d2-160">L’appel est effectué en envoyant un message au thread qui a installé le hook.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-160">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="4f9d2-161">Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="4f9d2-161">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f9d2-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f9d2-162">See also</span></span>

[<span data-ttu-id="4f9d2-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="4f9d2-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="4f9d2-164">GetMessage</span><span class="sxs-lookup"><span data-stu-id="4f9d2-164">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="4f9d2-165">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="4f9d2-165">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="4f9d2-166">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="4f9d2-166">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="4f9d2-167">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="4f9d2-167">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="4f9d2-168">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="4f9d2-168">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="4f9d2-169">Hooks</span><span class="sxs-lookup"><span data-stu-id="4f9d2-169">Hooks</span></span>](hooks.md)
