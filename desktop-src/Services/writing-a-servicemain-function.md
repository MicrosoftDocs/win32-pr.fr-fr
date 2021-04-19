---
description: La fonction SvcMain de l’exemple suivant est la fonction ServiceMain pour l’exemple de service.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Écriture d’une fonction ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3e947c356bad6c6d54395a671aa192c93de1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514810"
---
# <a name="writing-a-servicemain-function"></a><span data-ttu-id="22fe8-103">Écriture d’une fonction ServiceMain</span><span class="sxs-lookup"><span data-stu-id="22fe8-103">Writing a ServiceMain Function</span></span>

<span data-ttu-id="22fe8-104">La fonction SvcMain de l’exemple suivant est la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) pour l’exemple de service.</span><span class="sxs-lookup"><span data-stu-id="22fe8-104">The SvcMain function in the following example is the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function for the example service.</span></span> <span data-ttu-id="22fe8-105">SvcMain a accès aux arguments de ligne de commande du service de la même façon que la fonction **principale** d’une application console.</span><span class="sxs-lookup"><span data-stu-id="22fe8-105">SvcMain has access to the command-line arguments for the service in the way that the **main** function of a console application does.</span></span> <span data-ttu-id="22fe8-106">Le premier paramètre contient le nombre d’arguments passés au service dans le deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="22fe8-106">The first parameter contains the number of arguments being passed to the service in the second parameter.</span></span> <span data-ttu-id="22fe8-107">Il y aura toujours au moins un argument.</span><span class="sxs-lookup"><span data-stu-id="22fe8-107">There will always be at least one argument.</span></span> <span data-ttu-id="22fe8-108">Le deuxième paramètre est un pointeur vers un tableau de pointeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="22fe8-108">The second parameter is a pointer to an array of string pointers.</span></span> <span data-ttu-id="22fe8-109">Le premier élément du tableau est toujours le nom du service.</span><span class="sxs-lookup"><span data-stu-id="22fe8-109">The first item in the array is always the service name.</span></span>

<span data-ttu-id="22fe8-110">La fonction SvcMain appelle d’abord la fonction [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) pour inscrire la fonction SvcCtrlHandler comme fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) du service et commencer l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="22fe8-110">The SvcMain function first calls the [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) function to register the SvcCtrlHandler function as the service's [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function and begin initialization.</span></span> <span data-ttu-id="22fe8-111">**RegisterServiceCtrlHandler** doit être la première fonction qui ne fonctionne pas dans [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , de sorte que le service peut utiliser le handle d’état retourné par cette fonction pour appeler [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) avec l’état d’arrêt du service \_ si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="22fe8-111">**RegisterServiceCtrlHandler** should be the first nonfailing function in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) so the service can use the status handle returned by this function to call [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) with the SERVICE\_STOPPED state if an error occurs.</span></span>

<span data-ttu-id="22fe8-112">Ensuite, la fonction SvcMain appelle la fonction ReportSvcStatus pour indiquer que son état initial est \_ en attente de démarrage de service \_ .</span><span class="sxs-lookup"><span data-stu-id="22fe8-112">Next, the SvcMain function calls the ReportSvcStatus function to indicate that its initial status is SERVICE\_START\_PENDING.</span></span> <span data-ttu-id="22fe8-113">Si le service est dans cet État, aucun contrôle n’est accepté.</span><span class="sxs-lookup"><span data-stu-id="22fe8-113">While the service is in this state, no controls are accepted.</span></span> <span data-ttu-id="22fe8-114">Pour simplifier la logique du service, il est recommandé que le service n’accepte aucun contrôle pendant qu’il effectue son initialisation.</span><span class="sxs-lookup"><span data-stu-id="22fe8-114">To simplify the logic of the service, it is recommended that the service not accept any controls while it is performing its initialization.</span></span>

<span data-ttu-id="22fe8-115">Enfin, la fonction SvcMain appelle la fonction SvcInit pour effectuer l’initialisation spécifique au service et commencer le travail à effectuer par le service.</span><span class="sxs-lookup"><span data-stu-id="22fe8-115">Finally, the SvcMain function calls the SvcInit function to perform the service-specific initialization and begin the work to be performed by the service.</span></span>

