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
# <a name="writing-a-servicemain-function"></a>Écriture d’une fonction ServiceMain

La fonction SvcMain de l’exemple suivant est la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) pour l’exemple de service. SvcMain a accès aux arguments de ligne de commande du service de la même façon que la fonction **principale** d’une application console. Le premier paramètre contient le nombre d’arguments passés au service dans le deuxième paramètre. Il y aura toujours au moins un argument. Le deuxième paramètre est un pointeur vers un tableau de pointeurs de chaîne. Le premier élément du tableau est toujours le nom du service.

La fonction SvcMain appelle d’abord la fonction [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) pour inscrire la fonction SvcCtrlHandler comme fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) du service et commencer l’initialisation. **RegisterServiceCtrlHandler** doit être la première fonction qui ne fonctionne pas dans [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) , de sorte que le service peut utiliser le handle d’état retourné par cette fonction pour appeler [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) avec l’état d’arrêt du service \_ si une erreur se produit.

Ensuite, la fonction SvcMain appelle la fonction ReportSvcStatus pour indiquer que son état initial est \_ en attente de démarrage de service \_ . Si le service est dans cet État, aucun contrôle n’est accepté. Pour simplifier la logique du service, il est recommandé que le service n’accepte aucun contrôle pendant qu’il effectue son initialisation.

Enfin, la fonction SvcMain appelle la fonction SvcInit pour effectuer l’initialisation spécifique au service et commencer le travail à effectuer par le service.

L’exemple de fonction d’initialisation, SvcInit, est un exemple très simple ; Il n’effectue pas de tâches d’initialisation plus complexes, telles que la création de threads supplémentaires. Il crée un événement que le gestionnaire de contrôle des services peut signaler pour indiquer que le service doit s’arrêter, puis appelle ReportSvcStatus pour indiquer que le service est passé à l’état d’exécution du SERVICE \_ . À ce stade, le service a terminé son initialisation et est prêt à accepter les contrôles. Pour optimiser les performances du système, votre application doit passer à l’État en cours d’exécution dans les 25-100 millisecondes.

Étant donné que cet exemple de service n’effectue pas de tâches réelles, SvcInit attend simplement que l’événement d’arrêt de service soit signalé en appelant la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) , appelle ReportSvcStatus pour indiquer que le service est passé à l’état d’arrêt du service \_ et retourne. (Notez qu’il est important que la fonction retourne, plutôt que d’appeler la fonction [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) , car le retour permet de nettoyer la mémoire allouée pour les arguments.) Vous pouvez effectuer des tâches de nettoyage supplémentaires à l’aide de la fonction [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) au lieu de **WaitForSingleObject**. Le thread qui exécute la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) se termine, mais le service lui-même continue de s’exécuter. Quand le gestionnaire de contrôle des services signale l’événement, un thread du pool de threads exécute votre rappel pour effectuer le nettoyage supplémentaire, y compris la définition de l’État sur SERVICE \_ arrêté.

Notez que cet exemple utilise SvcReportEvent pour écrire des événements d’erreur dans le journal des événements. Pour obtenir le code source de SvcReportEvent, consultez [SVC. cpp](svc-cpp.md). Pour obtenir un exemple de fonction de gestionnaire de contrôles, consultez [écriture d’une fonction de gestionnaire de contrôle](writing-a-control-handler-function.md).

Les définitions globales suivantes sont utilisées dans cet exemple.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



L’exemple de fragment suivant est extrait de l’exemple de service complet.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonction de service ServiceMain](service-servicemain-function.md)
</dt> <dt>

[Exemple de service complet](the-complete-service-sample.md)
</dt> </dl>

 

 
