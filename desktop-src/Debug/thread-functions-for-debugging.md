---
description: Apprenez à utiliser la fonction CreateThread pour créer un nouveau thread pour un processus. Les débogueurs doivent généralement examiner ou modifier le contenu des registres d’un thread.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Fonctions de thread pour le débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403982"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="8a604-104">Fonctions de thread pour le débogage</span><span class="sxs-lookup"><span data-stu-id="8a604-104">Thread Functions for Debugging</span></span>

<span data-ttu-id="8a604-105">La fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crée un nouveau thread pour un processus.</span><span class="sxs-lookup"><span data-stu-id="8a604-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="8a604-106">Les débogueurs doivent généralement examiner ou modifier le contenu des registres d’un thread.</span><span class="sxs-lookup"><span data-stu-id="8a604-106">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="8a604-107">Pour ce faire, un débogueur doit obtenir un handle pour le thread à l’aide de la fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) et en spécifiant l’accès approprié au thread (contexte d’obtention de thread \_ \_ , contexte de groupe de threads \_ \_ , ou les deux).</span><span class="sxs-lookup"><span data-stu-id="8a604-107">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="8a604-108">La fonction [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) permet à un débogueur d’obtenir l’identificateur d’un thread existant.</span><span class="sxs-lookup"><span data-stu-id="8a604-108">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="8a604-109">Un processus avec un accès approprié à un thread peut examiner les registres du thread à l’aide de la fonction [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) et définir le contenu des registres du thread à l’aide de la fonction [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .</span><span class="sxs-lookup"><span data-stu-id="8a604-109">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="8a604-110">Un processus peut également obtenir \_ \_ l’accès de reprise d’interruption de thread à un thread.</span><span class="sxs-lookup"><span data-stu-id="8a604-110">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="8a604-111">Ce type d’accès permet à un débogueur de contrôler l’exécution d’un thread à l’aide des fonctions [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) et [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="8a604-111">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="8a604-112">Pour plus d’informations sur les threads, consultez [processus et threads](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="8a604-112">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
