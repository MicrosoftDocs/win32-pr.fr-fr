---
description: Le débogueur utilise la fonction WaitForDebugEvent au début de sa boucle principale.
ms.assetid: 5a45854e-2711-49d5-982b-6b85248ec632
title: Écriture de la boucle principale du débogueur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f21c56364c314c676c5fd5dbb1cd6e9d1acd63e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950618"
---
# <a name="writing-the-debuggers-main-loop"></a><span data-ttu-id="92b25-103">Écriture de la boucle principale du débogueur</span><span class="sxs-lookup"><span data-stu-id="92b25-103">Writing the Debugger's Main Loop</span></span>

<span data-ttu-id="92b25-104">Le débogueur utilise la fonction [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) au début de sa boucle principale.</span><span class="sxs-lookup"><span data-stu-id="92b25-104">The debugger uses the [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) function at the beginning of its main loop.</span></span> <span data-ttu-id="92b25-105">Cette fonction bloque le débogueur jusqu’à ce qu’un événement de débogage se produise.</span><span class="sxs-lookup"><span data-stu-id="92b25-105">This function blocks the debugger until a debugging event occurs.</span></span> <span data-ttu-id="92b25-106">Lorsque l’événement de débogage se produit, le système interrompt tous les threads du processus en cours de débogage et notifie le débogueur de l’événement.</span><span class="sxs-lookup"><span data-stu-id="92b25-106">When the debugging event occurs, the system suspends all threads in the process being debugged and notifies the debugger of the event.</span></span>

<span data-ttu-id="92b25-107">Le débogueur peut interagir avec l’utilisateur ou manipuler l’état du processus en cours de débogage, à l’aide des fonctions [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext), [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry), [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory), [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)et [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) .</span><span class="sxs-lookup"><span data-stu-id="92b25-107">The debugger can interact with the user, or manipulate the state of the process being debugged, by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext), [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry), [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory), [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext), and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="92b25-108">**GetThreadSelectorEntry** retourne l’entrée de table du descripteur pour un sélecteur et un thread spécifiés.</span><span class="sxs-lookup"><span data-stu-id="92b25-108">**GetThreadSelectorEntry** returns the descriptor table entry for a specified selector and thread.</span></span> <span data-ttu-id="92b25-109">Les débogueurs utilisent l’entrée de la table du descripteur pour convertir une adresse relative à un segment en adresse virtuelle linéaire.</span><span class="sxs-lookup"><span data-stu-id="92b25-109">Debuggers use the descriptor table entry to convert a segment-relative address to a linear virtual address.</span></span> <span data-ttu-id="92b25-110">Les fonctions **ReadProcessMemory** et **WriteProcessMemory** requièrent des adresses virtuelles linéaires.</span><span class="sxs-lookup"><span data-stu-id="92b25-110">The **ReadProcessMemory** and **WriteProcessMemory** functions require linear virtual addresses.</span></span>

<span data-ttu-id="92b25-111">Les débogueurs lisent fréquemment la mémoire du processus en cours de débogage et écrivent la mémoire qui contient des instructions dans le cache d’instructions.</span><span class="sxs-lookup"><span data-stu-id="92b25-111">Debuggers frequently read the memory of the process being debugged and write the memory that contains instructions to the instruction cache.</span></span> <span data-ttu-id="92b25-112">Une fois les instructions écrites, le débogueur appelle la fonction [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache) pour exécuter les instructions mises en cache.</span><span class="sxs-lookup"><span data-stu-id="92b25-112">After the instructions are written, the debugger calls the [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache) function to execute the cached instructions.</span></span>

<span data-ttu-id="92b25-113">Le débogueur utilise la fonction [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) à la fin de sa boucle principale.</span><span class="sxs-lookup"><span data-stu-id="92b25-113">The debugger uses the [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) function at the end of its main loop.</span></span> <span data-ttu-id="92b25-114">Cette fonction permet au processus en cours de débogage de continuer à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="92b25-114">This function allows the process being debugged to continue executing.</span></span>

<span data-ttu-id="92b25-115">L’exemple suivant utilise les fonctions [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) et [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) pour illustrer comment un débogueur simple peut être organisé.</span><span class="sxs-lookup"><span data-stu-id="92b25-115">The following example uses the [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) and [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) functions to illustrate how a simple debugger might be organized.</span></span>


