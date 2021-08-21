---
description: Chargement de VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Chargement de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec6a757b57c8e06e53862b3d36b9d54f291e4b07693dff008ecc2bbbb961c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125939"
---
# <a name="loading-vds"></a>Chargement de VDS

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

**Pour charger et initialiser VDS**

1.  Libère les interfaces non null.
2.  Appelez la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)ou [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) pour obtenir un pointeur vers l’objet service Loader.

    **CLSCTX \_ Impossible \_** de spécifier AAA dans cet appel. Si la méthode [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) est appelée, **EOAC \_ Disable \_ AAA** ne peut pas être spécifié dans le paramètre *dwCapabilities* .

3.  Appelez la méthode [**IVdsServiceLoader :: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) pour charger VDS.

    Le passage de la **valeur null** en tant que premier paramètre charge et initialise VDS sur l’hôte local.

4.  Appelez la méthode [**IVdsService :: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) pour attendre la fin de l’initialisation de VDS.

L’exemple de code suivant initialise le service qui retourne un pointeur vers l’objet de service.


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de VDS](using-vds.md)
</dt> <dt>

[**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Objets d’installation et de service](startup-and-service-objects.md)
</dt> </dl>

 

 
