---
description: La méthode la plus courante de mise à jour d’une instance de classe WMI consiste à mettre à jour l’intégralité de l’instance à la fois.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Mise à jour d’une instance entière
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cac29805eeff1f8c659c0bee6832eb65e9e6b5bdee8cd15bd0a052247a70e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995538"
---
# <a name="updating-an-entire-instance"></a>Mise à jour d’une instance entière

La méthode la plus courante de mise à jour d’une instance de classe WMI consiste à mettre à jour l’intégralité de l’instance à la fois. En mettant à jour une instance entière, WMI n’a pas besoin d’analyser l’instance dans des propriétés individuelles et de les envoyer à votre application. Au lieu de cela, WMI peut simplement vous envoyer l’instance entière. Lorsque vous avez terminé, WMI peut ensuite copier l’intégralité de votre instance modifiée sur l’instance d’origine.

La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de PowerShell.

**Pour modifier ou mettre à jour une instance à l’aide de PowerShell**

1.  Récupérez une copie locale de l’objet à l’aide d’un appel à la fonction « obtenir-WmiObject ».

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Si nécessaire, affichez les propriétés de l’objet avec un appel à la collection de propriétés.

    Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Apportez des modifications aux propriétés de l’objet local.

    Cela modifie uniquement la copie locale. Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Replacez l’objet dans le référentiel WMI à l’aide d’un appel à la méthode put.

    ```PowerShell
    $mySettings.Put()
    ```

    

La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de C#.

**Pour modifier ou mettre à jour une instance à l’aide de C# (Microsoft. Management. infrastructure)**

1.  Récupérez une copie locale de l’objet à l’aide d’un appel à [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), comme décrit dans [récupération d’une instance WMI](retrieving-an-instance.md).

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  Si nécessaire, affichez les propriétés de l’objet avec un appel à la collection de propriétés.

    Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Apportez des modifications aux propriétés de l’objet local.

    Cela modifie uniquement la copie locale. Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Replacez l’objet dans le référentiel WMI à l’aide d’un appel à [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de PowerShell.

> [!Note]  
> **System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.

 

**Pour modifier ou mettre à jour une instance à l’aide de C# (Microsoft. Management)**

1.  Récupérez une copie locale de l’objet à l’aide d’un appel à [ManagementObject. obtenir](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Si nécessaire, affichez les propriétés de l’objet avec un appel à la collection de propriétés.

    Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Apportez des modifications aux propriétés de l’objet local.

    Cela modifie uniquement la copie locale. Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Replacez l’objet dans le référentiel WMI à l’aide d’un appel à la méthode [ManagementObject. put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) ou.

    ```CSharp
    myDisk.Put();
    ```

    

La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de VBScript.

**Pour modifier ou mettre à jour une instance à l’aide de VBScript**

1.  Récupérez une copie locale de l’objet à l’aide d’un appel à **GetObject**.
2.  Si nécessaire, affichez les propriétés de l’objet à l’aide d’un appel à la méthode [**Properties \_**](swbemobject-properties-.md) .

    Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.

3.  Apportez des modifications aux propriétés de l’objet avec un appel à la méthode [**SWbemProperty. Value**](swbemproperty-value.md) .

    La méthode **value** modifie uniquement la copie locale. Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.

4.  Replacez l’objet dans le référentiel WMI avec un appel aux méthodes [**SWbemObject. put \_**](swbemobject-put-.md) ou [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md) .

Comme le nom l’indique [**, \_ Mettez**](swbemobject-put-.md) les mises à jour de façon synchrone pendant que [**PutAsync \_**](swbemobject-putasync-.md) est mis à jour de façon asynchrone. L’une ou l’autre méthode copie l’instance d’origine avec votre instance modifiée. Toutefois, pour tirer parti du traitement asynchrone, vous devez créer un objet [**SWbemSink**](swbemsink.md) . Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

La procédure suivante décrit comment modifier ou mettre à jour une instance de à l’aide de C++.

**Pour modifier ou mettre à jour une instance à l’aide de C++**

1.  Récupérez une copie locale de l’instance avec un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).
2.  Si nécessaire, affichez les propriétés de l’objet à l’aide d’un appel à [**IWbemClassObject :: obtenir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).

    Bien que cela ne soit pas obligatoire, vous souhaiterez peut-être connaître la valeur de la propriété avant de la modifier.

3.  Apportez les modifications nécessaires à la copie à l’aide d’un appel à [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    La méthode **put** modifie uniquement la copie locale. Pour enregistrer les modifications apportées à WMI, vous devez replacer la copie entière dans le référentiel WMI.

4.  Replacez votre copie dans le référentiel WMI avec un appel aux méthodes [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    Comme le nom l’indique, **PutInstance** est mis à jour de façon synchrone pendant que [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) est mis à jour de façon asynchrone. L’une ou l’autre méthode copie l’instance d’origine avec votre instance modifiée. Toutefois, pour tirer parti du traitement asynchrone, vous devez implémenter l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    Vous devez savoir qu’une opération de mise à jour sur une instance appartenant à une hiérarchie de classes peut échouer en raison d’une erreur impliquant une autre classe dans la hiérarchie. WMI appelle la méthode [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) de chacun des fournisseurs responsables des classes dont dérive la classe propriétaire de l’instance d’origine. Si l’un de ces fournisseurs échoue, la demande de mise à jour d’origine échoue. Pour plus d’informations, consultez la section Notes de [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

Pour plus d’informations, consultez [appel d’une méthode de fournisseur](calling-a-provider-method.md).

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser le mode semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

 

 