```C++
#include <windows.h>

DWORD OnCreateThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnCreateProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitThreadDebugEvent(const LPDEBUG_EVENT);
DWORD OnExitProcessDebugEvent(const LPDEBUG_EVENT);
DWORD OnLoadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnUnloadDllDebugEvent(const LPDEBUG_EVENT);
DWORD OnOutputDebugStringEvent(const LPDEBUG_EVENT);
DWORD OnRipEvent(const LPDEBUG_EVENT);

void EnterDebugLoop(const LPDEBUG_EVENT DebugEv)
{
   DWORD dwContinueStatus = DBG_CONTINUE; // exception continuation 
 
   for(;;) 
   { 
   // Wait for a debugging event to occur. The second parameter indicates
   // that the function does not return until a debugging event occurs. 
 
      WaitForDebugEvent(DebugEv, INFINITE); 

   // Process the debugging event code. 
 
      switch (DebugEv->dwDebugEventCode) 
      { 
         case EXCEPTION_DEBUG_EVENT: 
         // Process the exception code. When handling 
         // exceptions, remember to set the continuation 
         // status parameter (dwContinueStatus). This value 
         // is used by the ContinueDebugEvent function. 
 
            switch(DebugEv->u.Exception.ExceptionRecord.ExceptionCode)
            { 
               case EXCEPTION_ACCESS_VIOLATION: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_BREAKPOINT: 
               // First chance: Display the current 
               // instruction and register values. 
                  break;
 
               case EXCEPTION_DATATYPE_MISALIGNMENT: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               case EXCEPTION_SINGLE_STEP: 
               // First chance: Update the display of the 
               // current instruction and register values. 
                  break;
 
               case DBG_CONTROL_C: 
               // First chance: Pass this on to the system. 
               // Last chance: Display an appropriate error. 
                  break;
 
               default:
               // Handle other exceptions. 
                  break;
            } 

            break;
 
         case CREATE_THREAD_DEBUG_EVENT: 
         // As needed, examine or change the thread's registers 
         // with the GetThreadContext and SetThreadContext functions; 
         // and suspend and resume thread execution with the 
         // SuspendThread and ResumeThread functions. 

            dwContinueStatus = OnCreateThreadDebugEvent(DebugEv);
            break;

         case CREATE_PROCESS_DEBUG_EVENT: 
         // As needed, examine or change the registers of the
         // process's initial thread with the GetThreadContext and
         // SetThreadContext functions; read from and write to the
         // process's virtual memory with the ReadProcessMemory and
         // WriteProcessMemory functions; and suspend and resume
         // thread execution with the SuspendThread and ResumeThread
         // functions. Be sure to close the handle to the process image
         // file with CloseHandle.

            dwContinueStatus = OnCreateProcessDebugEvent(DebugEv);
            break;
 
         case EXIT_THREAD_DEBUG_EVENT: 
         // Display the thread's exit code. 

            dwContinueStatus = OnExitThreadDebugEvent(DebugEv);
            break;
 
         case EXIT_PROCESS_DEBUG_EVENT: 
         // Display the process's exit code. 

            dwContinueStatus = OnExitProcessDebugEvent(DebugEv);
            break;
 
         case LOAD_DLL_DEBUG_EVENT: 
         // Read the debugging information included in the newly 
         // loaded DLL. Be sure to close the handle to the loaded DLL 
         // with CloseHandle.

            dwContinueStatus = OnLoadDllDebugEvent(DebugEv);
            break;
 
         case UNLOAD_DLL_DEBUG_EVENT: 
         // Display a message that the DLL has been unloaded. 

            dwContinueStatus = OnUnloadDllDebugEvent(DebugEv);
            break;
 
         case OUTPUT_DEBUG_STRING_EVENT: 
         // Display the output debugging string. 

            dwContinueStatus = OnOutputDebugStringEvent(DebugEv);
            break;

         case RIP_EVENT:
            dwContinueStatus = OnRipEvent(DebugEv);
            break;
      } 
 
   // Resume executing the thread that reported the debugging event. 
 
   ContinueDebugEvent(DebugEv->dwProcessId, 
                      DebugEv->dwThreadId, 
                      dwContinueStatus);
   }
}
```



 

 
