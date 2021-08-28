---
description: Un programme de configuration de service utilise la fonction CreateService pour installer un service dans la base de données SCM.
ms.assetid: b94bf94e-1b07-4686-be5c-306e7cf13f39
title: Installation d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 955875511688f9c3f2437d60fd615617e964c8f2f60333a7410143c7d451494b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968017"
---
# <a name="installing-a-service"></a>Installation d’un service

Un [programme de configuration de service](service-configuration-programs.md) utilise la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) pour installer un service dans la base de données SCM.

La fonction SvcInstall de l’exemple suivant montre comment installer un service à partir du programme de service lui-même. Pour obtenir un exemple complet, consultez [SVC. cpp](svc-cpp.md).


```C++
//
// Purpose: 
//   Installs a service in the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID SvcInstall()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    TCHAR szPath[MAX_PATH];

    if( !GetModuleFileName( "", szPath, MAX_PATH ) )
    {
        printf("Cannot install service (%d)\n", GetLastError());
        return;
    }

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

    // Create the service

    schService = CreateService( 
        schSCManager,              // SCM database 
        SVCNAME,                   // name of service 
        SVCNAME,                   // service name to display 
        SERVICE_ALL_ACCESS,        // desired access 
        SERVICE_WIN32_OWN_PROCESS, // service type 
        SERVICE_DEMAND_START,      // start type 
        SERVICE_ERROR_NORMAL,      // error control type 
        szPath,                    // path to service's binary 
        NULL,                      // no load ordering group 
        NULL,                      // no tag identifier 
        NULL,                      // no dependencies 
        NULL,                      // LocalSystem account 
        NULL);                     // no password 
 
    if (schService == NULL) 
    {
        printf("CreateService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }
    else printf("Service installed successfully\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Installation, suppression et énumération des services](service-installation-removal-and-enumeration.md)
</dt> <dt>

[Exemple de service complet](the-complete-service-sample.md)
</dt> </dl>

 

 



