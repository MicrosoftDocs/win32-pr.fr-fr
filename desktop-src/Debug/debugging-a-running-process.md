---
description: Pour déboguer un processus qui est déjà en cours d’exécution, le débogueur doit utiliser DebugActiveProcess avec l’identificateur de processus. Pour récupérer une liste d’identificateurs de processus, utilisez la fonction EnumProcesses ou Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Débogage d’un processus en cours d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109991"
---
# <a name="debugging-a-running-process"></a><span data-ttu-id="9d5a9-104">Débogage d’un processus en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="9d5a9-104">Debugging a Running Process</span></span>

<span data-ttu-id="9d5a9-105">Pour déboguer un processus qui est déjà en cours d’exécution, le débogueur doit utiliser [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) avec l’identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="9d5a9-105">To debug a process that is already running, the debugger should use [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) with the process identifier.</span></span> <span data-ttu-id="9d5a9-106">Pour récupérer une liste d’identificateurs de processus, utilisez la fonction [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) ou [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="9d5a9-106">To retrieve a list of process identifiers, use either the [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) or [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function.</span></span>

<span data-ttu-id="9d5a9-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attache le débogueur au processus actif.</span><span class="sxs-lookup"><span data-stu-id="9d5a9-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attaches the debugger to the active process.</span></span> <span data-ttu-id="9d5a9-108">Dans ce cas, seul le processus actif peut être débogué ; ses processus enfants ne peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="9d5a9-108">In this case, only the active process can be debugged; its child processes cannot.</span></span> <span data-ttu-id="9d5a9-109">Le débogueur doit avoir un accès approprié au processus en cours d’exécution pour utiliser **DebugActiveProcess**.</span><span class="sxs-lookup"><span data-stu-id="9d5a9-109">The debugger must have appropriate access to the executing process to use **DebugActiveProcess**.</span></span> <span data-ttu-id="9d5a9-110">Pour plus d’informations sur les droits d’accès, consultez [Access Control](../secauthz/access-control.md).</span><span class="sxs-lookup"><span data-stu-id="9d5a9-110">For more information about access rights, see [Access Control](../secauthz/access-control.md).</span></span>

<span data-ttu-id="9d5a9-111">Une fois que le débogueur a créé ou attaché lui-même au processus qu’il envisage de déboguer, le système notifie le débogueur de tous les événements de débogage qui se produisent dans le processus et, s’il est spécifié, dans tous les processus enfants.</span><span class="sxs-lookup"><span data-stu-id="9d5a9-111">After the debugger has either created or attached itself to the process it intends to debug, the system notifies the debugger of all debugging events that occur in the process, and, if specified, in any child processes.</span></span> <span data-ttu-id="9d5a9-112">Pour plus d’informations sur les événements de débogage, consultez [débogage d’événements](debugging-events.md).</span><span class="sxs-lookup"><span data-stu-id="9d5a9-112">For more information about debugging events, see [Debugging Events](debugging-events.md).</span></span>

<span data-ttu-id="9d5a9-113">Pour détacher du processus en cours de débogage, le débogueur doit utiliser la fonction [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .</span><span class="sxs-lookup"><span data-stu-id="9d5a9-113">To detach from the process being debugged, the debugger should use the [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) function.</span></span>

 

 
