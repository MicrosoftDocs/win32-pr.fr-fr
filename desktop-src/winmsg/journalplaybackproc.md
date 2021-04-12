---
UID: ''
title: JournalPlaybackProc fonction de rappel
description: Lit une série de messages de souris et de clavier enregistrés précédemment.
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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "104381746"
---
# <a name="journalplaybackproc-function"></a><span data-ttu-id="4fbe0-103">JournalPlaybackProc fonction)</span><span class="sxs-lookup"><span data-stu-id="4fbe0-103">JournalPlaybackProc function</span></span>

## <a name="description"></a><span data-ttu-id="4fbe0-104">Description</span><span class="sxs-lookup"><span data-stu-id="4fbe0-104">Description</span></span>

<span data-ttu-id="4fbe0-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="4fbe0-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="4fbe0-106">En règle générale, une application utilise cette fonction pour lire une série de messages de souris et de clavier enregistrés précédemment par la procédure de hook **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="4fbe0-106">Typically, an application uses this function to play back a series of mouse and keyboard messages recorded previously by the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="4fbe0-107">Tant qu’une procédure de hook **JournalPlaybackProc** est installée, l’entrée de souris et de clavier normale est désactivée.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-107">As long as a **JournalPlaybackProc** hook procedure is installed, regular mouse and keyboard input is disabled.</span></span>

<span data-ttu-id="4fbe0-108">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="4fbe0-109">**JournalPlaybackProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-109">**JournalPlaybackProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="4fbe0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fbe0-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="4fbe0-111">Code [in]</span><span class="sxs-lookup"><span data-stu-id="4fbe0-111">code [in]</span></span>

<span data-ttu-id="4fbe0-112">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="4fbe0-112">Type: **int**</span></span>

