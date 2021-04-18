---
description: L’énumération est l’action consistant à passer par un ensemble d’objets et éventuellement à modifier chaque objet au fur et à mesure.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Énumération de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519038"
---
# <a name="enumerating-wmi"></a>Énumération de WMI

L’énumération est l’action consistant à passer par un ensemble d’objets et éventuellement à modifier chaque objet au fur et à mesure. Par exemple, vous pouvez énumérer un ensemble d’objets [**\_ DiskDrive Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) pour rechercher un numéro de série particulier. Notez que même si vous pouvez énumérer n’importe quel objet, WMI retourne uniquement les objets pour lesquels vous disposez d’un accès de sécurité.

Les énumérations de jeux de données volumineux peuvent nécessiter une grande quantité de ressources et nuire aux performances. Pour plus d’informations, consultez amélioration des performances de l' [énumération](improving-enumeration-performance.md). Vous pouvez également demander des données avec une requête plus spécifique. Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).

Les sections suivantes sont présentées dans cette rubrique :

-   [Énumération de WMI à l’aide de PowerShell](#enumerating-wmi-using-powershell)
-   [Énumération de WMI à l’aide de C# (Microsoft. Management. infrastructure)](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [Énumération de WMI à l’aide de C# (System. Management)](#enumerating-wmi-using-c-systemmanagement)
-   [Énumération de WMI à l’aide de VBScript](#enumerating-wmi-using-vbscript)
-   [Énumération de WMI à l’aide de C++](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a>Énumération de WMI à l’aide de PowerShell

Si vous ne connaissez pas le chemin d’accès de l’objet pour une instance spécifique, ou si vous souhaitez récupérer toutes les instances d’une classe spécifique [, utilisez la](https://technet.microsoft.com/library/dd315379.aspx)fonction de mise à niveau de l’objet avec le nom de la classe dans le paramètre *-Class* . Si vous souhaitez utiliser une requête, vous pouvez utiliser le paramètre *-query* .

La procédure suivante décrit comment énumérer les instances d’une classe à l’aide de PowerShell.

**Pour énumérer les instances d’une classe à l’aide de PowerShell**

1.  Énumérez les instances avec un appel à l’applet de commande [« obtenir-WmiObject »](https://technet.microsoft.com/library/dd315379.aspx) .

    L’accès [en fonction](https://technet.microsoft.com/library/dd315379.aspx) de la méthode obtient une collection d’un ou de plusieurs objets WMI par le biais desquels vous pouvez effectuer l’énumération. Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).

    Si vous souhaitez récupérer une instance de classe WMI dans un autre espace de noms ou sur un autre ordinateur, spécifiez l’ordinateur et l’espace de noms respectivement dans les paramètres *-Computer* et *-namespace* . Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md). Cela ne fonctionne que si vous disposez des privilèges d’accès appropriés. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md) et [exécution des opérations privilégiées](executing-privileged-operations.md).

2.  Récupérez les instances individuelles que vous souhaitez à l’aide des membres de la collection.

L’exemple de code suivant récupère une collection PowerShell, puis affiche la propriété Size pour toutes les instances de lecteurs logiques sur l’ordinateur local.


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a>Énumération de WMI à l’aide de C# (Microsoft. Management. infrastructure)

1.  Ajoutez une référence à l’assembly de référence **Microsoft. Management. infrastructure** . (Cet assembly est fourni avec le [Kit de développement logiciel (SDK) Windows pour Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)
2.  Ajoutez une instruction **using** pour l’espace de noms **Microsoft. Management. infrastructure** .

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  Instanciez un objet [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) . L’extrait de code suivant utilise la valeur standard « localhost » pour la méthode [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  Appelez la méthode [**CimSession. QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) en passant l’espace de noms CIM souhaité et WQL à utiliser. L’extrait de code suivant retourne deux instances représentant deux processus Windows standard où la propriété handle (représentant un ID de processus, ou PID) a la valeur 0 ou 4.

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  Parcourez les objets [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) retournés.

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

L’exemple de code suivant énumère toutes les instances de la classe [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) (qui représentent les processus actifs) sur l’ordinateur local et imprime le nom de chaque processus.

> [!Note]  
> Dans une application réelle, vous devez définir comme paramètres le nom de l’ordinateur (« localhost ») et l’espace de noms CIM (« root \\ cimv2 »). À des fins de simplicité, elles ont été codées en dur dans cet exemple.

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a>Énumération de WMI à l’aide de C# (System. Management)

Si vous ne connaissez pas le chemin d’accès de l’objet pour une instance spécifique, ou si vous souhaitez récupérer toutes les instances d’une classe spécifique, utilisez l’objet [ManagementClass](/dotnet/api/system.management.managementclass) pour récupérer un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) qui contient toutes les instances d’une classe donnée dans l’espace de noms WMI. Vous pouvez également interroger WMI via un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) pour obtenir le même jeu d’objets.

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

La procédure suivante décrit comment énumérer les instances d’une classe à l’aide de C#.

**Pour énumérer les instances d’une classe à l’aide de C #**

1.  Énumérez les instances avec un appel à [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).

    La méthode [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) retourne une collection ou un ensemble d’objets par le biais desquels vous pouvez effectuer l’énumération. Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md). La collection retournée est en fait un objet [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) , de sorte que toutes les méthodes de cet objet peuvent être appelées.

    Si vous souhaitez récupérer une instance de classe WMI dans un autre espace de noms ou sur un autre ordinateur, spécifiez l’ordinateur et l’espace de noms dans le paramètre *path* . Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md). Cela ne fonctionne que si vous disposez des privilèges d’accès appropriés. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md) et [exécution des opérations privilégiées](executing-privileged-operations.md).

2.  Récupérez les instances individuelles que vous souhaitez à l’aide des membres de la collection.

L’exemple de code suivant récupère une collection C#, puis affiche la propriété Size pour toutes les instances de lecteurs logiques sur l’ordinateur local.


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a>Énumération de WMI à l’aide de VBScript

Si vous ne connaissez pas le chemin d’accès de l’objet pour une instance spécifique, ou si vous souhaitez récupérer toutes les instances d’une classe spécifique, utilisez la méthode [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) pour retourner une énumération [**SWbemObjectSet**](swbemobjectset.md) de toutes les instances d’une classe. Vous pouvez également interroger WMI via [**SWbemServices.ExecQuery**](swbemservices-execquery.md) pour obtenir le même jeu d’objets.

La procédure suivante décrit comment énumérer les instances d’une classe à l’aide de VBScript.

**Pour énumérer les instances d’une classe à l’aide de VBScript**

1.  Énumérez les instances avec un appel à la méthode [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) .

    La méthode [**InstancesOf**](swbemservices-instancesof.md) retourne une collection ou un ensemble d’objets par le biais desquels vous pouvez effectuer l’énumération. Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md). La collection retournée est en fait un objet [**SWbemObjectSet**](swbemobjectset.md) , de sorte que toutes les méthodes de cet objet peuvent être appelées.

    Si vous souhaitez récupérer une instance de classe WMI dans un autre espace de noms ou sur un autre ordinateur, spécifiez l’ordinateur et l’espace de noms dans le moniker. Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md). Cela ne fonctionne que si vous disposez des privilèges d’accès appropriés. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md) et [exécution des opérations privilégiées](executing-privileged-operations.md).

