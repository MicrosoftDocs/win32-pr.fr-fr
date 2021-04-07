---
description: Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, récupère les données semisynchronously, puis nettoie.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 'Exemple : obtention de données WMI à partir de l’ordinateur local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840cd4ada941bdfd8ba7fca9b8ca9393c0b5eb55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864018"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a>Exemple : obtention de données WMI à partir de l’ordinateur local

Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, récupère les données semisynchronously, puis nettoie. Cet exemple obtient le nom du système d’exploitation sur l’ordinateur local et l’affiche. Pour récupérer des données à partir d’un ordinateur distant, consultez [exemple : obtention de données WMI à partir d’un ordinateur distant](example--getting-wmi-data-from-a-remote-computer.md). Pour obtenir les données de manière asynchrone, consultez [exemple : obtention de données WMI à partir de l’ordinateur local de manière asynchrone](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

La procédure suivante est utilisée pour exécuter l’application WMI. Les étapes 1 à 5 contiennent toutes les étapes nécessaires à la configuration et à la connexion à WMI, et les étapes 6 et 7 sont l’endroit où les données sont interrogées et reçues.

1.  Initialisez les paramètres COM avec un appel à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).

2.  Initialisez la sécurité des processus COM en appelant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md).

3.  Obtenez le localisateur initial pour WMI en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Obtenez un pointeur vers [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour l' \\ espace de noms CIMV2 racine sur l’ordinateur local en appelant [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Pour vous connecter à un ordinateur distant, consultez [exemple : obtention de données WMI à partir d’un ordinateur distant](example--getting-wmi-data-from-a-remote-computer.md).

    Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).

5.  Définissez la sécurité du proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) afin que le service WMI puisse emprunter l’identité du client en appelant [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).

6.  Utilisez le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour effectuer des demandes WMI. Cet exemple exécute une requête pour le nom du système d’exploitation en appelant [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    La requête WQL suivante est l’un des arguments de méthode.

    `SELECT * FROM Win32_OperatingSystem`

    Le résultat de cette requête est stocké dans un pointeur [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Cela permet aux objets de données de la requête d’être récupérés semisynchronously avec l’interface **IEnumWbemClassObject** . Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md). Pour obtenir les données de manière asynchrone, consultez [exemple : obtention de données WMI à partir de l’ordinateur local de manière asynchrone](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

    Pour plus d’informations sur la création de requêtes à WMI, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md), [interrogation de WMI](querying-wmi.md)et [appel d’une méthode](calling-a-method.md).

7.  Obtenir et afficher les données de la requête WQL. Le pointeur [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) est lié aux objets de données retournés par la requête, et les objets de données peuvent être récupérés avec la méthode [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) . Cette méthode lie les objets de données à un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) passé dans la méthode. Utilisez la méthode [**IWbemClassObject :: obten**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) pour récupérer les informations souhaitées à partir des objets de données.

    L’exemple de code suivant est utilisé pour récupérer la propriété Name de l’objet de données, qui fournit le nom du système d’exploitation.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    Une fois que la valeur de la propriété Name est stockée dans la variable [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) vtProp, elle peut être affichée à l’utilisateur.

    Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md).

L’exemple de code suivant récupère des semisynchronously de données WMI à partir d’un ordinateur local.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



 

 