<span data-ttu-id="4fbe0-113">Code que la procédure de raccordement utilise pour déterminer comment traiter le message.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-113">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="4fbe0-114">Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="4fbe0-115">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="4fbe0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fbe0-116">Value</span></span> | <span data-ttu-id="4fbe0-117">Signification</span><span class="sxs-lookup"><span data-stu-id="4fbe0-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="4fbe0-118">**HC_GETNEXT** 1</span><span class="sxs-lookup"><span data-stu-id="4fbe0-118">**HC_GETNEXT** 1</span></span> | <span data-ttu-id="4fbe0-119">La procédure de raccordement doit copier le message de la souris ou du clavier actuel dans la structure [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) vers laquelle pointe le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="4fbe0-119">The hook procedure must copy the current mouse or keyboard message to the [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure pointed to by the *lParam* parameter.</span></span> |
| <span data-ttu-id="4fbe0-120">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="4fbe0-120">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="4fbe0-121">Une application a appelé la fonction [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) avec wRemoveMsg défini sur **PM_NOREMOVE**, ce qui indique que le message n’est pas supprimé de la file d’attente de messages après le traitement **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="4fbe0-121">An application has called the [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function with wRemoveMsg set to **PM_NOREMOVE**, indicating that the message is not removed from the message queue after **PeekMessage** processing.</span></span> |
| <span data-ttu-id="4fbe0-122">**HC_NOREMOVE** 2</span><span class="sxs-lookup"><span data-stu-id="4fbe0-122">**HC_NOREMOVE** 2</span></span> | <span data-ttu-id="4fbe0-123">La procédure de raccordement doit préparer la copie du message suivant de la souris ou du clavier vers la structure **EVENTMSG** pointée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-123">The hook procedure must prepare to copy the next mouse or keyboard message to the **EVENTMSG** structure pointed to by *lParam*.</span></span> <span data-ttu-id="4fbe0-124">Lors de la réception du code **HC_GETNEXT** , la procédure de raccordement doit copier le message dans la structure.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-124">Upon receiving the **HC_GETNEXT** code, the hook procedure must copy the message to the structure.</span></span> |
| <span data-ttu-id="4fbe0-125">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="4fbe0-125">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="4fbe0-126">Une boîte de dialogue modale du système a été détruite.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-126">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="4fbe0-127">La procédure de raccordement doit reprendre la réécriture des messages.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-127">The hook procedure must resume playing back the messages.</span></span> |
| <span data-ttu-id="4fbe0-128">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="4fbe0-128">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="4fbe0-129">Une boîte de dialogue modale du système s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-129">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="4fbe0-130">Jusqu’à ce que la boîte de dialogue soit détruite, la procédure de raccordement doit cesser de lire les messages.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-130">Until the dialog box is destroyed, the hook procedure must stop playing back messages.</span></span> |

### <a name="wparam"></a><span data-ttu-id="4fbe0-131">wParam</span><span class="sxs-lookup"><span data-stu-id="4fbe0-131">wParam</span></span>

<span data-ttu-id="4fbe0-132">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="4fbe0-132">Type: **WPARAM**</span></span>

<span data-ttu-id="4fbe0-133">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-133">This parameter is not used.</span></span>

### <a name="lparam"></a><span data-ttu-id="4fbe0-134">lParam</span><span class="sxs-lookup"><span data-stu-id="4fbe0-134">lParam</span></span>

<span data-ttu-id="4fbe0-135">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="4fbe0-135">Type: **LPARAM**</span></span>

<span data-ttu-id="4fbe0-136">Pointeur vers une structure **EVENTMSG** qui représente un message en cours de traitement par la procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-136">A pointer to an **EVENTMSG** structure that represents a message being processed by the hook procedure.</span></span>
<span data-ttu-id="4fbe0-137">Ce paramètre est valide uniquement lorsque le paramètre de *code* est **HC_GETNEXT**.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-137">This parameter is valid only when the *code* parameter is **HC_GETNEXT**.</span></span>

## <a name="returns"></a><span data-ttu-id="4fbe0-138">Retours</span><span class="sxs-lookup"><span data-stu-id="4fbe0-138">Returns</span></span>

<span data-ttu-id="4fbe0-139">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="4fbe0-139">Type: **LRESULT**</span></span>

<span data-ttu-id="4fbe0-140">Pour que le système attende avant de traiter le message, la valeur de retour doit correspondre à la durée, en battements d’horloge, que le système doit attendre.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-140">To have the system wait before processing the message, the return value must be the amount of time, in clock ticks, that the system should wait.</span></span>

<span data-ttu-id="4fbe0-141">(Cette valeur peut être calculée en calculant la différence entre les membres de temps dans les messages d’entrée actuels et précédents.)</span><span class="sxs-lookup"><span data-stu-id="4fbe0-141">(This value can be computed by calculating the difference between the time members in the current and previous input messages.)</span></span>

<span data-ttu-id="4fbe0-142">Pour traiter le message immédiatement, la valeur de retour doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-142">To process the message immediately, the return value should be zero.</span></span> <span data-ttu-id="4fbe0-143">La valeur de retour est utilisée uniquement si le code de raccordement est **HC_GETNEXT**; Sinon, il est ignoré.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-143">The return value is used only if the hook code is **HC_GETNEXT**; otherwise, it is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbe0-144">Notes</span><span class="sxs-lookup"><span data-stu-id="4fbe0-144">Remarks</span></span>

<span data-ttu-id="4fbe0-145">Une procédure de hook **JournalPlaybackProc** doit copier un message d’entrée vers le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="4fbe0-145">A **JournalPlaybackProc** hook procedure should copy an input message to The *lParam* parameter.</span></span>
<span data-ttu-id="4fbe0-146">Le message doit avoir été enregistré précédemment à l’aide d’une procédure de hook **JournalRecordProc** , qui ne doit pas modifier le message.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-146">The message must have been previously recorded by using a **JournalRecordProc** hook procedure, which should not modify the message.</span></span>

<span data-ttu-id="4fbe0-147">Pour récupérer le même message à la fois, la procédure de raccordement peut être appelée plusieurs fois avec le paramètre de *code* défini sur **HC_GETNEXT** sans appel intermédiaire avec le *code* défini sur **HC_SKIP**.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-147">To retrieve the same message over and over, the hook procedure can be called several times with the *code* parameter set to **HC_GETNEXT** without an intervening call with *code* set to **HC_SKIP**.</span></span>

<span data-ttu-id="4fbe0-148">Si le *code* est **HC_GETNEXT** et que la valeur de retour est supérieure à zéro, le système se met en veille pendant le nombre de millisecondes spécifié par la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-148">If *code* is **HC_GETNEXT** and the return value is greater than zero, the system sleeps for the number of milliseconds specified by the return value.</span></span> <span data-ttu-id="4fbe0-149">Lorsque le système continue, il appelle à nouveau la procédure de raccordement avec le *code* défini sur **HC_GETNEXT** pour récupérer le même message.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-149">When the system continues, it calls the hook procedure again with *code* set to **HC_GETNEXT** to retrieve the same message.</span></span>
<span data-ttu-id="4fbe0-150">La valeur de retour de ce nouvel appel à **JournalPlaybackProc** doit être égale à zéro ; dans le cas contraire, le système revient en mode veille pendant le nombre de millisecondes spécifié par la valeur de retour, appelle à nouveau **JournalPlaybackProc** , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-150">The return value from this new call to **JournalPlaybackProc** should be zero; otherwise, the system will go back to sleep for the number of milliseconds specified by the return value, call **JournalPlaybackProc** again, and so on.</span></span>
<span data-ttu-id="4fbe0-151">Le système semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-151">The system will appear to be not responding.</span></span>

<span data-ttu-id="4fbe0-152">Contrairement à la plupart des autres procédures de raccordement globales, les procédures de hook **JournalRecordProc** et **JournalPlaybackProc** sont toujours appelées dans le contexte du thread qui définit le hook.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-152">Unlike most other global hook procedures, the **JournalRecordProc** and **JournalPlaybackProc** hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="4fbe0-153">Une fois que la procédure de Hook a retourné le contrôle au système, le message continue à être traité.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-153">After the hook procedure returns control to the system, the message continues to be processed.</span></span> <span data-ttu-id="4fbe0-154">Si le *code* est **HC_SKIP**, la procédure de raccordement doit se préparer à retourner le prochain message d’événement enregistré lors de l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-154">If *code* is **HC_SKIP**, the hook procedure must prepare to return the next recorded event message on its next call.</span></span>

<span data-ttu-id="4fbe0-155">Installez la procédure de hook **JournalPlaybackProc** en spécifiant le type de [WH_JOURNALPLAYBACK](about-hooks.md) et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="4fbe0-155">Install the **JournalPlaybackProc** hook procedure by specifying the [WH_JOURNALPLAYBACK](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="4fbe0-156">Si l’utilisateur appuie sur CTRL + ECHAP ou CTRL + ALT + SUPPR pendant la lecture du journal, le système arrête la lecture, décroche la procédure de lecture du journal et envoie un message d' [WM_CANCELJOURNAL](wm-canceljournal.md) à l’application de journalisation.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-156">If the user presses CTRL+ESC OR CTRL+ALT+DEL during journal playback, the system stops the playback, unhooks the journal playback procedure, and posts a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

<span data-ttu-id="4fbe0-157">Si la procédure de raccordement retourne un message dans la plage **WM_KEYFIRST** à **WM_KEYLAST**, les conditions suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="4fbe0-157">If the hook procedure returns a message in the range **WM_KEYFIRST** to **WM_KEYLAST**, the following conditions apply:</span></span>

* <span data-ttu-id="4fbe0-158">Le membre **param** de la structure **EVENTMSG** spécifie le code de la touche virtuelle de la touche qui a été enfoncée.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-158">The **paramL** member of the **EVENTMSG** structure specifies the virtual key code of the key that was pressed.</span></span>
* <span data-ttu-id="4fbe0-159">Le membre **paramH** de la structure **EVENTMSG** spécifie le code d’analyse.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-159">The **paramH** member of the **EVENTMSG** structure specifies the scan code.</span></span>
* <span data-ttu-id="4fbe0-160">Il n’existe aucun moyen de spécifier un nombre de répétitions.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-160">There's no way to specify a repeat count.</span></span>
<span data-ttu-id="4fbe0-161">L’événement est toujours pris pour représenter un événement clé.</span><span class="sxs-lookup"><span data-stu-id="4fbe0-161">The event is always taken to represent one key event.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fbe0-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fbe0-162">See also</span></span>

[<span data-ttu-id="4fbe0-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="4fbe0-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="4fbe0-164">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="4fbe0-164">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="4fbe0-165">JournalRecordProc</span><span class="sxs-lookup"><span data-stu-id="4fbe0-165">JournalRecordProc</span></span>](journalrecordproc.md)

[<span data-ttu-id="4fbe0-166">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="4fbe0-166">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="4fbe0-167">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="4fbe0-167">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="4fbe0-168">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="4fbe0-168">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="4fbe0-169">Hooks</span><span class="sxs-lookup"><span data-stu-id="4fbe0-169">Hooks</span></span>](hooks.md)
