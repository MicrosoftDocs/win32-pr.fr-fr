---
description: Un programme de configuration de service utilise la fonction OpenService pour obtenir un handle vers un objet de service installé. Le programme peut ensuite utiliser le descripteur d’objet de service dans la fonction DeleteService pour supprimer le service de la base de données SCM.
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: Suppression d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b1e0e95e0ea943487a0d3fa513afa2c0563d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952690"
---
# <a name="deleting-a-service"></a>Suppression d’un service

Un [programme de configuration de service](service-configuration-programs.md) utilise la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) pour obtenir un handle vers un objet de service installé. Le programme peut ensuite utiliser le descripteur d’objet de service dans la fonction [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) pour supprimer le service de la base de données SCM.

La fonction DoDeleteSvc de l’exemple suivant montre comment supprimer un service de la base de données SCM. La variable szSvcName est une variable globale qui contient le nom du service à supprimer. Pour obtenir l’exemple complet qui définit cette variable, consultez [SvcConfig. cpp](svcconfig-cpp.md).


```C++
//
// Purpose: 
//   Deletes a service from the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDeleteSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_STATUS ssStatus; 

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
        schSCManager,       // SCM database 
        szSvcName,          // name of service 
        DELETE);            // need delete access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Delete the service.
 
    if (! DeleteService(schService) ) 
    {
        printf("DeleteService failed (%d)\n", GetLastError()); 
    }
    else printf("Service deleted successfully\n"); 
 
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

 

 



