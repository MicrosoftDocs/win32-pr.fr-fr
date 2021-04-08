---
title: Inscription d’une fonction de raccordement
description: Les applications clientes reçoivent WinEvents dans une fonction de rappel WinEventProc. Les actions effectuées par la fonction de rappel sont définies par l’application, mais la syntaxe doit être telle qu’elle est spécifiée dans le prototype.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839662"
---
# <a name="registering-a-hook-function"></a><span data-ttu-id="fd5b8-104">Inscription d’une fonction de raccordement</span><span class="sxs-lookup"><span data-stu-id="fd5b8-104">Registering a Hook Function</span></span>

<span data-ttu-id="fd5b8-105">Les applications clientes reçoivent WinEvents dans une fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) .</span><span class="sxs-lookup"><span data-stu-id="fd5b8-105">Client applications receive WinEvents in a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function.</span></span> <span data-ttu-id="fd5b8-106">Les actions effectuées par la fonction de rappel sont définies par l’application, mais la syntaxe doit être telle qu’elle est spécifiée dans le prototype.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-106">The actions performed by the callback function are defined by the application, but the syntax must be as specified in the prototype.</span></span>

<span data-ttu-id="fd5b8-107">Avant de pouvoir recevoir des événements, la fonction doit être inscrite en appelant [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span><span class="sxs-lookup"><span data-stu-id="fd5b8-107">Before it can receive events, the function must be registered by calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="fd5b8-108">Le client peut appeler **SetWinEventHook** plusieurs fois pour inscrire différentes fonctions de raccordement, ou pour définir des événements supplémentaires pour une fonction de raccordement précédemment enregistrée.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-108">The client can call **SetWinEventHook** more than once to register different hook functions, or to set additional events for a previously registered hook function.</span></span>

<span data-ttu-id="fd5b8-109">Lors de l’appel de [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , le client spécifie les événements à recevoir et comment les recevoir.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-109">When calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) the client specifies which events to receive and how to receive them.</span></span> <span data-ttu-id="fd5b8-110">Le client peut choisir d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd5b8-110">The client can choose to:</span></span>

-   <span data-ttu-id="fd5b8-111">Recevoir tous les événements ou un ensemble spécifique d’événements.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-111">Receive all events or a specific set of events.</span></span>
-   <span data-ttu-id="fd5b8-112">Recevoir des événements de tous les threads ou d’un thread spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-112">Receive events from all threads or from a specific thread.</span></span>
-   <span data-ttu-id="fd5b8-113">Recevoir des événements de tous les processus ou d’un processus spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-113">Receive events from all processes or from a specific process.</span></span>
-   <span data-ttu-id="fd5b8-114">Gérer les événements en cours de traitement ou hors processus.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-114">Handle events in process or out of process.</span></span>

<span data-ttu-id="fd5b8-115">Lors de la génération d’un événement qui correspond aux critères spécifiés, le système appelle la fonction de rappel [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) du client (ou « procédure de Hook »).</span><span class="sxs-lookup"><span data-stu-id="fd5b8-115">When an event is generated that matches the specified criteria, the system calls the client's [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function (or "hook procedure").</span></span> <span data-ttu-id="fd5b8-116">Les paramètres que la fonction de raccordement reçoit indiquent au client la fenêtre, l’objet et l’élément enfant possible qui a généré l’événement.</span><span class="sxs-lookup"><span data-stu-id="fd5b8-116">The parameters that the hook function receives tell the client about the window, object, and possible child element that generated the event.</span></span> <span data-ttu-id="fd5b8-117">Un client utilise ces paramètres dans un appel de récupération d’objet, tel que [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="fd5b8-117">A client uses these parameters in an object retrieval call, such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

 




