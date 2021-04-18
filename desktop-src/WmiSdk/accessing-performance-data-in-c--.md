---
description: L’API WMI hautes performances est une série d’interfaces qui obtiennent des données à partir de classes de compteurs de performances.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Accès aux données de performances en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522827"
---
# <a name="accessing-performance-data-in-c"></a>Accès aux données de performances en C++

L’API WMI hautes performances est une série d’interfaces qui obtiennent des données à partir de [classes de compteurs de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes). Ces interfaces requièrent l’utilisation d’un objet [*actualisateur*](gloss-r.md) pour augmenter le taux d’échantillonnage. Pour plus d’informations sur l’utilisation de l’objet actualisateur dans les scripts, consultez [accès aux données de performances dans le script](accessing-performance-data-in-script.md) et les [tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md).

Les sections suivantes sont présentées dans cette rubrique :

-   [Actualisation des données de performances](#refreshing-performance-data)
-   [Ajout d’énumérateurs à l’actualisateur WMI](#adding-enumerators-to-the-wmi-refresher)
-   [Exemple](#example)
-   [Rubriques connexes](#related-topics)

## <a name="refreshing-performance-data"></a>Actualisation des données de performances

Un objet actualisateur augmente les performances du fournisseur de données et du client en extrayant les données sans franchir les limites du processus. Si le client et le serveur sont tous deux situés sur le même ordinateur, un actualisateur charge le fournisseur de haute performance en cours de traitement sur le client, et copie les données directement à partir des objets de fournisseur dans les objets clients. Si le client et le serveur se trouvent sur des ordinateurs différents, l’actualisateur augmente les performances en mettant en cache les objets sur l’ordinateur distant et en transmettant le nombre minimal de jeux de données au client.

Un actualisateur également :

-   Reconnecte automatiquement un client à un service WMI distant lorsqu’une erreur réseau se produit ou lorsque l’ordinateur distant est redémarré.

    Par défaut, un actualisateur tente de reconnecter votre application au fournisseur haute performance approprié lorsqu’une connexion à distance entre les deux ordinateurs échoue. Pour empêcher la reconnexion, transmettez l’indicateur **WBEM \_ \_ ne pas actualiser l’indicateur de \_ \_ \_ reconnexion automatique** dans l’appel de la méthode [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) . Les clients de script doivent définir la propriété [**SWbemRefresher. reconnexion automatique**](swbemrefresher-autoreconnect.md) sur **false**.

-   Charge plusieurs objets et énumérateurs fournis par le même fournisseur ou des fournisseurs différents.

    Vous permet d’ajouter plusieurs objets, énumérateurs ou les deux à un actualisateur.

-   Énumère les objets.

    Comme les autres fournisseurs, un fournisseur de haute performance peut énumérer des objets.

Une fois que vous avez fini d’écrire votre client hautes performances, vous souhaiterez peut-être améliorer le temps de réponse. Étant donné que l’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) est optimisée pour la vitesse, l’interface n’est pas intrinsèquement threadsafe. Par conséquent, au cours d’une opération d’actualisation, n’accédez pas à l’objet ou à l’énumération actualisable. Pour protéger des objets entre les threads pendant les appels de méthode **IWbemObjectAccess** , utilisez les méthodes [**IWbemObjectAccess :: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) et [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) . Pour améliorer les performances, synchronisez vos threads afin de ne pas avoir à verrouiller des threads individuels. La réduction des threads et la synchronisation des groupes d’objets pour les opérations d’actualisation offrent les meilleures performances globales.

## <a name="adding-enumerators-to-the-wmi-refresher"></a>Ajout d’énumérateurs à l’actualisateur WMI

Le nombre d’instances et de données de chaque instance est actualisé en ajoutant un énumérateur à l’actualisateur afin que chaque appel à [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) donne une énumération complète.

L’exemple de code C++ suivant requiert les références suivantes et les \# instructions include pour compiler correctement.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procédure suivante montre comment ajouter un énumérateur à un actualisateur.

**Pour ajouter un énumérateur à un actualisateur**

1.  Appelez la méthode [**IWbemConfigureRefresher :: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) à l’aide du chemin d’accès à l’objet actualisable et de l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

    L’actualisateur retourne un pointeur vers une interface [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) . Vous pouvez utiliser l’interface **IWbemHiPerfEnum** pour accéder aux objets de l’énumération.

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  Créez une boucle qui effectue les actions suivantes :

    -   Actualise l’objet à l’aide d’un appel à [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).
    -   Fournit un tableau de pointeurs d’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) à la méthode [**IWbemHiPerfEnum :: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .
    -   Accède aux propriétés de l’énumérateur à l’aide des méthodes [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) passées dans [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

        Un descripteur de propriété peut être passé à chaque instance [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) pour récupérer la valeur actualisée. Le client doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer les pointeurs **IWbemObjectAccess** retournés par [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

## <a name="example"></a>Exemple

L’exemple de code C++ suivant énumère une classe à hautes performances, où le client récupère un handle de propriété à partir du premier objet et réutilise le handle pour le reste de l’opération d’actualisation. Chaque appel à la méthode [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) met à jour le nombre d’instances et les données d’instance.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes du compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accès aux données de performances dans le script](accessing-performance-data-in-script.md)
</dt> <dt>

[Actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> <dt>

[Qualificateurs de propriété pour les classes de compteur de performance mises en forme](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
