---
description: Un qualificateur est une balise qui fournit plus d’informations sur un objet, une méthode ou une propriété WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Accès à un qualificateur WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45601de8e7b3f8ef7054742812c24f9a81dcedf5417f7b7ba501f2471adedc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820617"
---
# <a name="accessing-a-wmi-qualifier"></a>Accès à un qualificateur WMI

Un qualificateur est une balise qui fournit plus d’informations sur un objet, une méthode ou une propriété WMI. Dans certains cas, vous devrez peut-être accéder aux données stockées dans un qualificateur. Par exemple, une tâche courante consiste à déterminer si un fournisseur implémente une méthode en tentant de récupérer le qualificateur **implémenté** pour cette méthode. Pour plus d’informations, consultez [qualificateurs WMI](wmi-qualifiers.md) et [Ajout d’un qualificateur](adding-a-qualifier.md).

Vous pouvez récupérer les qualificateurs d’un objet WMI dans PowerShell en extrayant d’abord l’objet, puis en examinant les qualificateurs comme vous le feriez pour toute autre propriété.

**Pour récupérer un qualificateur à l’aide de PowerShell**

-   Récupérez l’objet dont vous souhaitez afficher les qualificateurs à l’aide de la propriété [obtenir-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), puis accédez aux qualificateurs via la propriété **qualificateurs** :

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).

Vous pouvez récupérer les qualificateurs sur une instance WMI en C# en extrayant d’abord l’objet, puis en examinant les qualificateurs en tant que collection.

**Pour récupérer un qualificateur à l’aide de C# (Microsoft.SysTEM. Gestion**

1.  Récupérez la classe dont vous souhaitez afficher les qualificateurs en créant un objet CimInstance à l’aide du nom de classe et de l’espace de noms spécifiés.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).

2.  Vous pouvez récupérer les qualificateurs de classe à partir de [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), les qualificateurs de propriété de [CimInstance. CimClass. CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))et les qualificateurs de méthode de [CimInstance. CimClass. CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).

Vous pouvez récupérer les qualificateurs sur un objet WMI en C# en extrayant d’abord l’objet, puis en examinant les qualificateurs en tant que collection.

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

**Pour récupérer un qualificateur à l’aide de C# (System. Management)**

1.  Récupérez l’objet dont vous souhaitez afficher les qualificateurs à l’aide de [ManagementObject](/dotnet/api/system.management.managementobject).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).

2.  Placez les qualificateurs dans un [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)et Énumérez les valeurs [QualifierData](/dotnet/api/system.management.qualifierdata) .

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).

La procédure suivante décrit comment récupérer un qualificateur à l’aide de VBScript.

**Pour récupérer un qualificateur à l’aide de VBScript**

1.  Récupérez l’objet dont vous souhaitez afficher les qualificateurs, comme illustré dans l’exemple suivant :

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    La méthode la plus courante pour récupérer un objet consiste à utiliser la méthode [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) . Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).

2.  Accédez aux qualificateurs de l’objet via la propriété [**SWbemObject. Qualifiers \_**](swbemobject-qualifiers-.md) , comme indiqué dans l’exemple suivant :

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

L’exemple de code suivant décrit comment accéder à tous les qualificateurs d’un objet [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) .


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



La procédure suivante décrit comment récupérer un qualificateur à l’aide de C++.

**Pour récupérer un qualificateur à l’aide de C++**

1.  Récupérez l’objet dont vous souhaitez afficher les qualificateurs.

    La méthode la plus courante pour récupérer un objet consiste à utiliser un appel à [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou à [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Pour plus d’informations, consultez [récupération de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).

2.  Récupérez le jeu de qualificateurs pour une propriété donnée avec un appel à [**IWbemClassObject :: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) ou [**IWbemClassObject :: GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) méthodes.

3.  Accédez aux qualificateurs de l’objet par le biais de l’interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) retournée.

## <a name="examples"></a>Exemples

Pour plus d’informations sur la récupération des qualificateurs, consultez l’exemple de code PowerShell [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) dans la Galerie technet.

 

 
