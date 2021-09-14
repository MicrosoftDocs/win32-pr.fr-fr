---
description: Une requête synchrone est une requête qui maintient le contrôle sur le processus de votre application pendant la durée de la requête.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Appel d’une requête synchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010463"
---
# <a name="invoking-a-synchronous-query"></a>Appel d’une requête synchrone

Une requête synchrone est une requête qui maintient le contrôle sur le processus de votre application pendant la durée de la requête. Une requête synchrone requiert un appel d’interface unique et est donc plus simple qu’un appel asynchrone. Toutefois, une requête synchrone a le potentiel de verrouiller votre application pour les requêtes ou requêtes volumineuses sur un réseau.

La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de PowerShell.

**Pour émettre une requête de données synchrones dans PowerShell**

-   Décrivez votre requête à WMI à l’aide de l’applet de commande WMI [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) et du paramètre *-query* . L’applet de commande retourne soit un objet unique, soit une collection d’objets, selon le nombre d’objets qui correspondent à la requête.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de C#.

**Pour émettre une requête de données synchrone en C# (Microsoft. Management. infrastructure)**

1.  Décrivez votre requête à WMI à l’aide de CimSession. QueryInstances. Cette méthode retourne une collection d’objets CimInstance.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  Utilisez les techniques de collection de langage C# standard pour accéder à chaque objet retourné.

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de C#.

**Pour émettre une requête de données synchrone en C# (System. Management)**

1.  Créez la requête avec un objet [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) et récupérez les informations à l’aide d’un appel à [ManagementObjectSearcher. obtenir](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).

    Cette méthode retourne un objet [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) .

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  Utilisez les techniques de collection de langage C# standard pour accéder à chaque objet retourné.

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de VBScript.

**Pour émettre une requête de données synchrones dans VBScript**

1.  Décrivez votre requête à WMI à l’aide de [**SWbemServices. ExecQuery**](swbemservices-execquery.md). Cette méthode retourne une [**SWbemObjectSet**](swbemobjectset.md).

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  Utilisez les techniques de [collection](accessing-a-collection.md) de langage de script standard pour accéder à chaque objet retourné.

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

La procédure suivante décrit comment émettre une requête de données synchrone à l’aide de C++.

**Pour émettre une requête synchrone en C++**

1.  Décrivez votre requête à WMI à l’aide d’un appel à [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    La méthode [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) prend une chaîne de recherche WQL comme paramètre qui décrit votre requête. WMI exécute la requête et retourne un pointeur d’interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . À l’aide de l’interface **IEnumWbemClassObject** , vous pouvez accéder aux classes ou aux instances qui composent le jeu de résultats.

2.  Une fois que vous avez reçu votre requête, vous pouvez énumérer votre requête avec un appel à [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next). Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md).

    L’exemple de code suivant requiert les références suivantes et les \# instructions include pour compiler correctement.

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    L’exemple de code suivant décrit comment interroger les objets qui représentent les utilisateurs et les groupes dans WMI.

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

    

 

 
