---
title: Mots clés dynamiques de pare-feu
description: Vous utilisez les API de mots clés dynamiques de pare-feu pour gérer les adresses de mots clés dynamiques dans le pare-feu Microsoft Defender.
keywords:
- Mots clés dynamiques de pare-feu
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: bac179764b253035e0e8f1ef422f07bffb58821b55390c9c87d985bde5d2cdf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062529"
---
# <a name="firewall-dynamic-keywords"></a>Mots clés dynamiques de pare-feu

Vous utilisez les API de mots clés dynamiques de pare-feu pour gérer les *adresses de mots clés dynamiques* dans le [pare-feu Microsoft Defender](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security). Une adresse de mot clé dynamique est utilisée pour créer un ensemble d’adresses IP auxquelles une ou plusieurs règles de pare-feu peuvent faire référence. Les adresses de mots clés dynamiques prennent en charge IPv4 et IPv6.

> [!NOTE]
> Pour obtenir des informations de référence sur les API des API présentées dans cette rubrique, consultez [référence des mots clés dynamiques de pare-feu](firewall-dynamic-keywords-reference.md).

## <a name="operations-on-dynamic-keyword-addresses"></a>Opérations sur les adresses de mots clés dynamiques

Avec les API de mots clés dynamiques de pare-feu, vous pouvez effectuer les opérations suivantes.

* Ajouter des adresses de mots clés dynamiques
* Supprimer les adresses de mots clés dynamiques
* Énumérer les adresses de mots clés dynamiques par ID ou par type
* Mettre à jour les adresses de mots clés dynamiques
* S’abonner aux notifications de modification des adresses de mots clés dynamiques et les gérer

Il existe des exemples de code pour toutes ces opérations plus loin dans cette rubrique.

Une fois que vous avez ajouté une adresse de mot clé dynamique, elle persiste entre les redémarrages. Vous devez supprimer une adresse de mot clé dynamique une fois que vous avez fini d’utiliser l’objet.

Il existe deux classes d’adresses de mots clés dynamiques, comme décrit dans les deux sections suivantes.

## <a name="autoresolve-dynamic-keyword-addresses"></a>Résoudre automatiquement les adresses de mots clés dynamiques

Le premier type est *autosolve*, où le champ de *mot clé* représente un nom pouvant être résolu, et les adresses IP ne sont pas définies lors de la création.

Ces objets sont conçus pour que leurs adresses IP soient résolues automatiquement. Autrement dit, pas via un administrateur au moment de la création de l’objet ; ni via le système d’exploitation lui-même. Un composant en dehors du service de pare-feu doit effectuer la résolution d’adresse IP pour ces objets et les mettre à jour de manière appropriée. L’implémentation d’un tel composant n’est pas la portée de ce contenu.

Une adresse de mot clé dynamique est indiquée comme étant *autosolve* en définissant l’indicateur **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** dans l’objet lors de l’appel de la fonction [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) . Le champ de *mot clé* doit être utilisé pour représenter la valeur résolue &mdash; , c’est-à-dire un nom de domaine complet (FQDN) ou un nom d’hôte. Initialement, le champ d' *adresses* doit avoir la valeur null pour ces objets. Ces objets n’auront pas leurs adresses IP conservées entre les cycles de démarrage et vous devrez réévaluer/remplir à nouveau leurs adresses au cours du prochain cycle de démarrage.

> [!NOTE]
> Résoudre automatiquement les objets d’adresse de mot clé dynamique déclenchent des notifications sur [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) et [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), mais pas sur [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).

## <a name="non-autoresolve-dynamic-keyword-addresses"></a>Adresses de mots clés dynamiques non résolues automatiquement

Le deuxième type est *non autosolve*, où le champ de *mot clé* est une chaîne, et les adresses sont définies au moment de la création.

Ces objets sont utilisés pour stocker un ensemble d’adresses IP, de sous-réseaux ou de plages. Le champ de *mot clé* ici est utilisé à des fins de gestion et peut être défini sur n’importe quelle chaîne. Le champ *adresses* ne doit pas avoir la valeur null lors de la création. Les adresses de ces objets sont conservées entre les redémarrages.

> [!NOTE]
> Les objets d’adresse de mot clé dynamique non résolus automatiquement déclenchent des notifications sur [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)et [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).

