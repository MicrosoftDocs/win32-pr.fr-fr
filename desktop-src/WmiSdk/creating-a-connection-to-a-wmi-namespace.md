---
description: 'Une fois que vous avez défini les appels standard à COM, vous devez ensuite vous connecter à WMI via un appel à la méthode IWbemLocator :: ConnectServer.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Création d’une connexion à un espace de noms WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485744"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>Création d’une connexion à un espace de noms WMI

Une fois que vous avez défini les appels standard à COM, vous devez ensuite vous connecter à WMI via un appel à la méthode [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . La méthode **ConnectServer** retourne un proxy d’une interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Via **IWbemServices**, vous pouvez accéder aux différentes fonctionnalités de WMI.

Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procédure suivante décrit comment créer une connexion à un espace de noms WMI.

**Pour créer une connexion à un espace de noms WMI**

-   Initialisez l’interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) par le biais d’un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    WMI ne nécessite pas l’exécution de procédures supplémentaires lors de l’appel de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) sur [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    L’exemple de code suivant décrit comment initialiser [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   Connectez-vous à WMI via un appel à la méthode [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .

        La méthode [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) retourne un proxy à une interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) qui utilise pour accéder à l’espace de noms WMI local ou distant spécifié dans votre appel à **ConnectServer**.

        L’exemple de code suivant décrit comment appeler [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

Une fois que vous avez reçu un pointeur vers le proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous devez définir la sécurité sur le proxy pour accéder à WMI. Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Prise en charge D’ipv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
