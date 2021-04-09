---
description: L’objet de script SWbemObject est l’objet WMI générique, qui définit des propriétés et des méthodes qui peuvent être utilisées indépendamment de l’objet WMI spécifique auquel l’objet SWbemObject est lié.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Écriture de scripts avec SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114891"
---
# <a name="scripting-with-swbemobject"></a><span data-ttu-id="2b5c4-103">Écriture de scripts avec SWbemObject</span><span class="sxs-lookup"><span data-stu-id="2b5c4-103">Scripting with SWbemObject</span></span>

<span data-ttu-id="2b5c4-104">L’objet de script [**SWbemObject**](swbemobject.md) est l’objet WMI générique, qui définit des propriétés et des méthodes qui peuvent être utilisées indépendamment de l’objet WMI spécifique auquel l’objet **SWbemObject** est lié.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-104">The [**SWbemObject**](swbemobject.md) scripting object is the generic WMI object, defining properties and methods that can be used regardless of the specific WMI object to which the **SWbemObject** object is bound.</span></span> <span data-ttu-id="2b5c4-105">Tous les objets WMI, tels qu’une instance [**de \_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou toute autre classe de données WMI, sont représentés par [**SWbemObject**](swbemobject.md) et peuvent utiliser les propriétés et méthodes communes **SWbemObject** en plus de leurs propres propriétés et méthodes.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-105">All WMI objects, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or any other WMI data class, are represented by [**SWbemObject**](swbemobject.md) and can use the **SWbemObject** common properties and methods in addition to their own particular properties and methods.</span></span>

<span data-ttu-id="2b5c4-106">Par exemple, utilisez le script suivant pour obtenir toutes les instances d’un [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) en appelant la méthode [**SWbemObject. instances \_**](swbemobject-instances-.md) .</span><span class="sxs-lookup"><span data-stu-id="2b5c4-106">For example, use the following script to obtain all of the instances of a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) by calling the [**SWbemObject.Instances\_**](swbemobject-instances-.md) method.</span></span> <span data-ttu-id="2b5c4-107">ClsobjProcess représente à la fois la définition de classe de **\_ processus Win32** et un [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-107">The clsobjProcess represents both the **Win32\_Process** class definition and an [**SWbemObject**](swbemobject.md).</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="2b5c4-108">L’exemple suivant obtient une instance spécifique du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) qui représente le service d’alerte et le stocke dans objAlerter.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-108">The following example obtains a specific instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) that represents the Alerter service and stores it in objAlerter.</span></span> <span data-ttu-id="2b5c4-109">Vous pouvez ensuite appeler les méthodes [**SWbemObject**](swbemobject.md) , telles que WScript. Echo ObjAlerter. Path \_ , ou les méthodes définies par la classe de données, telles que WScript. Echo objAlerter. State.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-109">You can then call either [**SWbemObject**](swbemobject.md) methods, such as WScript.Echo objAlerter.Path\_, or methods defined by the data class, such as WScript.Echo objAlerter.State.</span></span> <span data-ttu-id="2b5c4-110">objAlerter qui représente une instance de service Win32 \_ et un **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-110">objAlerter which represents both an instance of Win32\_Service and an **SWbemObject**.</span></span>


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



<span data-ttu-id="2b5c4-111">L’appel à [**SWbemObject. instances \_**](swbemobject-instances-.md) obtient un autre objet de script WMI générique, [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-111">The call to [**SWbemObject.Instances\_**](swbemobject-instances-.md) obtains another generic WMI scripting object, [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="2b5c4-112">Comme indiqué, l’objet **SWbemObjectSet** peut être traité comme une [collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-112">As shown, the **SWbemObjectSet** object can be treated as a [collection](accessing-a-collection.md).</span></span>


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



<span data-ttu-id="2b5c4-113">Vous pouvez identifier les méthodes [**SWbemObject**](swbemobject.md) , car elles se terminent toutes par un trait de soulignement ( \_ ), par exemple [**SWbemObject. instances \_**](swbemobject-instances-.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-113">You can identify the [**SWbemObject**](swbemobject.md) methods because they all end with an underscore (\_), for example, [**SWbemObject.Instances\_**](swbemobject-instances-.md).</span></span>

<span data-ttu-id="2b5c4-114">[**SWbemObjectEx**](swbemobjectex.md) étend les propriétés de [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-114">[**SWbemObjectEx**](swbemobjectex.md) extends the properties of [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="2b5c4-115">Par exemple, vous pouvez maintenant mettre à jour les données de n’importe quel objet WMI, par exemple une instance de [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process), par un appel à [**\_ SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-115">For example, you can now update the data of any WMI object, such as an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process), by a call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md).</span></span>

<span data-ttu-id="2b5c4-116">L’exemple suivant montre comment les données de défaillance de page de processus système peuvent être actualisées toutes les cinq secondes.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-116">The following example shows how the system process page fault data can be refreshed every five seconds.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



<span data-ttu-id="2b5c4-117">Pour plus d’informations sur l’actualisation des données à l’aide d’un objet [**SWbemRefresher**](swbemrefresher.md) , consultez [actualisation des données WMI dans des scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-117">For more information about refreshing data using an [**SWbemRefresher**](swbemrefresher.md) object, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="2b5c4-118">Les objets [**SWbemObject. \_ put**](swbemobject-put-.md) et [**\_ PutAsync**](swbemobject-putasync-.md) vous permettent d’écrire des modifications dans n’importe quel objet WMI.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-118">The [**SWbemObject.Put\_**](swbemobject-put-.md) and [**PutAsync\_**](swbemobject-putasync-.md) allow you to write changes back to any WMI object.</span></span> <span data-ttu-id="2b5c4-119">Ces méthodes valident uniquement les modifications apportées à un objet dans l’espace de noms dans lequel l’objet a été créé.</span><span class="sxs-lookup"><span data-stu-id="2b5c4-119">These methods only commit changes to an object in the namespace where the object was created.</span></span> <span data-ttu-id="2b5c4-120">Vous pouvez écrire l’objet dans un autre espace de noms à l’aide de [**SWbemServicesEx. put**](swbemservicesex-put.md) ou [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c4-120">You can write the object to a different namespace using [**SWbemServicesEx.Put**](swbemservicesex-put.md) or [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b5c4-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b5c4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b5c4-122">API de script pour WMI</span><span class="sxs-lookup"><span data-stu-id="2b5c4-122">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="2b5c4-123">Création d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="2b5c4-123">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="2b5c4-124">Mise à jour d’une instance entière</span><span class="sxs-lookup"><span data-stu-id="2b5c4-124">Updating an Entire Instance</span></span>](updating-an-entire-instance.md)
</dt> <dt>

[<span data-ttu-id="2b5c4-125">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="2b5c4-125">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
