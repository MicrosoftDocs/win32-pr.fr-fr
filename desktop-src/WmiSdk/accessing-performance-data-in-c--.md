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
# <a name="accessing-performance-data-in-c"></a><span data-ttu-id="e5f17-103">Accès aux données de performances en C++</span><span class="sxs-lookup"><span data-stu-id="e5f17-103">Accessing Performance Data in C++</span></span>

<span data-ttu-id="e5f17-104">L’API WMI hautes performances est une série d’interfaces qui obtiennent des données à partir de [classes de compteurs de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="e5f17-104">The WMI high-performance API is a series of interfaces that obtain data from [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="e5f17-105">Ces interfaces requièrent l’utilisation d’un objet [*actualisateur*](gloss-r.md) pour augmenter le taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e5f17-105">These interfaces require use of a [*refresher*](gloss-r.md) object to increase the sampling rate.</span></span> <span data-ttu-id="e5f17-106">Pour plus d’informations sur l’utilisation de l’objet actualisateur dans les scripts, consultez [accès aux données de performances dans le script](accessing-performance-data-in-script.md) et les [tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="e5f17-106">For more information about using the refresher object in scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span>

<span data-ttu-id="e5f17-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="e5f17-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="e5f17-108">Actualisation des données de performances</span><span class="sxs-lookup"><span data-stu-id="e5f17-108">Refreshing Performance Data</span></span>](#refreshing-performance-data)
-   [<span data-ttu-id="e5f17-109">Ajout d’énumérateurs à l’actualisateur WMI</span><span class="sxs-lookup"><span data-stu-id="e5f17-109">Adding Enumerators to the WMI Refresher</span></span>](#adding-enumerators-to-the-wmi-refresher)
-   [<span data-ttu-id="e5f17-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5f17-110">Example</span></span>](#example)
-   [<span data-ttu-id="e5f17-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5f17-111">Related topics</span></span>](#related-topics)

## <a name="refreshing-performance-data"></a><span data-ttu-id="e5f17-112">Actualisation des données de performances</span><span class="sxs-lookup"><span data-stu-id="e5f17-112">Refreshing Performance Data</span></span>

<span data-ttu-id="e5f17-113">Un objet actualisateur augmente les performances du fournisseur de données et du client en extrayant les données sans franchir les limites du processus.</span><span class="sxs-lookup"><span data-stu-id="e5f17-113">A refresher object increases data provider and client performance by retrieving data without crossing process boundaries.</span></span> <span data-ttu-id="e5f17-114">Si le client et le serveur sont tous deux situés sur le même ordinateur, un actualisateur charge le fournisseur de haute performance en cours de traitement sur le client, et copie les données directement à partir des objets de fournisseur dans les objets clients.</span><span class="sxs-lookup"><span data-stu-id="e5f17-114">If both the client and the server are located on the same computer, a refresher loads the high-performance provider in-process to the client, and copies data directly from provider objects into client objects.</span></span> <span data-ttu-id="e5f17-115">Si le client et le serveur se trouvent sur des ordinateurs différents, l’actualisateur augmente les performances en mettant en cache les objets sur l’ordinateur distant et en transmettant le nombre minimal de jeux de données au client.</span><span class="sxs-lookup"><span data-stu-id="e5f17-115">If the client and the server are located on different computers, the refresher increases performance by caching objects on the remote computer, and transmitting minimal data sets to the client.</span></span>

<span data-ttu-id="e5f17-116">Un actualisateur également :</span><span class="sxs-lookup"><span data-stu-id="e5f17-116">A refresher also:</span></span>

-   <span data-ttu-id="e5f17-117">Reconnecte automatiquement un client à un service WMI distant lorsqu’une erreur réseau se produit ou lorsque l’ordinateur distant est redémarré.</span><span class="sxs-lookup"><span data-stu-id="e5f17-117">Automatically reconnects a client to a remote WMI service when a network error occurs, or the remote computer is restarted.</span></span>

    <span data-ttu-id="e5f17-118">Par défaut, un actualisateur tente de reconnecter votre application au fournisseur haute performance approprié lorsqu’une connexion à distance entre les deux ordinateurs échoue.</span><span class="sxs-lookup"><span data-stu-id="e5f17-118">By default, a refresher attempts to reconnect your application to the relevant high-performance provider when a remote connection between the two computers fails.</span></span> <span data-ttu-id="e5f17-119">Pour empêcher la reconnexion, transmettez l’indicateur **WBEM \_ \_ ne pas actualiser l’indicateur de \_ \_ \_ reconnexion automatique** dans l’appel de la méthode [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="e5f17-119">To prevent the reconnection, pass the **WBEM\_FLAG\_REFRESH\_NO\_AUTO\_RECONNECT** flag in the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method call.</span></span> <span data-ttu-id="e5f17-120">Les clients de script doivent définir la propriété [**SWbemRefresher. reconnexion automatique**](swbemrefresher-autoreconnect.md) sur **false**.</span><span class="sxs-lookup"><span data-stu-id="e5f17-120">Scripting clients must set the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **FALSE**.</span></span>

-   <span data-ttu-id="e5f17-121">Charge plusieurs objets et énumérateurs fournis par le même fournisseur ou des fournisseurs différents.</span><span class="sxs-lookup"><span data-stu-id="e5f17-121">Loads multiple objects and enumerators that are provided by the same or different providers.</span></span>

    <span data-ttu-id="e5f17-122">Vous permet d’ajouter plusieurs objets, énumérateurs ou les deux à un actualisateur.</span><span class="sxs-lookup"><span data-stu-id="e5f17-122">Allows you to add multiple objects, enumerators, or both to a refresher.</span></span>

-   <span data-ttu-id="e5f17-123">Énumère les objets.</span><span class="sxs-lookup"><span data-stu-id="e5f17-123">Enumerates objects.</span></span>

    <span data-ttu-id="e5f17-124">Comme les autres fournisseurs, un fournisseur de haute performance peut énumérer des objets.</span><span class="sxs-lookup"><span data-stu-id="e5f17-124">Like other providers, a high-performance provider can enumerate objects.</span></span>

<span data-ttu-id="e5f17-125">Une fois que vous avez fini d’écrire votre client hautes performances, vous souhaiterez peut-être améliorer le temps de réponse.</span><span class="sxs-lookup"><span data-stu-id="e5f17-125">After you finish writing your high-performance client, you may want to improve your response time.</span></span> <span data-ttu-id="e5f17-126">Étant donné que l’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) est optimisée pour la vitesse, l’interface n’est pas intrinsèquement threadsafe.</span><span class="sxs-lookup"><span data-stu-id="e5f17-126">Because the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface is optimized for speed, the interface is not intrinsically threadsafe.</span></span> <span data-ttu-id="e5f17-127">Par conséquent, au cours d’une opération d’actualisation, n’accédez pas à l’objet ou à l’énumération actualisable.</span><span class="sxs-lookup"><span data-stu-id="e5f17-127">Therefore, during a refresh operation, do not access the refreshable object or enumeration.</span></span> <span data-ttu-id="e5f17-128">Pour protéger des objets entre les threads pendant les appels de méthode **IWbemObjectAccess** , utilisez les méthodes [**IWbemObjectAccess :: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) et [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) .</span><span class="sxs-lookup"><span data-stu-id="e5f17-128">To protect objects across threads during **IWbemObjectAccess** method calls, use the [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) and [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) methods.</span></span> <span data-ttu-id="e5f17-129">Pour améliorer les performances, synchronisez vos threads afin de ne pas avoir à verrouiller des threads individuels.</span><span class="sxs-lookup"><span data-stu-id="e5f17-129">For improved performance, synchronize your threads so that you do not need to lock individual threads.</span></span> <span data-ttu-id="e5f17-130">La réduction des threads et la synchronisation des groupes d’objets pour les opérations d’actualisation offrent les meilleures performances globales.</span><span class="sxs-lookup"><span data-stu-id="e5f17-130">Reducing threads and synchronizing groups of objects for refresh operations provides the best overall performance.</span></span>

## <a name="adding-enumerators-to-the-wmi-refresher"></a><span data-ttu-id="e5f17-131">Ajout d’énumérateurs à l’actualisateur WMI</span><span class="sxs-lookup"><span data-stu-id="e5f17-131">Adding Enumerators to the WMI Refresher</span></span>

<span data-ttu-id="e5f17-132">Le nombre d’instances et de données de chaque instance est actualisé en ajoutant un énumérateur à l’actualisateur afin que chaque appel à [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) donne une énumération complète.</span><span class="sxs-lookup"><span data-stu-id="e5f17-132">Both the number of instances and data in each instance are refreshed by adding an enumerator to the refresher so that each call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) results in a complete enumeration.</span></span>

<span data-ttu-id="e5f17-133">L’exemple de code C++ suivant requiert les références suivantes et les \# instructions include pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="e5f17-133">The following C++ code example requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="e5f17-134">La procédure suivante montre comment ajouter un énumérateur à un actualisateur.</span><span class="sxs-lookup"><span data-stu-id="e5f17-134">The following procedure shows how to add an enumerator to a refresher.</span></span>

<span data-ttu-id="e5f17-135">**Pour ajouter un énumérateur à un actualisateur**</span><span class="sxs-lookup"><span data-stu-id="e5f17-135">**To add an enumerator to a refresher**</span></span>

1.  <span data-ttu-id="e5f17-136">Appelez la méthode [**IWbemConfigureRefresher :: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) à l’aide du chemin d’accès à l’objet actualisable et de l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="e5f17-136">Call the [**IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) method using the path to the refreshable object and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

    <span data-ttu-id="e5f17-137">L’actualisateur retourne un pointeur vers une interface [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) .</span><span class="sxs-lookup"><span data-stu-id="e5f17-137">The refresher returns a pointer to an [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) interface.</span></span> <span data-ttu-id="e5f17-138">Vous pouvez utiliser l’interface **IWbemHiPerfEnum** pour accéder aux objets de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e5f17-138">You can use the **IWbemHiPerfEnum** interface to access the objects in the enumeration.</span></span>

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

    

2.  <span data-ttu-id="e5f17-139">Créez une boucle qui effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5f17-139">Create a loop that performs the following actions:</span></span>

    -   <span data-ttu-id="e5f17-140">Actualise l’objet à l’aide d’un appel à [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span><span class="sxs-lookup"><span data-stu-id="e5f17-140">Refreshes the object by using a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span></span>
    -   <span data-ttu-id="e5f17-141">Fournit un tableau de pointeurs d’interface [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) à la méthode [**IWbemHiPerfEnum :: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .</span><span class="sxs-lookup"><span data-stu-id="e5f17-141">Provides an array of [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface pointers to the [**IWbemHiPerfEnum::GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) method.</span></span>
    -   <span data-ttu-id="e5f17-142">Accède aux propriétés de l’énumérateur à l’aide des méthodes [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) passées dans [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="e5f17-142">Accesses the properties of the enumerator by using the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) methods passed into [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

        <span data-ttu-id="e5f17-143">Un descripteur de propriété peut être passé à chaque instance [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) pour récupérer la valeur actualisée.</span><span class="sxs-lookup"><span data-stu-id="e5f17-143">A property handle can be passed to each [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instance to retrieve the refreshed value.</span></span> <span data-ttu-id="e5f17-144">Le client doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer les pointeurs **IWbemObjectAccess** retournés par [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="e5f17-144">The client must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the **IWbemObjectAccess** pointers returned by [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

## <a name="example"></a><span data-ttu-id="e5f17-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5f17-145">Example</span></span>

<span data-ttu-id="e5f17-146">L’exemple de code C++ suivant énumère une classe à hautes performances, où le client récupère un handle de propriété à partir du premier objet et réutilise le handle pour le reste de l’opération d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="e5f17-146">The following C++ code example enumerates a high-performance class, where the client retrieves a property handle from the first object, and reuses the handle for the remainder of the refresh operation.</span></span> <span data-ttu-id="e5f17-147">Chaque appel à la méthode [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) met à jour le nombre d’instances et les données d’instance.</span><span class="sxs-lookup"><span data-stu-id="e5f17-147">Each call to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method updates the number of instances and the instance data.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e5f17-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5f17-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5f17-149">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="e5f17-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="e5f17-150">Accès aux données de performances dans le script</span><span class="sxs-lookup"><span data-stu-id="e5f17-150">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="e5f17-151">Actualisation des données WMI dans les scripts</span><span class="sxs-lookup"><span data-stu-id="e5f17-151">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="e5f17-152">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="e5f17-152">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="e5f17-153">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="e5f17-153">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="e5f17-154">Qualificateurs de propriété pour les classes de compteur de performance mises en forme</span><span class="sxs-lookup"><span data-stu-id="e5f17-154">Property Qualifiers for Formatted Performance Counter Classes</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="e5f17-155">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="e5f17-155">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="e5f17-156">**Wmiadap.exe**</span><span class="sxs-lookup"><span data-stu-id="e5f17-156">**Wmiadap.exe**</span></span>](wmiadap.md)
</dt> <dt>

[<span data-ttu-id="e5f17-157">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="e5f17-157">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
