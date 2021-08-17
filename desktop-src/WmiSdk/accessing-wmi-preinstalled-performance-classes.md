---
description: L’espace de stockage WMI contient des classes de performance préinstallées pour tous les objets de la bibliothèque de performances.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Accès aux classes de performance préinstallées par WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656c3434d2f20bd73ae9ff5273f7e67439fc6caa01ac9ee5bf0283850e64b34a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131892"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>Accès aux classes de performance préinstallées par WMI

L’espace de stockage WMI contient des classes de performance préinstallées pour tous les objets de la bibliothèque de performances. Par exemple, les instances du processus de la classe de performance données brutes [**Win32 \_ PerfRawData \_ perfproc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) représentent des processus. Cet objet de performance est visible dans le moniteur système en tant qu’objet processus.

La propriété **PageFaultsPerSec** du [**\_ \_ \_ processus Win32 PerfRawData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) représente le compteur de performances défauts de page par seconde pour le processus. Les [**classes \_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contiennent les valeurs de données calculées affichées dans le moniteur système (Perfmon.exe). La valeur de la propriété **PageFaultsPerSec** du [**\_ \_ \_ processus Win32 PerfFormattedData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) est identique à celle affichée dans le moniteur système.

Utilisez l' [API com pour WMI](com-api-for-wmi.md) ou l' [API de script pour WMI](scripting-api-for-wmi.md) pour accéder aux données de performances via les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes). Dans les deux cas, un objet [*actualisateur*](gloss-r.md) est requis pour obtenir chaque échantillon de données. Pour plus d’informations et des exemples de code de script pour l’utilisation d’actualisateurs et l’accès aux classes de performance, consultez [tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md). Pour plus d’informations, consultez [accès aux données de performances dans le script](accessing-performance-data-in-script.md).

## <a name="accessing-performance-data-from-c"></a>Accès aux données de performances à partir de C++

L’exemple de code C++ suivant utilise le fournisseur de compteurs de performance pour accéder aux classes haute performance prédéfinies. Il crée un objet actualiser et ajoute un objet à l’actualisateur. L’objet est une instance de [**\_ \_ \_ processus Win32 PerfRawData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) qui surveille les performances d’un processus spécifique. Le code lit uniquement une propriété de compteur dans l’objet processus, la propriété **Banque** . Le code requiert les références suivantes et les instructions **\# include** pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procédure suivante montre comment accéder aux données à partir d’un fournisseur de haute performance en C++.

**Pour accéder aux données à partir d’un fournisseur de haute performance en C++**

1.  Établissez une connexion à l’espace de noms WMI et définissez la sécurité WMI à l’aide d’un appel à [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) et [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Cette étape est une étape standard pour la création d’une application cliente WMI. Pour plus d’informations, consultez [création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md).

2.  Créez un objet actualisateur en utilisant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec CLSID \_ WbemRefresher. Demandez une interface [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) par le biais de la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . Demandez une interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) par le biais de la méthode **QueryInterface** .

    L’interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) est l’interface principale de l’objet [**actualisateur**](swbemrefreshableitem-refresher.md) WMI.

    L’exemple de code C++ suivant montre comment récupérer [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  Ajoutez un objet à l’actualisateur via un appel à la méthode [**IWbemConfigureRefresher :: AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .

    Lorsque vous ajoutez un objet à l’actualisateur, WMI actualise l’objet chaque fois que vous appelez la méthode [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) . L’objet que vous ajoutez désigne le fournisseur dans ses qualificateurs de classe.

    L’exemple de code C++ suivant montre comment appeler [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  Pour configurer un accès plus rapide à l’objet, connectez-vous à l’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) via [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .

    L’exemple de code C++ suivant montre comment récupérer un pointeur vers l’objet à l’aide de [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) au lieu de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    L’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) augmente les performances, car vous pouvez obtenir des handles vers des propriétés de compteur spécifiques, et vous devez verrouiller et déverrouiller l’objet dans votre code, qui est une opération que [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) effectue pour chaque accès à une propriété.

5.  Obtenez les descripteurs des propriétés à examiner à l’aide d’appels à la méthode [**IWbemObjectAccess :: GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .

    Les handles de propriété sont les mêmes pour toutes les instances d’une classe, ce qui signifie que vous pouvez utiliser le handle de propriété que vous récupérez à partir d’une instance spécifique pour toutes les instances d’une classe spécifique. Vous pouvez également obtenir un handle à partir d’un objet de classe pour récupérer des valeurs de propriété à partir d’un objet d’instance.

    L’exemple de code C++ suivant montre comment récupérer un handle de propriété.

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  Créez une boucle de programmation qui effectue les actions suivantes :

    -   Actualisez l’objet avec un appel à [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) en utilisant le pointeur créé dans l’appel précédent à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

        Dans cet appel, l’actualisateur WMI actualise l’objet client à l’aide des données fournies par le fournisseur.

    -   Effectuez toutes les actions nécessaires sur l’objet, telles que la récupération d’un nom de propriété, d’un type de données ou d’une valeur.

        Vous pouvez accéder à la propriété par le biais du handle de propriété obtenu précédemment. En raison de l’appel d' [**actualisation**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , WMI actualise la propriété à chaque fois par la boucle.

L’exemple C++ suivant montre comment utiliser l’API haute performance WMI.


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes du compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
