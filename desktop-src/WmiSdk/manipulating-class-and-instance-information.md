---
description: WMI fournit diverses techniques pour récupérer et manipuler les informations sur les classes et les instances WMI, à l’aide de Microsoft PowerShell, Visual&\# 160 ; Basic Scripting Edition (VBScript) et C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Manipulation des informations relatives aux classes et aux instances
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529404"
---
# <a name="manipulating-class-and-instance-information"></a>Manipulation des informations relatives aux classes et aux instances

WMI fournit diverses techniques pour récupérer et manipuler des informations sur les classes et les instances WMI, à l’aide de Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) et C++.

Le tableau suivant répertorie les rubriques qui traitent des techniques de récupération et de manipulation des informations d’instance et de classe WMI.



| Rubrique                                                                                  | Description                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Récupération des données de classe ou d’instance WMI](retrieving-class-or-instance-data.md)         | Récupérez et définissez les données depuis et vers le référentiel d’informations WMI.                                                                                                                 |
| [Modification d’une propriété d’instance](modifying-an-instance-property.md)                   | Modifiez les informations dans l’instance une fois qu’elle a été récupérée.                                                                                                                     |
| [Modification de l’héritage d’une instance](changing-the-inheritance-of-an-instance.md) | Modifiez la classe parente d’une instance.                                                                                                                                           |
| [Modification d’une méthode](modifying-a-method.md)                                           | Modifiez les paramètres d’une instance de.                                                                                                                                             |
| [Énumération de WMI](enumerating-wmi.md)                                                 | Énumérer les objets WMI.                                                                                                                                                            |
| [Interrogation de WMI](querying-wmi.md)                                                       | Interroger les objets WMI.                                                                                                                                                                |
| [Appel d’une méthode](calling-a-method.md)                                               | Utilisez les méthodes associées créées par Microsoft ou d’autres développeurs tiers pour améliorer la manipulation des objets WMI, ou affectez directement l’objet représenté par l’objet WMI. |
| [Accès à une collection](accessing-a-collection.md)                                   | Énumérez les collections dans le script.                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>Manipulation de données à l’aide de VBScript

Vous pouvez utiliser l’accès direct pour accéder aux propriétés WMI d’une classe ou d’une instance WMI directement sur un [**SWbemObject**](swbemobject.md), plutôt qu’à l’aide de la [collection](accessing-a-collection.md) de propriétés de cet objet. Vous pouvez également exécuter des méthodes sur cet objet dans le style natif du langage de programmation plutôt que d’utiliser le [**SWbemServices.Exeappel cMethod**](swbemservices-execmethod.md) . Par exemple, la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) dans le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) avait trois paramètres dans Windows 2000, mais a quatre paramètres dans Windows Server 2003.

À l’aide de l’accès direct, vous pouvez traiter les propriétés et les méthodes WMI comme s’il s’agissait de propriétés et de méthodes Automation de [**SWbemObject**](swbemobject.md).

L’exemple suivant montre comment vous pouvez accéder à une propriété.


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



L’exemple suivant montre comment vous pouvez accéder à une propriété lorsque vous avez un accès direct.


```VB
VolumeName = MyDisk.VolumeName
```



Le chaînage d’objets est également acceptable.

L’exemple suivant montre comment accéder à une propriété d’un objet incorporé dans un autre objet.


```VB
value = MyComputer.MyDisk.VolumeName
```



L’exemple suivant montre comment accéder à une propriété à l’aide d’une notation d’indice de tableau.


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



L’exemple de code VBScript suivant montre comment générer une instance des paramètres d’entrée dans la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la classe [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) en tant que [**SWbemObject**](swbemobject.md), remplir les propriétés d’entrée, puis exécuter la méthode **Create** à l’aide de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

La propriété [**SWbemObject. \_ Methods**](swbemobject-methods-.md) retourne une collection [**SWbemMethodSet**](swbemmethodset.md) des méthodes de [**\_ traitement Win32**](/windows/desktop/CIMWin32Prov/win32-process) . Les membres de la méthode définie sont des objets SWbemMethod et [**SWbemMethod.**](swbemmethod-inparameters.md) [**ins**](swbemmethod.md) retourne les paramètres d’entrée de la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Le paramètre d’entrée de la *ligne* de commande requis est défini sur « calc.exe ». La méthode est ensuite exécutée par [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), ce qui entraîne le lancement d’un processus de calc.exe.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



L’exemple de code suivant montre comment effectuer l’opération précédente à l’aide de l’accès direct.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



Pour plus d’informations, consultez [appel d’une méthode de fournisseur](calling-a-provider-method.md) et [écriture de scripts avec SWbemObject](scripting-with-swbemobject.md).

 

 