<span data-ttu-id="22fe8-116">L’exemple de fonction d’initialisation, SvcInit, est un exemple très simple ; Il n’effectue pas de tâches d’initialisation plus complexes, telles que la création de threads supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="22fe8-116">The sample initialization function, SvcInit, is a very simple example; it does not perform more complex initialization tasks such as creating additional threads.</span></span> <span data-ttu-id="22fe8-117">Il crée un événement que le gestionnaire de contrôle des services peut signaler pour indiquer que le service doit s’arrêter, puis appelle ReportSvcStatus pour indiquer que le service est passé à l’état d’exécution du SERVICE \_ .</span><span class="sxs-lookup"><span data-stu-id="22fe8-117">It creates an event that the service control handler can signal to indicate that the service should stop, then calls ReportSvcStatus to indicate that the service has entered the SERVICE\_RUNNING state.</span></span> <span data-ttu-id="22fe8-118">À ce stade, le service a terminé son initialisation et est prêt à accepter les contrôles.</span><span class="sxs-lookup"><span data-stu-id="22fe8-118">At this point, the service has completed its initialization and is ready to accept controls.</span></span> <span data-ttu-id="22fe8-119">Pour optimiser les performances du système, votre application doit passer à l’État en cours d’exécution dans les 25-100 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="22fe8-119">For best system performance, your application should enter the running state within 25-100 milliseconds.</span></span>

<span data-ttu-id="22fe8-120">Étant donné que cet exemple de service n’effectue pas de tâches réelles, SvcInit attend simplement que l’événement d’arrêt de service soit signalé en appelant la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) , appelle ReportSvcStatus pour indiquer que le service est passé à l’état d’arrêt du service \_ et retourne.</span><span class="sxs-lookup"><span data-stu-id="22fe8-120">Because this sample service does not complete any real tasks, SvcInit simply waits for the service stop event to be signaled by calling the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function, calls ReportSvcStatus to indicate that the service has entered the SERVICE\_STOPPED state, and returns.</span></span> <span data-ttu-id="22fe8-121">(Notez qu’il est important que la fonction retourne, plutôt que d’appeler la fonction [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) , car le retour permet de nettoyer la mémoire allouée pour les arguments.) Vous pouvez effectuer des tâches de nettoyage supplémentaires à l’aide de la fonction [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) au lieu de **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="22fe8-121">(Note that it is important for the function to return, rather than call the [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) function, because returning allows for cleanup of the memory allocated for the arguments.) You can perform additional cleanup tasks by using the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) function instead of **WaitForSingleObject**.</span></span> <span data-ttu-id="22fe8-122">Le thread qui exécute la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) se termine, mais le service lui-même continue de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="22fe8-122">The thread that is running the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function terminates, but the service itself continues to run.</span></span> <span data-ttu-id="22fe8-123">Quand le gestionnaire de contrôle des services signale l’événement, un thread du pool de threads exécute votre rappel pour effectuer le nettoyage supplémentaire, y compris la définition de l’État sur SERVICE \_ arrêté.</span><span class="sxs-lookup"><span data-stu-id="22fe8-123">When the service control handler signals the event, a thread from the thread pool executes your callback to perform the additional cleanup, including setting the status to SERVICE\_STOPPED.</span></span>

