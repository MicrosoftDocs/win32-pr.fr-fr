---
description: L’espace de stockage WMI contient des classes de performance préinstallées pour tous les objets de la bibliothèque de performances.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Accès aux classes de performance préinstallées par WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525088"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a><span data-ttu-id="24b3a-103">Accès aux classes de performance préinstallées par WMI</span><span class="sxs-lookup"><span data-stu-id="24b3a-103">Accessing WMI Preinstalled Performance Classes</span></span>

<span data-ttu-id="24b3a-104">L’espace de stockage WMI contient des classes de performance préinstallées pour tous les objets de la bibliothèque de performances.</span><span class="sxs-lookup"><span data-stu-id="24b3a-104">The WMI repository contains preinstalled performance classes for all the performance library objects.</span></span> <span data-ttu-id="24b3a-105">Par exemple, les instances du processus de la classe de performance données brutes [**Win32 \_ PerfRawData \_ perfproc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) représentent des processus.</span><span class="sxs-lookup"><span data-stu-id="24b3a-105">For example, instances of the raw data performance class [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represent processes.</span></span> <span data-ttu-id="24b3a-106">Cet objet de performance est visible dans le moniteur système en tant qu’objet processus.</span><span class="sxs-lookup"><span data-stu-id="24b3a-106">This performance object is visible in System Monitor as the Process object.</span></span>

<span data-ttu-id="24b3a-107">La propriété **PageFaultsPerSec** du [**\_ \_ \_ processus Win32 PerfRawData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) représente le compteur de performances défauts de page par seconde pour le processus.</span><span class="sxs-lookup"><span data-stu-id="24b3a-107">The **PageFaultsPerSec** property of [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represents the Page Faults per second performance counter for the process.</span></span> <span data-ttu-id="24b3a-108">Les [**classes \_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contiennent les valeurs de données calculées affichées dans le moniteur système (Perfmon.exe).</span><span class="sxs-lookup"><span data-stu-id="24b3a-108">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data values displayed in System Monitor (Perfmon.exe).</span></span> <span data-ttu-id="24b3a-109">La valeur de la propriété **PageFaultsPerSec** du [**\_ \_ \_ processus Win32 PerfFormattedData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) est identique à celle affichée dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="24b3a-109">The value of the **PageFaultsPerSec** property of [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) is the same as when it appears in System Monitor.</span></span>

<span data-ttu-id="24b3a-110">Utilisez l' [API com pour WMI](com-api-for-wmi.md) ou l' [API de script pour WMI](scripting-api-for-wmi.md) pour accéder aux données de performances via les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="24b3a-110">Use either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md) to access performance data through the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="24b3a-111">Dans les deux cas, un objet [*actualisateur*](gloss-r.md) est requis pour obtenir chaque échantillon de données.</span><span class="sxs-lookup"><span data-stu-id="24b3a-111">In both cases a [*refresher*](gloss-r.md) object is required to obtain each data sample.</span></span> <span data-ttu-id="24b3a-112">Pour plus d’informations et des exemples de code de script pour l’utilisation d’actualisateurs et l’accès aux classes de performance, consultez [tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="24b3a-112">For more information and script code examples for using refreshers and accessing performance classes, see [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span> <span data-ttu-id="24b3a-113">Pour plus d’informations, consultez [accès aux données de performances dans le script](accessing-performance-data-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="24b3a-113">For more information, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md).</span></span>

## <a name="accessing-performance-data-from-c"></a><span data-ttu-id="24b3a-114">Accès aux données de performances à partir de C++</span><span class="sxs-lookup"><span data-stu-id="24b3a-114">Accessing Performance Data from C++</span></span>

<span data-ttu-id="24b3a-115">L’exemple de code C++ suivant utilise le fournisseur de compteurs de performance pour accéder aux classes haute performance prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="24b3a-115">The following C++ code example uses the Performance Counter provider to access predefined high-performance classes.</span></span> <span data-ttu-id="24b3a-116">Il crée un objet actualiser et ajoute un objet à l’actualisateur.</span><span class="sxs-lookup"><span data-stu-id="24b3a-116">It creates a refresher object and adds an object to the refresher.</span></span> <span data-ttu-id="24b3a-117">L’objet est une instance de [**\_ \_ \_ processus Win32 PerfRawData perfproc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) qui surveille les performances d’un processus spécifique.</span><span class="sxs-lookup"><span data-stu-id="24b3a-117">The object is a [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instance that monitors the performance of a specific process.</span></span> <span data-ttu-id="24b3a-118">Le code lit uniquement une propriété de compteur dans l’objet processus, la propriété **Banque** .</span><span class="sxs-lookup"><span data-stu-id="24b3a-118">The code only reads one counter property in the process object, the **VirtualBytes** property.</span></span> <span data-ttu-id="24b3a-119">Le code requiert les références suivantes et les instructions **\# include** pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="24b3a-119">The code requires the following references and **\#include** statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="24b3a-120">La procédure suivante montre comment accéder aux données à partir d’un fournisseur de haute performance en C++.</span><span class="sxs-lookup"><span data-stu-id="24b3a-120">The following procedure shows how to access data from a high-performance provider in C++.</span></span>

<span data-ttu-id="24b3a-121">**Pour accéder aux données à partir d’un fournisseur de haute performance en C++**</span><span class="sxs-lookup"><span data-stu-id="24b3a-121">**To access data from a high-performance provider in C++**</span></span>

1.  <span data-ttu-id="24b3a-122">Établissez une connexion à l’espace de noms WMI et définissez la sécurité WMI à l’aide d’un appel à [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) et [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="24b3a-122">Establish a connection to the WMI namespace, and set WMI security by using a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) and [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="24b3a-123">Cette étape est une étape standard pour la création d’une application cliente WMI.</span><span class="sxs-lookup"><span data-stu-id="24b3a-123">This step is a standard step for creating any WMI client application.</span></span> <span data-ttu-id="24b3a-124">Pour plus d’informations, consultez [création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="24b3a-124">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

2.  <span data-ttu-id="24b3a-125">Créez un objet actualisateur en utilisant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec CLSID \_ WbemRefresher.</span><span class="sxs-lookup"><span data-stu-id="24b3a-125">Create a refresher object by using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_WbemRefresher.</span></span> <span data-ttu-id="24b3a-126">Demandez une interface [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) par le biais de la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="24b3a-126">Request an [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) interface through the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span> <span data-ttu-id="24b3a-127">Demandez une interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) par le biais de la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="24b3a-127">Request an [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface through the **QueryInterface** method.</span></span>

    <span data-ttu-id="24b3a-128">L’interface [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) est l’interface principale de l’objet [**actualisateur**](swbemrefreshableitem-refresher.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="24b3a-128">The [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface is the main interface for the WMI [**Refresher**](swbemrefreshableitem-refresher.md) object.</span></span>

    <span data-ttu-id="24b3a-129">L’exemple de code C++ suivant montre comment récupérer [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span><span class="sxs-lookup"><span data-stu-id="24b3a-129">The following C++ code example shows how to retrieve [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span></span>

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

    

3.  <span data-ttu-id="24b3a-130">Ajoutez un objet à l’actualisateur via un appel à la méthode [**IWbemConfigureRefresher :: AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .</span><span class="sxs-lookup"><span data-stu-id="24b3a-130">Add an object to the refresher through a call to the [**IWbemConfigureRefresher::AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) method.</span></span>

    <span data-ttu-id="24b3a-131">Lorsque vous ajoutez un objet à l’actualisateur, WMI actualise l’objet chaque fois que vous appelez la méthode [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="24b3a-131">When you add an object to the refresher, WMI refreshes the object whenever you call the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method.</span></span> <span data-ttu-id="24b3a-132">L’objet que vous ajoutez désigne le fournisseur dans ses qualificateurs de classe.</span><span class="sxs-lookup"><span data-stu-id="24b3a-132">The object you add designates the provider in its class qualifiers.</span></span>

    <span data-ttu-id="24b3a-133">L’exemple de code C++ suivant montre comment appeler [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span><span class="sxs-lookup"><span data-stu-id="24b3a-133">The following C++ code example shows how to call [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span></span>

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

    

4.  <span data-ttu-id="24b3a-134">Pour configurer un accès plus rapide à l’objet, connectez-vous à l’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) via [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="24b3a-134">To set up faster access to the object, connect to the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span>

    <span data-ttu-id="24b3a-135">L’exemple de code C++ suivant montre comment récupérer un pointeur vers l’objet à l’aide de [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) au lieu de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span><span class="sxs-lookup"><span data-stu-id="24b3a-135">The following C++ code example shows how to retrieve a pointer to the object using [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instead of [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span></span>

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    <span data-ttu-id="24b3a-136">L’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) augmente les performances, car vous pouvez obtenir des handles vers des propriétés de compteur spécifiques, et vous devez verrouiller et déverrouiller l’objet dans votre code, qui est une opération que [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) effectue pour chaque accès à une propriété.</span><span class="sxs-lookup"><span data-stu-id="24b3a-136">The [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface increases performance because you can get handles to specific counter properties, and it requires that you lock and unlock the object in your code, which is an operation that [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) performs for each property access.</span></span>

5.  <span data-ttu-id="24b3a-137">Obtenez les descripteurs des propriétés à examiner à l’aide d’appels à la méthode [**IWbemObjectAccess :: GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .</span><span class="sxs-lookup"><span data-stu-id="24b3a-137">Obtain the handles of the properties to examine by using calls to the [**IWbemObjectAccess::GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) method.</span></span>

    <span data-ttu-id="24b3a-138">Les handles de propriété sont les mêmes pour toutes les instances d’une classe, ce qui signifie que vous pouvez utiliser le handle de propriété que vous récupérez à partir d’une instance spécifique pour toutes les instances d’une classe spécifique.</span><span class="sxs-lookup"><span data-stu-id="24b3a-138">Property handles are the same for all instances of a class, which means that use the property handle you retrieve from a specific instance for all instances of a specific class.</span></span> <span data-ttu-id="24b3a-139">Vous pouvez également obtenir un handle à partir d’un objet de classe pour récupérer des valeurs de propriété à partir d’un objet d’instance.</span><span class="sxs-lookup"><span data-stu-id="24b3a-139">You can also obtain a handle from a class object to retrieve property values from an instance object.</span></span>

    <span data-ttu-id="24b3a-140">L’exemple de code C++ suivant montre comment récupérer un handle de propriété.</span><span class="sxs-lookup"><span data-stu-id="24b3a-140">The following C++ code example shows how to retrieve a property handle.</span></span>

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

    

6.  <span data-ttu-id="24b3a-141">Créez une boucle de programmation qui effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="24b3a-141">Create a programming loop that performs the following actions:</span></span>

    -   <span data-ttu-id="24b3a-142">Actualisez l’objet avec un appel à [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) en utilisant le pointeur créé dans l’appel précédent à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="24b3a-142">Refresh the object with a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) by using the pointer created in the previous call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

        <span data-ttu-id="24b3a-143">Dans cet appel, l’actualisateur WMI actualise l’objet client à l’aide des données fournies par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="24b3a-143">In this call, the WMI Refresher refreshes the client object by using data that the provider supplies.</span></span>

    -   <span data-ttu-id="24b3a-144">Effectuez toutes les actions nécessaires sur l’objet, telles que la récupération d’un nom de propriété, d’un type de données ou d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="24b3a-144">Perform any action as necessary on the object, such as retrieving a property name, data type, or value.</span></span>

        <span data-ttu-id="24b3a-145">Vous pouvez accéder à la propriété par le biais du handle de propriété obtenu précédemment.</span><span class="sxs-lookup"><span data-stu-id="24b3a-145">You can access the property through the property handle obtained earlier.</span></span> <span data-ttu-id="24b3a-146">En raison de l’appel d' [**actualisation**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , WMI actualise la propriété à chaque fois par la boucle.</span><span class="sxs-lookup"><span data-stu-id="24b3a-146">Due to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) call, WMI refreshes the property each time through the loop.</span></span>

<span data-ttu-id="24b3a-147">L’exemple C++ suivant montre comment utiliser l’API haute performance WMI.</span><span class="sxs-lookup"><span data-stu-id="24b3a-147">The following C++ example shows how to use the WMI high-performance API.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="24b3a-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24b3a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24b3a-149">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="24b3a-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="24b3a-150">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="24b3a-150">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
