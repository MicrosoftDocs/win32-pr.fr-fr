---
UID: ''
title: JournalRecordProc fonction de rappel
description: La fonction enregistre les messages que le système supprime de la file d’attente des messages système.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "103940785"
---
# <a name="journalrecordproc-function"></a><span data-ttu-id="1e20d-103">JournalRecordProc fonction)</span><span class="sxs-lookup"><span data-stu-id="1e20d-103">JournalRecordProc function</span></span>

## <a name="description"></a><span data-ttu-id="1e20d-104">Description</span><span class="sxs-lookup"><span data-stu-id="1e20d-104">Description</span></span>

<span data-ttu-id="1e20d-105">Fonction de rappel définie par l’application ou définie par la Bibliothèque utilisée avec la fonction [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="1e20d-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="1e20d-106">La fonction enregistre les messages que le système supprime de la file d’attente des messages système.</span><span class="sxs-lookup"><span data-stu-id="1e20d-106">The function records messages the system removes from the system message queue.</span></span>
<span data-ttu-id="1e20d-107">Plus tard, une application peut utiliser une procédure de hook [JournalPlaybackProc](journalplaybackproc.md) pour lire les messages.</span><span class="sxs-lookup"><span data-stu-id="1e20d-107">Later, an application can use a [JournalPlaybackProc](journalplaybackproc.md) hook procedure to play back the messages.</span></span>

<span data-ttu-id="1e20d-108">Le type **HOOKPROC** définit un pointeur vers cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1e20d-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="1e20d-109">**JournalRecordProc** est un espace réservé pour le nom de la fonction définie par l’application ou par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1e20d-109">**JournalRecordProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="1e20d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e20d-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="1e20d-111">Code [in]</span><span class="sxs-lookup"><span data-stu-id="1e20d-111">code [in]</span></span>

<span data-ttu-id="1e20d-112">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="1e20d-112">Type: **int**</span></span>

<span data-ttu-id="1e20d-113">Spécifie comment traiter le message.</span><span class="sxs-lookup"><span data-stu-id="1e20d-113">Specifies how to process the message.</span></span>
<span data-ttu-id="1e20d-114">Si le *code* est inférieur à zéro, la procédure de raccordement doit passer le message à la fonction [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sans traitement supplémentaire et doit retourner la valeur retournée par **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="1e20d-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="1e20d-115">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e20d-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="1e20d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e20d-116">Value</span></span> | <span data-ttu-id="1e20d-117">Signification</span><span class="sxs-lookup"><span data-stu-id="1e20d-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="1e20d-118">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="1e20d-118">**HC_ACTION** 0</span></span> | <span data-ttu-id="1e20d-119">Le paramètre *lParam* est un pointeur vers une structure [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) contenant des informations sur un message supprimé de la file d’attente système.</span><span class="sxs-lookup"><span data-stu-id="1e20d-119">The *lParam* parameter is a pointer to an [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure containing information about a message removed from the system queue.</span></span> <span data-ttu-id="1e20d-120">La procédure de raccordement doit enregistrer le contenu de la structure en les copiant dans un fichier ou une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1e20d-120">The hook procedure must record the contents of the structure by copying them to a buffer or file.</span></span> |
| <span data-ttu-id="1e20d-121">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="1e20d-121">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="1e20d-122">Une boîte de dialogue modale du système a été détruite.</span><span class="sxs-lookup"><span data-stu-id="1e20d-122">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="1e20d-123">La procédure de raccordement doit reprendre l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e20d-123">The hook procedure must resume recording.</span></span> |
| <span data-ttu-id="1e20d-124">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="1e20d-124">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="1e20d-125">Une boîte de dialogue modale du système s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1e20d-125">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="1e20d-126">Jusqu’à ce que la boîte de dialogue soit détruite, la procédure de raccordement doit arrêter l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e20d-126">Until the dialog box is destroyed, the hook procedure must stop recording.</span></span> |

### <a name="wparam"></a><span data-ttu-id="1e20d-127">wParam</span><span class="sxs-lookup"><span data-stu-id="1e20d-127">wParam</span></span>

<span data-ttu-id="1e20d-128">Type : **wParam**</span><span class="sxs-lookup"><span data-stu-id="1e20d-128">Type: **WPARAM**</span></span>

<span data-ttu-id="1e20d-129">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="1e20d-129">This parameter is not used.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="1e20d-130">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="1e20d-130">lParam [in]</span></span>

<span data-ttu-id="1e20d-131">Type : **lParam**</span><span class="sxs-lookup"><span data-stu-id="1e20d-131">Type: **LPARAM**</span></span>

<span data-ttu-id="1e20d-132">Pointeur vers une structure **EVENTMSG** qui contient le message à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="1e20d-132">A pointer to an **EVENTMSG** structure that contains the message to be recorded.</span></span>

## <a name="returns"></a><span data-ttu-id="1e20d-133">Retours</span><span class="sxs-lookup"><span data-stu-id="1e20d-133">Returns</span></span>

<span data-ttu-id="1e20d-134">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="1e20d-134">Type: **LRESULT**</span></span>

<span data-ttu-id="1e20d-135">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1e20d-135">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e20d-136">Notes</span><span class="sxs-lookup"><span data-stu-id="1e20d-136">Remarks</span></span>

<span data-ttu-id="1e20d-137">Une procédure de hook **JournalRecordProc** doit copier mais ne pas modifier les messages.</span><span class="sxs-lookup"><span data-stu-id="1e20d-137">A **JournalRecordProc** hook procedure must copy but not modify the messages.</span></span>
<span data-ttu-id="1e20d-138">Une fois que la procédure de Hook a retourné le contrôle au système, le message continue à être traité.</span><span class="sxs-lookup"><span data-stu-id="1e20d-138">After the hook procedure returns control to the system, the message continues to be processed.</span></span>

<span data-ttu-id="1e20d-139">Installez la procédure de hook **JournalRecordProc** en spécifiant le type de [WH_JOURNALRECORD](about-hooks.md) et un pointeur vers la procédure de Hook dans un appel à la fonction **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="1e20d-139">Install the **JournalRecordProc** hook procedure by specifying the [WH_JOURNALRECORD](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="1e20d-140">Une procédure de hook **JournalRecordProc** n’a pas besoin de résider dans une bibliothèque de liens dynamiques.</span><span class="sxs-lookup"><span data-stu-id="1e20d-140">A **JournalRecordProc** hook procedure does not need to live in a dynamic-link library.</span></span>
<span data-ttu-id="1e20d-141">Une procédure de hook **JournalRecordProc** peut résider dans l’application elle-même.</span><span class="sxs-lookup"><span data-stu-id="1e20d-141">A **JournalRecordProc** hook procedure can live in the application itself.</span></span>

<span data-ttu-id="1e20d-142">Contrairement à la plupart des autres procédures de raccordement globales, les procédures de hook **JournalRecordProc** et [JournalPlaybackProc](journalplaybackproc.md) sont toujours appelées dans le contexte du thread qui définit le hook.</span><span class="sxs-lookup"><span data-stu-id="1e20d-142">Unlike most other global hook procedures, the **JournalRecordProc** and [JournalPlaybackProc](journalplaybackproc.md) hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="1e20d-143">Une application qui a installé une procédure de hook **JournalRecordProc** doit surveiller la [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) code de clé virtuelle (qui est implémenté en tant que combinaison de touches CTRL + ATTN sur la plupart des claviers).</span><span class="sxs-lookup"><span data-stu-id="1e20d-143">An application that has installed a **JournalRecordProc** hook procedure should watch for the [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) virtual key code (which is implemented as the CTRL+BREAK key combination on most keyboards).</span></span>
<span data-ttu-id="1e20d-144">Ce code de clé virtuelle doit être interprété par l’application comme un signal indiquant que l’utilisateur souhaite arrêter l’enregistrement du journal.</span><span class="sxs-lookup"><span data-stu-id="1e20d-144">This virtual key code should be interpreted by the application as a signal that the user wishes to stop journal recording.</span></span>
<span data-ttu-id="1e20d-145">L’application doit répondre en mettant fin à la séquence d’enregistrement et en supprimant la procédure de hook **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="1e20d-145">The application should respond by ending the recording sequence and removing the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="1e20d-146">La suppression est importante.</span><span class="sxs-lookup"><span data-stu-id="1e20d-146">Removal is important.</span></span>
<span data-ttu-id="1e20d-147">Il empêche une application de journalisation de verrouiller le système en raccrochant à l’intérieur d’une procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="1e20d-147">It prevents a journaling application from locking up the system by hanging inside a hook procedure.</span></span>

<span data-ttu-id="1e20d-148">Ce rôle en tant que signal d’arrêt de l’enregistrement journl signifie qu’une combinaison de touches CTRL + ATTN ne peut pas être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="1e20d-148">This role as a signal to stop journl recording means that a CTRL+BREAK key combination cannot itself be recorded.</span></span>
<span data-ttu-id="1e20d-149">Étant donné que la combinaison de touches CTRL + C n’a pas de rôle comme un signal de journalisation, elle peut être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="1e20d-149">Since the CTRL+C key combination has no such role as a journaling signal, it can be recorded.</span></span>
<span data-ttu-id="1e20d-150">Il existe deux autres combinaisons de touches qui ne peuvent pas être enregistrées : CTRL + ECHAP et CTRL + ALT + SUPPR.</span><span class="sxs-lookup"><span data-stu-id="1e20d-150">There are two other key combinations that cannot be recorded: CTRL+ESC and CTRL+ALT+DEL.</span></span>
<span data-ttu-id="1e20d-151">Ces deux combinaisons de touches entraînent l’arrêt de toutes les activités de journalisation (enregistrement ou lecture) par le système, la suppression de tous les hooks de journalisation et la publication d’un message de [WM_CANCELJOURNAL](wm-canceljournal.md) dans l’application de journalisation.</span><span class="sxs-lookup"><span data-stu-id="1e20d-151">Those two key combinations cause the system to stop all journaling activities (record or playback), remove all journaling hooks, and post a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e20d-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e20d-152">See also</span></span>

[<span data-ttu-id="1e20d-153">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="1e20d-153">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="1e20d-154">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="1e20d-154">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="1e20d-155">JournalPlaybackProc</span><span class="sxs-lookup"><span data-stu-id="1e20d-155">JournalPlaybackProc</span></span>](journalplaybackproc.md)

[<span data-ttu-id="1e20d-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="1e20d-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="1e20d-157">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="1e20d-157">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="1e20d-158">Hooks</span><span class="sxs-lookup"><span data-stu-id="1e20d-158">Hooks</span></span>](hooks.md)