<span data-ttu-id="22fe8-124">Notez que cet exemple utilise SvcReportEvent pour écrire des événements d’erreur dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="22fe8-124">Note that this example uses SvcReportEvent to write error events to the event log.</span></span> <span data-ttu-id="22fe8-125">Pour obtenir le code source de SvcReportEvent, consultez [SVC. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="22fe8-125">For the source code for SvcReportEvent, see [Svc.cpp](svc-cpp.md).</span></span> <span data-ttu-id="22fe8-126">Pour obtenir un exemple de fonction de gestionnaire de contrôles, consultez [écriture d’une fonction de gestionnaire de contrôle](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="22fe8-126">For an example control handler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span>

<span data-ttu-id="22fe8-127">Les définitions globales suivantes sont utilisées dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="22fe8-127">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="22fe8-128">L’exemple de fragment suivant est extrait de l’exemple de service complet.</span><span class="sxs-lookup"><span data-stu-id="22fe8-128">The following sample fragment is taken from the complete service sample.</span></span>


```C++
//
// Purpose: 
//   Entry point for the service
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None.
//
VOID WINAPI SvcMain( DWORD dwArgc, LPTSTR *lpszArgv )
{
    // Register the handler function for the service

    gSvcStatusHandle = RegisterServiceCtrlHandler( 
        SVCNAME, 
        SvcCtrlHandler);

    if( !gSvcStatusHandle )
    { 
        SvcReportEvent(TEXT("RegisterServiceCtrlHandler")); 
        return; 
    } 

    // These SERVICE_STATUS members remain as set here

    gSvcStatus.dwServiceType = SERVICE_WIN32_OWN_PROCESS; 
    gSvcStatus.dwServiceSpecificExitCode = 0;    

    // Report initial status to the SCM

    ReportSvcStatus( SERVICE_START_PENDING, NO_ERROR, 3000 );

    // Perform service-specific initialization and work.

    SvcInit( dwArgc, lpszArgv );
}

//
// Purpose: 
//   The service code
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None
//
VOID SvcInit( DWORD dwArgc, LPTSTR *lpszArgv)
{
    // TO_DO: Declare and set any required variables.
    //   Be sure to periodically call ReportSvcStatus() with 
    //   SERVICE_START_PENDING. If initialization fails, call
    //   ReportSvcStatus with SERVICE_STOPPED.

    // Create an event. The control handler function, SvcCtrlHandler,
    // signals this event when it receives the stop control code.

    ghSvcStopEvent = CreateEvent(
                         NULL,    // default security attributes
                         TRUE,    // manual reset event
                         FALSE,   // not signaled
                         NULL);   // no name

    if ( ghSvcStopEvent == NULL)
    {
        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }

    // Report running status when initialization is complete.

    ReportSvcStatus( SERVICE_RUNNING, NO_ERROR, 0 );

    // TO_DO: Perform work until service stops.

    while(1)
    {
        // Check whether to stop the service.

        WaitForSingleObject(ghSvcStopEvent, INFINITE);

        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }
}

//
// Purpose: 
//   Sets the current service status and reports it to the SCM.
//
// Parameters:
//   dwCurrentState - The current state (see SERVICE_STATUS)
//   dwWin32ExitCode - The system error code
//   dwWaitHint - Estimated time for pending operation, 
//     in milliseconds
// 
// Return value:
//   None
//
VOID ReportSvcStatus( DWORD dwCurrentState,
                      DWORD dwWin32ExitCode,
                      DWORD dwWaitHint)
{
    static DWORD dwCheckPoint = 1;

    // Fill in the SERVICE_STATUS structure.

    gSvcStatus.dwCurrentState = dwCurrentState;
    gSvcStatus.dwWin32ExitCode = dwWin32ExitCode;
    gSvcStatus.dwWaitHint = dwWaitHint;

    if (dwCurrentState == SERVICE_START_PENDING)
        gSvcStatus.dwControlsAccepted = 0;
    else gSvcStatus.dwControlsAccepted = SERVICE_ACCEPT_STOP;

    if ( (dwCurrentState == SERVICE_RUNNING) ||
           (dwCurrentState == SERVICE_STOPPED) )
        gSvcStatus.dwCheckPoint = 0;
    else gSvcStatus.dwCheckPoint = dwCheckPoint++;

    // Report the status of the service to the SCM.
    SetServiceStatus( gSvcStatusHandle, &gSvcStatus );
}

```



## <a name="related-topics"></a><span data-ttu-id="22fe8-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22fe8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22fe8-130">Fonction de service ServiceMain</span><span class="sxs-lookup"><span data-stu-id="22fe8-130">Service ServiceMain Function</span></span>](service-servicemain-function.md)
</dt> <dt>

[<span data-ttu-id="22fe8-131">Exemple de service complet</span><span class="sxs-lookup"><span data-stu-id="22fe8-131">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
