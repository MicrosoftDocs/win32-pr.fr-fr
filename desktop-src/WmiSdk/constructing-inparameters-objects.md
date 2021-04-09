---
description: Un objet Parameters contient la liste de paramètres pour appeler des méthodes de fournisseur lors de l’utilisation d’un type ExecMethod d’appel.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Construction d’objets inparamètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864034"
---
# <a name="constructing-inparameters-objects"></a>Construction d’objets inparamètres

Un objet [**Parameters**](swbemmethod-inparameters.md) contient la liste de paramètres pour appeler des méthodes de fournisseur lors de l’utilisation d’un type **ExecMethod** d’appel. Les méthodes [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)et [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requièrent tous un objet **Parameters** .

La procédure suivante décrit comment construire un objet [**inparamètres**](swbemmethod-inparameters.md) .

**Pour construire le paramètre *objwbemInParams***

1.  Connectez-vous à WMI.
2.  Obtenez la définition de la classe WMI qui définit la méthode que vous souhaitez exécuter.
3.  Obtenez un objet [**inparamètres**](swbemmethod-inparameters.md) spécifique à la méthode de classe WMI que vous souhaitez exécuter.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Définissez les propriétés de l’instance sur les valeurs appropriées. Veillez à attribuer des valeurs aux propriétés de clé dans la classe WMI qui contient la méthode que vous souhaitez exécuter.

    Par exemple, si vous souhaitez définir un paramètre d’entrée nommé myinputparam sur la valeur « ABC » dans une instance d' [**inparamètres**](swbemmethod-inparameters.md) appelée « inst », le code doit ressembler à ce qui suit.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Exécutez la méthode et obtenez l’état de retour de la méthode que vous exécutez.

L’exemple de code suivant illustre la configuration de l’objet [**inparamètres**](swbemmethod-inparameters.md) pour créer un nouvel objet WMI qui représente un partage. Pour plus d’informations sur l’objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) , consultez analyse des objets de [paramètres de paramètres](parsing-outparameters-objects.md). Cet exemple retourne une valeur de retour réussie (0) s’il existe un dossier nommé « Share » à l’emplacement « C:/share ». Cet exemple permet de partager ce dossier avec d’autres utilisateurs.


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



