---
description: La récupération d’une instance est l’une des procédures de récupération les plus courantes que vous êtes susceptible d’effectuer dans WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Récupération d’une instance WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042762"
---
# <a name="retrieving-a-wmi-instance"></a>Récupération d’une instance WMI

La récupération d’une instance est l’une des procédures de récupération les plus courantes que vous êtes susceptible d’effectuer dans WMI. Vous pouvez récupérer une instance existante ou créer une nouvelle instance sans nom. Le chemin d’accès WMI de l’instance existante est un paramètre obligatoire. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

> [!Note]  
> Lorsque vous fournissez une instance, un fournisseur peut ne pas être en mesure de fournir une valeur pour certaines propriétés. Sauf indication contraire dans la description de la propriété, vous ne pouvez pas déduire une signification à partir d’une valeur vide. Cela ne doit pas être confondu avec une chaîne qui a une valeur **null** . Dans ce cas, la valeur est remplie. Il est vide, mais a une valeur : **null**.

 

Récupérez une copie locale de l’instance avec un appel à l’applet de commande PowerShell [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .

**Pour récupérer une instance d’une classe WMI à l’aide de PowerShell**

-   Vous pouvez récupérer des instances spécifiques à l’aide des paramètres *-Class* et *-Filter* .

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

Vous pouvez récupérer une instance WMI en utilisant C# en créant un objet de recherche à l’aide de [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), puis en le remplissant avec les valeurs de clé pertinentes, puis en recherchant cet objet avec un appel de [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

**Pour récupérer une instance d’une classe WMI à l’aide de C# (Microsoft. Management. infrastructure)**

1.  À l’aide de l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , créez un nouvel objet [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) avec le nom de classe et l’espace de noms appropriés.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  Créez un [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) qui contient le nom et la valeur de la propriété de clé de l’instance que vous souhaitez rechercher, puis ajoutez cette propriété à votre objet de classe.

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  Récupérez l’objet de WMI avec un appel [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

Vous pouvez récupérer une instance de classe WMI spécifique ou une collection d’instances de classe WMI à l’aide des classes de l’espace de noms [System. Management](/dotnet/api/system.management) .

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

**Pour récupérer une instance d’une classe WMI à l’aide de C# (System. Management)**

1.  Récupérez une copie locale d’une instance spécifique en créant un nouveau [ManagementObject](/dotnet/api/system.management.managementobject), avec le nom et la valeur d’instance spécifique transmis par le biais du paramètre *ManagementPath* . Vous pouvez ensuite récupérer les données d’instance en appelant explicitement [ManagementObject. obtenir](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  Vous pouvez également récupérer toutes les instances d’une classe WMI en les recherchant avec un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), puis en énumérant les [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)retournés.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    Vous pouvez appeler la méthode d' **extraction** de manière implicite en accédant à l’instance. Pour plus d’informations, consultez [récupération d’une partie d’une instance WMI](retrieving-part-of-an-instance.md).

Récupérez une copie locale de l’instance avec un appel à la méthode VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .

**Pour récupérer une instance d’une classe WMI à l’aide de VBScript**

-   Appelez [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) avec le chemin d’accès de l’objet de l’instance, comme indiqué dans l’exemple suivant.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    Pour récupérer une instance spécifique, vous devez donner un nom dans le chemin d’accès à l’objet.

En C++, appelez [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Pour récupérer une instance d’une classe WMI à l’aide de C++**

-   Récupérez une copie locale de l’instance avec un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Le chemin d’accès WMI de l’objet doit être inclus.

    Comme son nom l’indique, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) récupère l’instance de façon asynchrone, tandis que [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) récupère l’instance de façon synchrone. Si vous souhaitez utiliser la récupération asynchrone, vous devez implémenter l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple VBScript à utiliser comme modèle pour récupérer des informations de classe et d’instance, consultez l’exemple de [script de modèle WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) sur la Galerie technet. Cet exemple particulier utilise GetObject pour récupérer le service WMI.

 

 
