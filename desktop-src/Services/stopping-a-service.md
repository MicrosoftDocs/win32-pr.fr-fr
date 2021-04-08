---
description: Un programme de contrôle de service peut arrêter un service à l’aide de la fonction ControlService pour envoyer une demande d’arrêt de contrôle de SERVICE \_ \_ .
ms.assetid: fe16d2a8-3e66-49cc-b9c7-fffbc206e8d3
title: Arrêt d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb9625dd674623823341c1465964095de7efaf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868174"
---
# <a name="stopping-a-service"></a><span data-ttu-id="4cbf5-103">Arrêt d’un service</span><span class="sxs-lookup"><span data-stu-id="4cbf5-103">Stopping a Service</span></span>

<span data-ttu-id="4cbf5-104">Un [programme de contrôle de service](service-control-programs.md) peut arrêter un service à l’aide de la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour envoyer une demande d’arrêt de contrôle de service \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4cbf5-104">A [service control program](service-control-programs.md) can stop a service by using the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to send a SERVICE\_CONTROL\_STOP request.</span></span> <span data-ttu-id="4cbf5-105">Si le [Gestionnaire de contrôle des services](service-control-manager.md) (SCM) reçoit \_ une \_ demande d’arrêt de contrôle de service pour un service, il demande au service de s’arrêter en le transférant à la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) du service.</span><span class="sxs-lookup"><span data-stu-id="4cbf5-105">If the [service control manager](service-control-manager.md) (SCM) receives a SERVICE\_CONTROL\_STOP request for a service, it instructs the service to stop by forwarding the request to the service's [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function.</span></span> <span data-ttu-id="4cbf5-106">Toutefois, si le SCM détermine que d’autres services en cours d’exécution dépendent du service spécifié, il ne transfère pas la demande d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4cbf5-106">However, if the SCM determines that other running services are dependent on the specified service, it will not forward the stop request.</span></span> <span data-ttu-id="4cbf5-107">Au lieu de cela, elle retourne les \_ services dépendants des erreurs \_ \_ qui exécutent.</span><span class="sxs-lookup"><span data-stu-id="4cbf5-107">Instead, it returns ERROR\_DEPENDENT\_SERVICES\_RUNNING.</span></span> <span data-ttu-id="4cbf5-108">Par conséquent, pour arrêter un tel service par programmation, vous devez d’abord énumérer et arrêter ses services dépendants.</span><span class="sxs-lookup"><span data-stu-id="4cbf5-108">Therefore, to programmatically stop such a service, you must first enumerate and stop its dependent services.</span></span>