## <a name="more-about-dynamic-keyword-addresses"></a>En savoir plus sur les adresses de mots clés dynamiques 

Toutes les adresses de mots clés dynamiques doivent avoir un identificateur [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) unique pour les représenter.

L’API [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) fournit des notifications à un client lorsque les adresses de mots clés dynamiques changent. Aucune charge utile n’est fournie au client pour décrire exactement ce qui a changé sur le système. Si vous avez besoin de savoir quels objets ont changé, vous devez interroger l’état actuel des objets sur le système à l’aide des API [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) ou [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) . Vous pouvez utiliser les différents indicateurs pour demander des notifications uniquement pour un sous-ensemble d’objets. Si vous n’utilisez aucun indicateur, les notifications de modification sont remises pour tous les objets.

Une règle de pare-feu peut utiliser des adresses de mots clés dynamiques au lieu de définir explicitement des adresses IP pour sa condition d’adresse distante. Une règle de pare-feu peut utiliser à la fois des adresses de mots clés dynamiques et des plages d’adresses distantes définies statiquement. Un seul objet d’adresse de mot clé dynamique peut être réutilisé sur plusieurs règles de pare-feu. Si une règle de pare-feu n’a aucune adresse distante configurée (c’est-à-dire configurée uniquement avec des objets qui n’ont pas encore été résolus), la règle n’est pas appliquée. En outre, si une règle utilise plusieurs adresses de mots clés dynamiques, la règle est appliquée à toutes les adresses qui sont actuellement résolues, même s’il existe d’autres objets qui ne sont pas encore résolus. Lorsqu’une adresse de mot clé dynamique est mise à jour, les adresses distantes sont également mises à jour pour tous les objets de règle associés.

Le système d’exploitation lui-même n’impose aucune dépendance entre une règle et une adresse de mot clé dynamique. Cela signifie que l’un ou l’autre objet peut être créé &mdash; en premier, la règle peut faire référence à des ID d’adresse de mot clé dynamique qui n’existent pas encore (dans ce cas, la règle ne sera pas appliquée). En outre, vous pouvez supprimer une adresse de mot clé dynamique, même si elle est utilisée par une règle de pare-feu. Cette rubrique décrit comment un administrateur peut configurer des règles pour utiliser l’adresse de mot clé dynamique.

## <a name="code-examples"></a>Exemples de code

pour essayer chacun de ces exemples de code, lancez d’abord Visual Studio et créez un projet basé sur le modèle de projet d' **application Console** . Vous pouvez simplement remplacer le contenu de `main.cpp` par la liste de code.

la plupart des exemples de code utilisent les [bibliothèques d’implémentation de Windows (WIL)](https://github.com/Microsoft/wil). pour installer le WIL, il est pratique d’accéder à Visual Studio, de cliquer sur **Project** \> **gérer les Packages de NuGet...** \> **parcourir**, tapez ou collez **Microsoft. Windows. ImplementationLibrary** dans la zone de recherche, sélectionnez l’élément dans les résultats de la recherche, puis cliquez sur **installer** pour installer le package pour ce projet.

> [!NOTE]
> Les types de pointeurs pour les fonctions Free NetFw sont publiés via `NetFw.h` , mais une bibliothèque de liens statiques n’est pas publiée. Utilisez le modèle [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) / [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour appeler ces fonctions, comme indiqué dans ces exemples de code.

### <a name="add-a-dynamic-keyword-address"></a>Ajouter une adresse de mot clé dynamique

Cet exemple montre comment utiliser la fonction [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) .

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a>Supprimer une adresse de mot clé dynamique

Cet exemple montre comment utiliser la fonction [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) .

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a>Énumérer et libérer des adresses de mots clés dynamiques par ID

Cet exemple montre comment utiliser les fonctions [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) et [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) .

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a>Énumérer et libérer des adresses de mots clés dynamiques par type

Cet exemple montre comment utiliser les fonctions [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) et [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) .

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a>Mettre à jour les adresses de mots clés dynamiques

Cet exemple montre comment utiliser la fonction [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) .

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a>S’abonner aux notifications de modification des adresses de mots clés dynamiques et les gérer

Cet exemple montre comment utiliser les fonctions [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) et [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) , ainsi que le rappel [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) .

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a>Rubriques connexes

* [Référence des mots clés dynamiques du pare-feu](firewall-dynamic-keywords-reference.md)
