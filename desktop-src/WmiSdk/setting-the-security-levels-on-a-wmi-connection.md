---
description: Après avoir récupéré un pointeur vers un proxy IWbemServices, vous devez définir la sécurité sur le proxy pour accéder à WMI par le biais du proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Définition des niveaux de sécurité sur une connexion WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c2c4a492d4b40410b42fd9a94f22d346617a84d3baaa0679db325452a69c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315323"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a>Définition des niveaux de sécurité sur une connexion WMI

Après avoir récupéré un pointeur vers un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous devez définir la sécurité sur le proxy pour accéder à WMI par le biais du proxy. Vous devez définir la sécurité, car le proxy **IWbemServices** accorde l’accès à un objet hors processus. En général, la sécurité COM ne permet pas à un processus d’accéder à un autre processus si vous ne définissez pas les propriétés de sécurité appropriées. Pour plus d’informations, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md). Les connexions à différents systèmes d’exploitation nécessitent différents niveaux d’authentification et d’emprunt d’identité. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procédure suivante décrit comment définir les niveaux de sécurité sur une connexion WMI.

**Pour définir les niveaux de sécurité sur une connexion WMI**

-   Définissez les niveaux de sécurité sur le proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) à l’aide d’un appel à [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    L’exemple de code suivant décrit une méthode courante pour appeler [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

Une fois que vous avez défini les niveaux de sécurité pour votre pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous pouvez accéder aux diverses fonctionnalités de WMI. Une fois que vous avez fini d’utiliser WMI, vous devez arrêter votre application. Pour plus d’informations, consultez [nettoyage et arrêt d’une application WMI](cleaning-up-and-shutting-down-a-wmi-application.md).

 

 
