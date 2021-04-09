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
# <a name="constructing-inparameters-objects"></a><span data-ttu-id="41969-103">Construction d’objets inparamètres</span><span class="sxs-lookup"><span data-stu-id="41969-103">Constructing InParameters Objects</span></span>

<span data-ttu-id="41969-104">Un objet [**Parameters**](swbemmethod-inparameters.md) contient la liste de paramètres pour appeler des méthodes de fournisseur lors de l’utilisation d’un type **ExecMethod** d’appel.</span><span class="sxs-lookup"><span data-stu-id="41969-104">An [**InParameters**](swbemmethod-inparameters.md) object contains the parameter list for calling provider methods when using an **ExecMethod** type of call.</span></span> <span data-ttu-id="41969-105">Les méthodes [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)et [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requièrent tous un objet **Parameters** .</span><span class="sxs-lookup"><span data-stu-id="41969-105">The [**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods all require an **InParameters** object.</span></span>

<span data-ttu-id="41969-106">La procédure suivante décrit comment construire un objet [**inparamètres**](swbemmethod-inparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="41969-106">The following procedure describes how to construct an [**InParameters**](swbemmethod-inparameters.md) object.</span></span>

<span data-ttu-id="41969-107">**Pour construire le paramètre *objwbemInParams***</span><span class="sxs-lookup"><span data-stu-id="41969-107">**To construct the *objwbemInParams* parameter**</span></span>

1.  <span data-ttu-id="41969-108">Connectez-vous à WMI.</span><span class="sxs-lookup"><span data-stu-id="41969-108">Connect to WMI.</span></span>
2.  <span data-ttu-id="41969-109">Obtenez la définition de la classe WMI qui définit la méthode que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="41969-109">Obtain the definition of the WMI class that defines the method you want to execute.</span></span>
3.  <span data-ttu-id="41969-110">Obtenez un objet [**inparamètres**](swbemmethod-inparameters.md) spécifique à la méthode de classe WMI que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="41969-110">Obtain an [**InParameters**](swbemmethod-inparameters.md) object specific to the WMI class method you want to execute.</span></span>

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  <span data-ttu-id="41969-111">Définissez les propriétés de l’instance sur les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="41969-111">Set the properties of the instance to whatever values are appropriate.</span></span> <span data-ttu-id="41969-112">Veillez à attribuer des valeurs aux propriétés de clé dans la classe WMI qui contient la méthode que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="41969-112">Be sure to give values to the key properties in the WMI class that contains the method you want to execute.</span></span>

    <span data-ttu-id="41969-113">Par exemple, si vous souhaitez définir un paramètre d’entrée nommé myinputparam sur la valeur « ABC » dans une instance d' [**inparamètres**](swbemmethod-inparameters.md) appelée « inst », le code doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="41969-113">For example, if you want to set an input parameter named myinputparam to the value "abc" in an instance of [**InParameters**](swbemmethod-inparameters.md) called "INST", the code would look like this.</span></span>

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  <span data-ttu-id="41969-114">Exécutez la méthode et obtenez l’état de retour de la méthode que vous exécutez.</span><span class="sxs-lookup"><span data-stu-id="41969-114">Execute the method and obtain the return status of the method you are executing.</span></span>

<span data-ttu-id="41969-115">L’exemple de code suivant illustre la configuration de l’objet [**inparamètres**](swbemmethod-inparameters.md) pour créer un nouvel objet WMI qui représente un partage.</span><span class="sxs-lookup"><span data-stu-id="41969-115">The following code example illustrates setting up the [**InParameters**](swbemmethod-inparameters.md) object to create a new WMI object that represents a share.</span></span> <span data-ttu-id="41969-116">Pour plus d’informations sur l’objet de [**paramètres de paramètres**](swbemmethod-outparameters.md) , consultez analyse des objets de [paramètres de paramètres](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="41969-116">For more information about the [**OutParameters**](swbemmethod-outparameters.md) object, see [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="41969-117">Cet exemple retourne une valeur de retour réussie (0) s’il existe un dossier nommé « Share » à l’emplacement « C:/share ».</span><span class="sxs-lookup"><span data-stu-id="41969-117">This example returns a successful return value (0) if there is a folder named "Share" at the location "C:/Share".</span></span> <span data-ttu-id="41969-118">Cet exemple permet de partager ce dossier avec d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="41969-118">This example enables this folder to be shared with other users.</span></span>


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



 

 



