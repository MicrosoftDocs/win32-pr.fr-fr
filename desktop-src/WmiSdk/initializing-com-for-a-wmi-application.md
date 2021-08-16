---
description: La première étape de la connexion à WMI consiste à configurer les appels COM vers CoInitializeEx et CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Initialisation de COM pour une application WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723188602e440cd3ba49d78d8efb3c28ddae30f35dd0d4361a4fdb5ced026ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318573"
---
# <a name="initializing-com-for-a-wmi-application"></a>Initialisation de COM pour une application WMI

La première étape de la connexion à WMI consiste à configurer les appels COM vers [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procédure suivante décrit comment initialiser COM à partir d’une application cliente.

**Pour initialiser COM à partir d’une application cliente**

1.  Initialisez COM avec un appel à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    L’appel de [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) est une procédure standard pour configurer une interface com. Par conséquent, WMI ne nécessite pas que vous observiez des procédures supplémentaires lors de l’appel de **CoInitializeEx**. Pour plus d’informations, consultez [com](../com/component-object-model--com--portal.md).

    L’exemple de code suivant décrit comment appeler [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  Définissez les niveaux de sécurité COM généraux à l’aide d’un appel à l’interface [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) est une fonction standard que vous devez appeler lors de la configuration d’une interface com pour un processus. Appelez **CoInitializeSecurity** si vous souhaitez définir les paramètres de sécurité par défaut pour l’authentification, l’emprunt d’identité ou le service d’authentification pour un processus entier. Pour plus d’informations, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md). Si vous souhaitez définir ou modifier la sécurité pour un proxy spécifique, vous devez appeler [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Utilisez **CoSetProxyBlanket** chaque fois que vous devez définir ou modifier la sécurité com lors de l’exécution dans un autre processus où vous ne pouvez pas contrôler les paramètres de sécurité par défaut pour l’authentification, l’emprunt d’identité ou le service d’authentification. Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md) et [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

    WMI présente plusieurs problèmes de sécurité que vous devez connaître lors de la programmation d’une application cliente WMI. Pour plus d’informations, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md).

    L’exemple de code suivant décrit comment appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité com sur le processus.

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

Après l’initialisation de COM, l’étape suivante consiste à créer une connexion à un espace de noms WMI. Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
