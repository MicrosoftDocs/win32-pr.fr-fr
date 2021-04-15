---
description: Les exemples suivants illustrent l’utilisation des fonctions d’initialisation à usage unique.
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: Utilisation de One-Time initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f89cbe0e2d3e7c45d4f18863533c8c161037ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529769"
---
# <a name="using-one-time-initialization"></a><span data-ttu-id="74761-103">Utilisation de One-Time initialisation</span><span class="sxs-lookup"><span data-stu-id="74761-103">Using One-Time Initialization</span></span>

<span data-ttu-id="74761-104">Les exemples suivants illustrent l’utilisation des fonctions d’initialisation à usage unique.</span><span class="sxs-lookup"><span data-stu-id="74761-104">The following examples demonstrate the use of the one-time initialization functions.</span></span>

## <a name="synchronous-example"></a><span data-ttu-id="74761-105">Exemple synchrone</span><span class="sxs-lookup"><span data-stu-id="74761-105">Synchronous Example</span></span>

<span data-ttu-id="74761-106">Dans cet exemple, la `g_InitOnce` variable globale est la structure d’initialisation à usage unique.</span><span class="sxs-lookup"><span data-stu-id="74761-106">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="74761-107">Elle est initialisée statiquement à l’aide d' **init \_ une fois l’initialisation \_ statique \_** terminée.</span><span class="sxs-lookup"><span data-stu-id="74761-107">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="74761-108">La `OpenEventHandleSync` fonction retourne un handle à un événement créé une seule fois.</span><span class="sxs-lookup"><span data-stu-id="74761-108">The `OpenEventHandleSync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="74761-109">Il appelle la fonction [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) pour exécuter le code d’initialisation contenu dans la `InitHandleFunction` fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="74761-109">It calls the [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) function to execute the initialization code contained in the `InitHandleFunction` callback function.</span></span> <span data-ttu-id="74761-110">Si la fonction de rappel réussit, `OpenEventHandleSync` retourne le handle d’événement retourné dans *lpContext*; sinon, elle retourne une **\_ \_ valeur de handle non valide**.</span><span class="sxs-lookup"><span data-stu-id="74761-110">If the callback function succeeds, `OpenEventHandleSync` returns the event handle returned in *lpContext*; otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="74761-111">La `InitHandleFunction` fonction est la [fonction de rappel d’initialisation à usage unique](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span><span class="sxs-lookup"><span data-stu-id="74761-111">The `InitHandleFunction` function is the [one-time initialization callback function](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn).</span></span> <span data-ttu-id="74761-112">`InitHandleFunction` appelle la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour créer l’événement et retourne le handle d’événement dans le paramètre *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="74761-112">`InitHandleFunction` calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and returns the event handle in the *lpContext* parameter.</span></span>


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Initialization callback function 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        
    PVOID Parameter,            
    PVOID *lpContext);           

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleSync()
{
  PVOID lpContext;
  BOOL  bStatus;
  
  // Execute the initialization callback function 
  bStatus = InitOnceExecuteOnce(&g_InitOnce,          // One-time initialization structure
                                InitHandleFunction,   // Pointer to initialization callback function
                                NULL,                 // Optional parameter to callback function (not used)
                                &lpContext);          // Receives pointer to event object stored in g_InitOnce

  // InitOnceExecuteOnce function succeeded. Return event object.
  if (bStatus)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return (INVALID_HANDLE_VALUE);
  }
}

