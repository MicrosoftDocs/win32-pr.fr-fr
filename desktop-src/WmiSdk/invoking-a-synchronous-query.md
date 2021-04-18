---
description: Une requête synchrone est une requête qui maintient le contrôle sur le processus de votre application pendant la durée de la requête.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Appel d’une requête synchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536210"
---
# <a name="invoking-a-synchronous-query"></a><span data-ttu-id="e6af1-103">Appel d’une requête synchrone</span><span class="sxs-lookup"><span data-stu-id="e6af1-103">Invoking a Synchronous Query</span></span>

<span data-ttu-id="e6af1-104">Une requête synchrone est une requête qui maintient le contrôle sur le processus de votre application pendant la durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="e6af1-104">A synchronous query is a query that maintains control over the process of your application for the duration of the query.</span></span> <span data-ttu-id="e6af1-105">Une requête synchrone requiert un appel d’interface unique et est donc plus simple qu’un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e6af1-105">A synchronous query requires a single interface call, and is therefore more simple than an asynchronous call.</span></span> <span data-ttu-id="e6af1-106">Toutefois, une requête synchrone a le potentiel de verrouiller votre application pour les requêtes ou requêtes volumineuses sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="e6af1-106">However, a synchronous query has the potential of locking up your application for large queries or queries over a network.</span></span>

<span data-ttu-id="e6af1-107">La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e6af1-107">The following procedure describes how to issue a synchronous data query using PowerShell.</span></span>

<span data-ttu-id="e6af1-108">**Pour émettre une requête de données synchrones dans PowerShell**</span><span class="sxs-lookup"><span data-stu-id="e6af1-108">**To issue a synchronous data query in PowerShell**</span></span>

-   <span data-ttu-id="e6af1-109">Décrivez votre requête à WMI à l’aide de l’applet de commande WMI [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) et du paramètre *-query* .</span><span class="sxs-lookup"><span data-stu-id="e6af1-109">Describe your query to WMI using the WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet and the *-query* parameter.</span></span> <span data-ttu-id="e6af1-110">L’applet de commande retourne soit un objet unique, soit une collection d’objets, selon le nombre d’objets qui correspondent à la requête.</span><span class="sxs-lookup"><span data-stu-id="e6af1-110">The cmdlet returns either a single object, or a collection of objects, depending on how many objects fit the query.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="e6af1-111">La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de C#.</span><span class="sxs-lookup"><span data-stu-id="e6af1-111">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="e6af1-112">**Pour émettre une requête de données synchrone en C# (Microsoft. Management. infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="e6af1-112">**To issue a synchronous data query in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="e6af1-113">Décrivez votre requête à WMI à l’aide de CimSession. QueryInstances.</span><span class="sxs-lookup"><span data-stu-id="e6af1-113">Describe your query to WMI using CimSession.QueryInstances.</span></span> <span data-ttu-id="e6af1-114">Cette méthode retourne une collection d’objets CimInstance.</span><span class="sxs-lookup"><span data-stu-id="e6af1-114">This method returns a collection of CimInstance objects.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  <span data-ttu-id="e6af1-115">Utilisez les techniques de collection de langage C# standard pour accéder à chaque objet retourné.</span><span class="sxs-lookup"><span data-stu-id="e6af1-115">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

<span data-ttu-id="e6af1-116">La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de C#.</span><span class="sxs-lookup"><span data-stu-id="e6af1-116">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="e6af1-117">**Pour émettre une requête de données synchrone en C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="e6af1-117">**To issue a synchronous data query in C# (System.Management)**</span></span>

1.  <span data-ttu-id="e6af1-118">Créez la requête avec un objet [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) et récupérez les informations à l’aide d’un appel à [ManagementObjectSearcher. obtenir](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span><span class="sxs-lookup"><span data-stu-id="e6af1-118">Create the query with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) object, and retrieve the information with a call to [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span></span>

    <span data-ttu-id="e6af1-119">Cette méthode retourne un objet [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) .</span><span class="sxs-lookup"><span data-stu-id="e6af1-119">This method returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  <span data-ttu-id="e6af1-120">Utilisez les techniques de collection de langage C# standard pour accéder à chaque objet retourné.</span><span class="sxs-lookup"><span data-stu-id="e6af1-120">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

<span data-ttu-id="e6af1-121">La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="e6af1-121">The following procedure describes how to issue a synchronous data query using VBScript.</span></span>

<span data-ttu-id="e6af1-122">**Pour émettre une requête de données synchrones dans VBScript**</span><span class="sxs-lookup"><span data-stu-id="e6af1-122">**To issue a synchronous data query in VBScript**</span></span>

1.  <span data-ttu-id="e6af1-123">Décrivez votre requête à WMI à l’aide de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="e6af1-123">Describe your query to WMI using [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="e6af1-124">Cette méthode retourne une [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="e6af1-124">This method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  <span data-ttu-id="e6af1-125">Utilisez les techniques de [collection](accessing-a-collection.md) de langage de script standard pour accéder à chaque objet retourné.</span><span class="sxs-lookup"><span data-stu-id="e6af1-125">Use standard scripting language [collection](accessing-a-collection.md) techniques to access each returned object.</span></span>

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

<span data-ttu-id="e6af1-126">La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="e6af1-126">The following procedure describes how to issue a synchronous data query using C++.</span></span>

<span data-ttu-id="e6af1-127">**Pour émettre une requête synchrone en C++**</span><span class="sxs-lookup"><span data-stu-id="e6af1-127">**To issue a synchronous query in C++**</span></span>

1.  <span data-ttu-id="e6af1-128">Décrivez votre requête à WMI à l’aide d’un appel à [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="e6af1-128">Describe your query to WMI through a call to [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="e6af1-129">La méthode [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) prend une chaîne de recherche WQL comme paramètre qui décrit votre requête.</span><span class="sxs-lookup"><span data-stu-id="e6af1-129">The [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) method takes a WQL search string as a parameter that describes your query.</span></span> <span data-ttu-id="e6af1-130">WMI exécute la requête et retourne un pointeur d’interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="e6af1-130">WMI performs the query and returns an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="e6af1-131">À l’aide de l’interface **IEnumWbemClassObject** , vous pouvez accéder aux classes ou aux instances qui composent le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="e6af1-131">Through the **IEnumWbemClassObject** interface, you can access the classes or instances that make up the result set.</span></span>

2.  <span data-ttu-id="e6af1-132">Une fois que vous avez reçu votre requête, vous pouvez énumérer votre requête avec un appel à [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span><span class="sxs-lookup"><span data-stu-id="e6af1-132">After you receive your query, you can enumerate your query with a call to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span></span> <span data-ttu-id="e6af1-133">Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="e6af1-133">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

    <span data-ttu-id="e6af1-134">L’exemple de code suivant requiert les références suivantes et les \# instructions include pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="e6af1-134">The following code example requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    <span data-ttu-id="e6af1-135">L’exemple de code suivant décrit comment interroger les objets qui représentent les utilisateurs et les groupes dans WMI.</span><span class="sxs-lookup"><span data-stu-id="e6af1-135">The following code example describes how to query for the objects that represent the users and groups in WMI.</span></span>

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
