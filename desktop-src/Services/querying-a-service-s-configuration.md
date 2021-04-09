---
description: Un programme de configuration de service utilise la fonction OpenService pour obtenir un handle avec l' \_ \_ accès de configuration de requête de service à un objet de service installé.
ms.assetid: e6633dc9-c9b6-457d-8adc-e751ec9cf71d
title: Interrogation d’une configuration de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efddea6ca590aa07b0c523588295d5f87ffefa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868397"
---
# <a name="querying-a-services-configuration"></a>Interrogation de la configuration d’un service

Un [programme de configuration de service](service-configuration-programs.md) utilise la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) pour obtenir un handle avec l' \_ accès de \_ configuration de requête de service à un objet de service installé. Le programme peut ensuite utiliser le descripteur d’objet de service dans les fonctions [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) et [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) pour récupérer la configuration actuelle du service.

Dans l’exemple suivant, la fonction DoQuerySvc utilise [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) et [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) pour récupérer les informations de configuration, puis écrit les informations sélectionnées dans la console. La variable szSvcName est une variable globale qui contient le nom du service. Pour obtenir l’exemple complet qui définit cette variable, consultez [SvcConfig. cpp](svcconfig-cpp.md).


```C++
//
// Purpose: 
//   Retrieves and displays the current service configuration.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoQuerySvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    LPQUERY_SERVICE_CONFIG lpsc; 
    LPSERVICE_DESCRIPTION lpsd;
    DWORD dwBytesNeeded, cbBufSize, dwError; 

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
        schSCManager,          // SCM database 
        szSvcName,             // name of service 
        SERVICE_QUERY_CONFIG); // need query config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Get the configuration information.
 
    if( !QueryServiceConfig( 
        schService, 
        NULL, 
        0, 
        &dwBytesNeeded))
    {
        dwError = GetLastError();
        if( ERROR_INSUFFICIENT_BUFFER == dwError )
        {
            cbBufSize = dwBytesNeeded;
            lpsc = (LPQUERY_SERVICE_CONFIG) LocalAlloc(LMEM_FIXED, cbBufSize);
        }
        else
        {
            printf("QueryServiceConfig failed (%d)", dwError);
            goto cleanup; 
        }
    }
  
    if( !QueryServiceConfig( 
        schService, 
        lpsc, 
        cbBufSize, 
        &dwBytesNeeded) ) 
    {
        printf("QueryServiceConfig failed (%d)", GetLastError());
        goto cleanup;
    }

    if( !QueryServiceConfig2( 
        schService, 
        SERVICE_CONFIG_DESCRIPTION,
        NULL, 
        0, 
        &dwBytesNeeded))
    {
        dwError = GetLastError();
        if( ERROR_INSUFFICIENT_BUFFER == dwError )
        {
            cbBufSize = dwBytesNeeded;
            lpsd = (LPSERVICE_DESCRIPTION) LocalAlloc(LMEM_FIXED, cbBufSize);
        }
        else
        {
            printf("QueryServiceConfig2 failed (%d)", dwError);
            goto cleanup; 
        }
    }
 
    if (! QueryServiceConfig2( 
        schService, 
        SERVICE_CONFIG_DESCRIPTION,
        (LPBYTE) lpsd, 
        cbBufSize, 
        &dwBytesNeeded) ) 
    {
        printf("QueryServiceConfig2 failed (%d)", GetLastError());
        goto cleanup;
    }
 
    // Print the configuration information.
 
    _tprintf(TEXT("%s configuration: \n"), szSvcName);
    _tprintf(TEXT("  Type: 0x%x\n"), lpsc->dwServiceType);
    _tprintf(TEXT("  Start Type: 0x%x\n"), lpsc->dwStartType);
    _tprintf(TEXT("  Error Control: 0x%x\n"), lpsc->dwErrorControl);
    _tprintf(TEXT("  Binary path: %s\n"), lpsc->lpBinaryPathName);
    _tprintf(TEXT("  Account: %s\n"), lpsc->lpServiceStartName);

    if (lpsd->lpDescription != NULL && lstrcmp(lpsd->lpDescription, TEXT("")) != 0)
        _tprintf(TEXT("  Description: %s\n"), lpsd->lpDescription);
    if (lpsc->lpLoadOrderGroup != NULL && lstrcmp(lpsc->lpLoadOrderGroup, TEXT("")) != 0)
        _tprintf(TEXT("  Load order group: %s\n"), lpsc->lpLoadOrderGroup);
    if (lpsc->dwTagId != 0)
        _tprintf(TEXT("  Tag ID: %d\n"), lpsc->dwTagId);
    if (lpsc->lpDependencies != NULL && lstrcmp(lpsc->lpDependencies, TEXT("")) != 0)
        _tprintf(TEXT("  Dependencies: %s\n"), lpsc->lpDependencies);
 
    LocalFree(lpsc); 
    LocalFree(lpsd);

cleanup:
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de service](service-configuration.md)
</dt> <dt>

[Exemple de service complet](the-complete-service-sample.md)
</dt> </dl>

 

 