<span data-ttu-id="4cbf5-109">La fonction DoStopSvc de l’exemple suivant montre comment arrêter un service et tous les services dépendants.</span><span class="sxs-lookup"><span data-stu-id="4cbf5-109">The DoStopSvc function in the following example shows how to stop a service and any dependent services.</span></span> <span data-ttu-id="4cbf5-110">La variable szSvcName est une variable globale qui contient le nom du service à arrêter.</span><span class="sxs-lookup"><span data-stu-id="4cbf5-110">The szSvcName variable is a global variable that contains the name of the service to be stopped.</span></span> <span data-ttu-id="4cbf5-111">Pour obtenir l’exemple complet qui définit cette variable, consultez [SvcControl. cpp](svccontrol-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="4cbf5-111">For the complete example that sets this variable, see [SvcControl.cpp](svccontrol-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Stops the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoStopSvc()
{
    SERVICE_STATUS_PROCESS ssp;
    DWORD dwStartTime = GetTickCount();
    DWORD dwBytesNeeded;
    DWORD dwTimeout = 30000; // 30-second time-out
    DWORD dwWaitTime;

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,         // SCM database 
        szSvcName,            // name of service 
        SERVICE_STOP | 
        SERVICE_QUERY_STATUS | 
        SERVICE_ENUMERATE_DEPENDENTS);  
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Make sure the service is not already stopped.

    if ( !QueryServiceStatusEx( 
            schService, 
            SC_STATUS_PROCESS_INFO,
            (LPBYTE)&ssp, 
            sizeof(SERVICE_STATUS_PROCESS),
            &dwBytesNeeded ) )
    {
        printf("QueryServiceStatusEx failed (%d)\n", GetLastError()); 
        goto stop_cleanup;
    }

    if ( ssp.dwCurrentState == SERVICE_STOPPED )
    {
        printf("Service is already stopped.\n");
        goto stop_cleanup;
    }

    // If a stop is pending, wait for it.

    while ( ssp.dwCurrentState == SERVICE_STOP_PENDING ) 
    {
        printf("Service stop pending...\n");

        // Do not wait longer than the wait hint. A good interval is 
        // one-tenth of the wait hint but not less than 1 second  
        // and not more than 10 seconds. 
 
        dwWaitTime = ssp.dwWaitHint / 10;

        if( dwWaitTime < 1000 )
            dwWaitTime = 1000;
        else if ( dwWaitTime > 10000 )
            dwWaitTime = 10000;

        Sleep( dwWaitTime );

        if ( !QueryServiceStatusEx( 
                 schService, 
                 SC_STATUS_PROCESS_INFO,
                 (LPBYTE)&ssp, 
                 sizeof(SERVICE_STATUS_PROCESS),
                 &dwBytesNeeded ) )
        {
            printf("QueryServiceStatusEx failed (%d)\n", GetLastError()); 
            goto stop_cleanup;
        }

        if ( ssp.dwCurrentState == SERVICE_STOPPED )
        {
            printf("Service stopped successfully.\n");
            goto stop_cleanup;
        }

        if ( GetTickCount() - dwStartTime > dwTimeout )
        {
            printf("Service stop timed out.\n");
            goto stop_cleanup;
        }
    }

    // If the service is running, dependencies must be stopped first.

    StopDependentServices();

    // Send a stop code to the service.

    if ( !ControlService( 
            schService, 
            SERVICE_CONTROL_STOP, 
            (LPSERVICE_STATUS) &ssp ) )
    {
        printf( "ControlService failed (%d)\n", GetLastError() );
        goto stop_cleanup;
    }

    // Wait for the service to stop.

    while ( ssp.dwCurrentState != SERVICE_STOPPED ) 
    {
        Sleep( ssp.dwWaitHint );
        if ( !QueryServiceStatusEx( 
                schService, 
                SC_STATUS_PROCESS_INFO,
                (LPBYTE)&ssp, 
                sizeof(SERVICE_STATUS_PROCESS),
                &dwBytesNeeded ) )
        {
            printf( "QueryServiceStatusEx failed (%d)\n", GetLastError() );
            goto stop_cleanup;
        }

        if ( ssp.dwCurrentState == SERVICE_STOPPED )
            break;

        if ( GetTickCount() - dwStartTime > dwTimeout )
        {
            printf( "Wait timed out\n" );
            goto stop_cleanup;
        }
    }
    printf("Service stopped successfully\n");

stop_cleanup:
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

BOOL __stdcall StopDependentServices()
{
    DWORD i;
    DWORD dwBytesNeeded;
    DWORD dwCount;

    LPENUM_SERVICE_STATUS   lpDependencies = NULL;
    ENUM_SERVICE_STATUS     ess;
    SC_HANDLE               hDepService;
    SERVICE_STATUS_PROCESS  ssp;

    DWORD dwStartTime = GetTickCount();
    DWORD dwTimeout = 30000; // 30-second time-out

    // Pass a zero-length buffer to get the required buffer size.
    if ( EnumDependentServices( schService, SERVICE_ACTIVE, 
         lpDependencies, 0, &dwBytesNeeded, &dwCount ) ) 
    {
         // If the Enum call succeeds, then there are no dependent
         // services, so do nothing.
         return TRUE;
    } 
    else 
    {
        if ( GetLastError() != ERROR_MORE_DATA )
            return FALSE; // Unexpected error

        // Allocate a buffer for the dependencies.
        lpDependencies = (LPENUM_SERVICE_STATUS) HeapAlloc( 
            GetProcessHeap(), HEAP_ZERO_MEMORY, dwBytesNeeded );
  
        if ( !lpDependencies )
            return FALSE;

        __try {
            // Enumerate the dependencies.
            if ( !EnumDependentServices( schService, SERVICE_ACTIVE, 
                lpDependencies, dwBytesNeeded, &dwBytesNeeded,
                &dwCount ) )
            return FALSE;

            for ( i = 0; i < dwCount; i++ ) 
            {
                ess = *(lpDependencies + i);
                // Open the service.
                hDepService = OpenService( schSCManager, 
                   ess.lpServiceName, 
                   SERVICE_STOP | SERVICE_QUERY_STATUS );

                if ( !hDepService )
                   return FALSE;

                __try {
                    // Send a stop code.
                    if ( !ControlService( hDepService, 
                            SERVICE_CONTROL_STOP,
                            (LPSERVICE_STATUS) &ssp ) )
                    return FALSE;

                    // Wait for the service to stop.
                    while ( ssp.dwCurrentState != SERVICE_STOPPED ) 
                    {
                        Sleep( ssp.dwWaitHint );
                        if ( !QueryServiceStatusEx( 
                                hDepService, 
                                SC_STATUS_PROCESS_INFO,
                                (LPBYTE)&ssp, 
                                sizeof(SERVICE_STATUS_PROCESS),
                                &dwBytesNeeded ) )
                        return FALSE;

                        if ( ssp.dwCurrentState == SERVICE_STOPPED )
                            break;

                        if ( GetTickCount() - dwStartTime > dwTimeout )
                            return FALSE;
                    }
                } 
                __finally 
                {
                    // Always release the service handle.
                    CloseServiceHandle( hDepService );
                }
            }
        } 
        __finally 
        {
            // Always free the enumeration buffer.
            HeapFree( GetProcessHeap(), 0, lpDependencies );
        }
    } 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="4cbf5-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4cbf5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cbf5-113">Exemple de service complet</span><span class="sxs-lookup"><span data-stu-id="4cbf5-113">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