2.  Récupérez toutes les instances individuelles que vous souhaitez à l’aide des méthodes regroupements.

L’exemple de code suivant récupère un objet [**SWbemServices**](swbemservices.md) , puis exécute la méthode [**InstancesOf**](swbemservices-instancesof.md) pour afficher la propriété Size pour toutes les instances de lecteurs logiques sur l’ordinateur local.


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a>Énumération de WMI à l’aide de C++

Outre l’exécution de l’énumération de base, vous pouvez définir plusieurs indicateurs et propriétés afin d’augmenter les performances de votre énumération. Pour plus d’informations, consultez amélioration des performances de l' [énumération](improving-enumeration-performance.md).

**Pour énumérer un jeu d’objets dans WMI**

1.  Créez une interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) décrivant l’ensemble d’objets que vous souhaitez énumérer.

    Un objet [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contient une liste décrivant un ensemble d’objets WMI. Vous pouvez utiliser les méthodes **IEnumWbemClassObject** pour énumérer les transferts, ignorer les objets, commencer au début et copier l’énumérateur. Le tableau suivant répertorie les méthodes utilisées pour créer des énumérateurs pour différents types d’objets WMI.

    

    <table>
    <thead>
    <tr class="header">
    <th>Object</th>
    <th>Méthode</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Classe</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices :: CreateClassEnum</strong></a><br />
[<strong>IWbemServices :: CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Instance</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices :: CreateInstanceEnum</strong></a><br />
[<strong>IWbemServices :: CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)<br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td>Résultat de la requête</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices :: ExecQuery</strong></a><br />
[<strong>IWbemServices :: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Notification d'événement</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices :: ExecNotificationQuery</strong></a><br />
[<strong>IWbemServices :: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Parcourez l’énumération retournée à l’aide de plusieurs appels à [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject :: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

 

 
