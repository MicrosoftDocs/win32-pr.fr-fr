---
UID: ''
title: MouseProc fonction de rappel
description: Le système appelle cette fonction lorsqu’une application appelle une fonction de message et qu’il y a un message de souris à traiter.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "106512302"
---
# <a name="mouseproc-function"></a><span data-ttu-id="4cbf1-103">MouseProc fonction)</span><span class="sxs-lookup"><span data-stu-id="4cbf1-103">MouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="4cbf1-104">Description</span><span class="sxs-lookup"><span data-stu-id="4cbf1-104">Description</span></span>

<span data-ttu-id="4cbf1-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="4cbf1-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="4cbf1-106">Le système appelle cette fonction chaque fois qu’une application appelle la fonction [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) et qu’un message de souris est traité.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a mouse message to be processed.</span></span>

<span data-ttu-id="4cbf1-107">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="4cbf1-108">**MouseProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-108">**MouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="4cbf1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cbf1-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="4cbf1-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="4cbf1-110">nCode [in]</span></span>

<span data-ttu-id="4cbf1-111">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="4cbf1-111">Type: **int**</span></span>

<span data-ttu-id="4cbf1-112">Code que la procédure de raccordement utilise pour déterminer comment traiter le message.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-112">A code that the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="4cbf1-113">Si *nCode* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="4cbf1-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="4cbf1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cbf1-115">Value</span></span> | <span data-ttu-id="4cbf1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="4cbf1-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="4cbf1-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="4cbf1-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="4cbf1-118">Les paramètres *wParam* et *lParam* contiennent des informations sur un message de souris.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |
| <span data-ttu-id="4cbf1-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="4cbf1-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="4cbf1-120">Les paramètres *wParam* et *lParam* contiennent des informations sur un message de souris, et le message de la souris n’a pas été supprimé de la file d’attente de messages.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-120">The *wParam* and *lParam* parameters contain information about a mouse message, and the mouse message has not been removed from the message queue.</span></span> <span data-ttu-id="4cbf1-121">(Une application appelée fonction **PeekMessage** , en spécifiant l’indicateur **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="4cbf1-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="4cbf1-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="4cbf1-122">wParam [in]</span></span>

<span data-ttu-id="4cbf1-123">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="4cbf1-123">Type: **WPARAM**</span></span>

<span data-ttu-id="4cbf1-124">Identificateur du message de la souris.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-124">The identifier of the mouse message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="4cbf1-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="4cbf1-125">lParam [in]</span></span>

<span data-ttu-id="4cbf1-126">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="4cbf1-126">Type: **LPARAM**</span></span>

<span data-ttu-id="4cbf1-127">Pointeur vers une structure [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .</span><span class="sxs-lookup"><span data-stu-id="4cbf1-127">A pointer to a [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="4cbf1-128">Retours</span><span class="sxs-lookup"><span data-stu-id="4cbf1-128">Returns</span></span>

<span data-ttu-id="4cbf1-129">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="4cbf1-129">Type: **LRESULT**</span></span>

<span data-ttu-id="4cbf1-130">Si *nCode* est inférieur à zéro, la procédure de raccordement doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="4cbf1-131">Si *nCode* est supérieur ou égal à zéro et que la procédure de hook n’a pas traité le message, il est vivement recommandé d’appeler **CallNextHookEx** et de retourner la valeur qu’il retourne ; dans le cas contraire, les autres applications qui ont installé [WH_MOUSE](about-hooks.md) hooks ne recevront pas de notifications de raccordement et pourront se comporter de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="4cbf1-132">Si la procédure de Hook a traité le message, elle peut retourner une valeur différente de zéro pour empêcher le système de transmettre le message à la procédure de fenêtre cible.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cbf1-133">Notes</span><span class="sxs-lookup"><span data-stu-id="4cbf1-133">Remarks</span></span>

<span data-ttu-id="4cbf1-134">Une application installe la procédure de raccordement en spécifiant le type de hook WH_MOUSE et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="4cbf1-134">An application installs the hook procedure by specifying the WH_MOUSE hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="4cbf1-135">La procédure de raccordement ne doit pas installer de [WH_JOURNALPLAYBACK](about-hooks.md) fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-135">The hook procedure must not install a [WH_JOURNALPLAYBACK](about-hooks.md) callback function.</span></span>

<span data-ttu-id="4cbf1-136">Ce hook peut être appelé dans le contexte du thread qui l’a installé.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-136">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="4cbf1-137">L’appel est effectué en envoyant un message au thread qui a installé le hook.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-137">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="4cbf1-138">Par conséquent, le thread qui a installé le hook doit avoir une boucle de message.</span><span class="sxs-lookup"><span data-stu-id="4cbf1-138">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cbf1-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cbf1-139">See also</span></span>

[<span data-ttu-id="4cbf1-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="4cbf1-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="4cbf1-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="4cbf1-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="4cbf1-142">MOUSEHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="4cbf1-142">MOUSEHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[<span data-ttu-id="4cbf1-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="4cbf1-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="4cbf1-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="4cbf1-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="4cbf1-145">Hooks</span><span class="sxs-lookup"><span data-stu-id="4cbf1-145">Hooks</span></span>](hooks.md)

[<span data-ttu-id="4cbf1-146">À propos des hooks</span><span class="sxs-lookup"><span data-stu-id="4cbf1-146">About Hooks</span></span>](about-hooks.md)