// Initialization callback function that creates the event object 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        // Pointer to one-time initialization structure        
    PVOID Parameter,            // Optional parameter passed by InitOnceExecuteOnce            
    PVOID *lpContext)           // Receives pointer to event object           
{
  HANDLE hEvent;

  // Create event object
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return FALSE;
  }
  // Event object creation succeeded.
  else
  {
    *lpContext = hEvent;
    return TRUE;
  }
}
```



## <a name="asynchronous-example"></a><span data-ttu-id="74761-113">Exemple asynchrone</span><span class="sxs-lookup"><span data-stu-id="74761-113">Asynchronous Example</span></span>

<span data-ttu-id="74761-114">Dans cet exemple, la `g_InitOnce` variable globale est la structure d’initialisation à usage unique.</span><span class="sxs-lookup"><span data-stu-id="74761-114">In this example, the `g_InitOnce` global variable is the one-time initialization structure.</span></span> <span data-ttu-id="74761-115">Elle est initialisée statiquement à l’aide d' **init \_ une fois l’initialisation \_ statique \_** terminée.</span><span class="sxs-lookup"><span data-stu-id="74761-115">It is initialized statically using **INIT\_ONCE\_STATIC\_INIT**.</span></span>

<span data-ttu-id="74761-116">La `OpenEventHandleAsync` fonction retourne un handle à un événement créé une seule fois.</span><span class="sxs-lookup"><span data-stu-id="74761-116">The `OpenEventHandleAsync` function returns a handle to an event that is created only once.</span></span> <span data-ttu-id="74761-117">`OpenEventHandleAsync` appelle la fonction [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) pour passer à l’état d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="74761-117">`OpenEventHandleAsync` calls the [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) function to enter the initializing state.</span></span>

<span data-ttu-id="74761-118">Si l’appel s’effectue correctement, le code vérifie la valeur du paramètre *fPending* pour déterminer s’il faut créer l’événement ou simplement retourner un handle à l’événement créé par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="74761-118">If the call succeeds, the code checks the value of the *fPending* parameter to determine whether to create the event or simply return a handle to the event created by another thread.</span></span> <span data-ttu-id="74761-119">Si *fPending* a la **valeur false**, l’initialisation est déjà terminée et `OpenEventHandleAsync` retourne alors le handle d’événement retourné dans le paramètre *lpContext* .</span><span class="sxs-lookup"><span data-stu-id="74761-119">If *fPending* is **FALSE**, initialization has already completed so `OpenEventHandleAsync` returns the event handle returned in the *lpContext* parameter.</span></span> <span data-ttu-id="74761-120">Dans le cas contraire, elle appelle la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) pour créer l’événement et la fonction [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) pour terminer l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="74761-120">Otherwise, it calls the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create the event and the [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) function to complete the initialization.</span></span>

<span data-ttu-id="74761-121">Si l’appel à [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) a échoué, `OpenEventHandleAsync` retourne le nouveau handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="74761-121">If the call to [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) succeeds, `OpenEventHandleAsync` returns the new event handle.</span></span> <span data-ttu-id="74761-122">Dans le cas contraire, il ferme le descripteur d’événement et appelle [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) avec **init \_ une fois la \_ vérification \_ uniquement** pour déterminer si l’initialisation a échoué ou a été effectuée par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="74761-122">Otherwise, it closes the event handle and calls [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) with **INIT\_ONCE\_CHECK\_ONLY** to determine whether initialization failed or was completed by another thread.</span></span>

<span data-ttu-id="74761-123">Si l’initialisation a été effectuée par un autre thread, `OpenEventHandleAsync` retourne le handle d’événement retourné dans *lpContext*.</span><span class="sxs-lookup"><span data-stu-id="74761-123">If the initialization was completed by another thread, `OpenEventHandleAsync` returns the event handle returned in *lpContext*.</span></span> <span data-ttu-id="74761-124">Sinon, elle retourne **une \_ \_ valeur de handle non valide**.</span><span class="sxs-lookup"><span data-stu-id="74761-124">Otherwise, it returns **INVALID\_HANDLE\_VALUE**.</span></span>


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleAsync()
{
  PVOID  lpContext;
  BOOL   fStatus;
  BOOL   fPending;
  HANDLE hEvent;
  
  // Begin one-time initialization
  fStatus = InitOnceBeginInitialize(&g_InitOnce,       // Pointer to one-time initialization structure
                                    INIT_ONCE_ASYNC,   // Asynchronous one-time initialization
                                    &fPending,         // Receives initialization status
                                    &lpContext);       // Receives pointer to data in g_InitOnce  

  // InitOnceBeginInitialize function failed.
  if (!fStatus)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Initialization has already completed and lpContext contains event object.
  if (!fPending)
  {
    return (HANDLE)lpContext;
  }

  // Create event object for one-time initialization.
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Complete one-time initialization.
  fStatus = InitOnceComplete(&g_InitOnce,             // Pointer to one-time initialization structure
                             INIT_ONCE_ASYNC,         // Asynchronous initialization
                             (PVOID)hEvent);          // Pointer to event object to be stored in g_InitOnce

  // InitOnceComplete function succeeded. Return event object.
  if (fStatus)
  {
    return hEvent;
  }
  
  // Initialization has already completed. Free the local event.
  CloseHandle(hEvent);


  // Retrieve the final context data.
  fStatus = InitOnceBeginInitialize(&g_InitOnce,            // Pointer to one-time initialization structure
                                    INIT_ONCE_CHECK_ONLY,   // Check whether initialization is complete
                                    &fPending,              // Receives initialization status
                                    &lpContext);            // Receives pointer to event object in g_InitOnce
  
  // Initialization is complete. Return handle.
  if (fStatus && !fPending)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return INVALID_HANDLE_VALUE;
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="74761-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74761-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74761-126">Initialisation unique</span><span class="sxs-lookup"><span data-stu-id="74761-126">One-Time Initialization</span></span>](one-time-initialization.md)
</dt> </dl>

 

 
