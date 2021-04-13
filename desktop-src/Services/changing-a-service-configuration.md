---
description: Un programme de configuration de service utilise les fonctions ChangeServiceConfig et ChangeServiceConfig2 pour modifier les paramètres de configuration d’un service installé.
ms.assetid: 79aa4ad5-87ee-4f5d-9c8e-4e788f4c7182
title: Modification de la configuration des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7afffcb896e7732536ad308ccd54f0ae1f0a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319586"
---
# <a name="changing-a-services-configuration"></a><span data-ttu-id="cd3a6-103">Modification de la configuration d’un service</span><span class="sxs-lookup"><span data-stu-id="cd3a6-103">Changing a Service's Configuration</span></span>

<span data-ttu-id="cd3a6-104">Un [programme de configuration de service](service-configuration-programs.md) utilise les fonctions [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) et [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) pour modifier les paramètres de configuration d’un service installé.</span><span class="sxs-lookup"><span data-stu-id="cd3a6-104">A [service configuration program](service-configuration-programs.md) uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) and [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) functions to change the configuration parameters of an installed service.</span></span> <span data-ttu-id="cd3a6-105">Le programme ouvre un handle pour l’objet de service, modifie sa configuration, puis ferme le descripteur d’objet de service.</span><span class="sxs-lookup"><span data-stu-id="cd3a6-105">The program opens a handle to the service object, modifies its configuration, and then closes the service object handle.</span></span>

<span data-ttu-id="cd3a6-106">Dans l’exemple suivant, la fonction DoDisableSvc utilise [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) pour remplacer le type de démarrage du service par « Disabled », la fonction DoEnableSvc utilise **ChangeServiceConfig** pour remplacer le type de démarrage du service par « Enabled », et la fonction DoUpdateSvcDesc utilise [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) pour définir la description de service sur « This is a test Description ».</span><span class="sxs-lookup"><span data-stu-id="cd3a6-106">In the following example, the DoDisableSvc function uses [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) to change the service start type to "Disabled", the DoEnableSvc function uses **ChangeServiceConfig** to change the service start type to "Enabled", and the DoUpdateSvcDesc function uses [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) to set the service description to "This is a test description".</span></span> <span data-ttu-id="cd3a6-107">La variable szSvcName est une variable globale qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="cd3a6-107">The szSvcName variable is a global variable that contains the name of the service.</span></span> <span data-ttu-id="cd3a6-108">Pour obtenir l’exemple complet qui définit cette variable, consultez [SvcConfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="cd3a6-108">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Disables the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDisableSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;

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
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service start type.

    if (! ChangeServiceConfig( 
        schService,        // handle of service 
        SERVICE_NO_CHANGE, // service type: no change 
        SERVICE_DISABLED,  // service start type 
        SERVICE_NO_CHANGE, // error control: no change 
        NULL,              // binary path: no change 
        NULL,              // load order group: no change 
        NULL,              // tag ID: no change 
        NULL,              // dependencies: no change 
        NULL,              // account name: no change 
        NULL,              // password: no change 
        NULL) )            // display name: no change
    {
        printf("ChangeServiceConfig failed (%d)\n", GetLastError()); 
    }
    else printf("Service disabled successfully.\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

//
// Purpose: 
//   Enables the service.
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoEnableSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;

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
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service start type.

    if (! ChangeServiceConfig( 
        schService,            // handle of service 
        SERVICE_NO_CHANGE,     // service type: no change 
        SERVICE_DEMAND_START,  // service start type 
        SERVICE_NO_CHANGE,     // error control: no change 
        NULL,                  // binary path: no change 
        NULL,                  // load order group: no change 
        NULL,                  // tag ID: no change 
        NULL,                  // dependencies: no change 
        NULL,                  // account name: no change 
        NULL,                  // password: no change 
        NULL) )                // display name: no change
    {
        printf("ChangeServiceConfig failed (%d)\n", GetLastError()); 
    }
    else printf("Service enabled successfully.\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}

//
// Purpose: 
//   Updates the service description to "This is a test description".
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoUpdateSvcDesc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_DESCRIPTION sd;
    LPTSTR szDesc = TEXT("This is a test description");

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
        schSCManager,            // SCM database 
        szSvcName,               // name of service 
        SERVICE_CHANGE_CONFIG);  // need change config access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }    

    // Change the service description.

    sd.lpDescription = szDesc;

    if( !ChangeServiceConfig2(
        schService,                 // handle to service
        SERVICE_CONFIG_DESCRIPTION, // change: description
        &sd) )                      // new description
    {
        printf("ChangeServiceConfig2 failed\n");
    }
    else printf("Service description updated successfully.\n");

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="cd3a6-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd3a6-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd3a6-110">Configuration de service</span><span class="sxs-lookup"><span data-stu-id="cd3a6-110">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="cd3a6-111">Exemple de service complet</span><span class="sxs-lookup"><span data-stu-id="cd3a6-111">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



