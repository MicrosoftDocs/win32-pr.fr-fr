---
description: Vous pouvez afficher ou manipuler les informations rendues disponibles par le biais de WMI à l’aide de scripts.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Création d’un script WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953142"
---
# <a name="creating-a-wmi-script"></a><span data-ttu-id="88c44-103">Création d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="88c44-103">Creating a WMI Script</span></span>

<span data-ttu-id="88c44-104">Vous pouvez afficher ou manipuler les informations rendues disponibles par le biais de WMI à l’aide de scripts.</span><span class="sxs-lookup"><span data-stu-id="88c44-104">You can view or manipulate any information made available through WMI using scripts.</span></span> <span data-ttu-id="88c44-105">Les scripts peuvent être écrits dans n’importe quel langage de script qui prend en charge l’hébergement de scripts Microsoft ActiveX, y compris Visual Basic Scripting Edition (VBScript), PowerShell et Perl.</span><span class="sxs-lookup"><span data-stu-id="88c44-105">Scripts can be written in any scripting language that supports Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript), PowerShell, and Perl.</span></span> <span data-ttu-id="88c44-106">Windows Script Host (WSH), Active Server pages et Internet Explorer peuvent tous héberger des scripts WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-106">Windows Script Host (WSH), Active Server Pages, and Internet Explorer can all host WMI scripts.</span></span>

> [!Note]
>
> <span data-ttu-id="88c44-107">Le langage de script principal actuellement pris en charge par WMI est PowerShell.</span><span class="sxs-lookup"><span data-stu-id="88c44-107">The primary scripting language currently supported by WMI is PowerShell.</span></span> <span data-ttu-id="88c44-108">Toutefois, WMI contient également un ensemble robuste de prise en charge des scripts pour VBScript et d’autres langages qui accèdent à l' [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-108">However, WMI also contains a robust body of scripting support for VBScript and other languages that access the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

 

## <a name="wmi-scripting-languages"></a><span data-ttu-id="88c44-109">Langages de script WMI</span><span class="sxs-lookup"><span data-stu-id="88c44-109">WMI Scripting Languages</span></span>

<span data-ttu-id="88c44-110">Les deux principaux langages pris en charge par WMI sont PowerShell et VBScript (via Windows Script Host ou WSH).</span><span class="sxs-lookup"><span data-stu-id="88c44-110">The two main languages supported by WMI are PowerShell and VBScript (through the Windows Script Host, or WSH).</span></span>

-   <span data-ttu-id="88c44-111">**PowerShell** a été conçu avec une intégration étroite avec WMI à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="88c44-111">**PowerShell** was designed with tight integration with WMI in mind.</span></span> <span data-ttu-id="88c44-112">Ainsi, la plupart des éléments sous-jacents de WMI sont intégrés aux applets de commande WMI : l’applet de commande Set- [WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)et [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span><span class="sxs-lookup"><span data-stu-id="88c44-112">As such, much of the underlying elements of WMI are built into the WMI cmdlets: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1), and [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span></span> <span data-ttu-id="88c44-113">Le tableau suivant décrit les processus généraux utilisés pour accéder aux informations WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-113">The following table describes the general processes used for accessing WMI information.</span></span> <span data-ttu-id="88c44-114">Notez que, bien que la plupart de ces exemples utilisent l’applet de commande-WMIObject, la plupart des applets de commande PowerShell WMI ont les mêmes paramètres, tels que *-Class* ou *-Credentials*.</span><span class="sxs-lookup"><span data-stu-id="88c44-114">Note that while most of these examples use Get-WMIObject, many of the PowerShell WMI cmdlets have the same parameters, such as *-Class* or *-Credentials*.</span></span> <span data-ttu-id="88c44-115">Par conséquent, un grand nombre de ces processus fonctionnent également pour d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="88c44-115">Therefore, many of these processes also work for other objects.</span></span> <span data-ttu-id="88c44-116">Pour une discussion plus approfondie de PowerShell et WMI, consultez Utilisation de [l’applet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) de commande Get-WMiObject et [Windows PowerShell : la connexion WMI](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="88c44-116">For a more in-depth discussion of PowerShell and WMI, see [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and [Windows PowerShell - the WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span></span>

-   <span data-ttu-id="88c44-117">**VBScript**, en revanche, effectue explicitement des appels à l' [API de script pour WMI](scripting-api-for-wmi.md), comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="88c44-117">**VBScript**, in contrast, explicitly makes calls to the [Scripting API for WMI](scripting-api-for-wmi.md), as mentioned above.</span></span> <span data-ttu-id="88c44-118">D’autres langages, tels que Perl, peuvent également utiliser l’API de script pour WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-118">Other languages, such as Perl, can also use the scripting API for WMI.</span></span> <span data-ttu-id="88c44-119">Toutefois, dans le cadre de cette documentation, la plupart des exemples qui illustrent l’API de script pour WMI utilisent VBScript.</span><span class="sxs-lookup"><span data-stu-id="88c44-119">However, for the purposes of this documentation, most samples that demonstrate the scripting API for WMI will use VBScript.</span></span> <span data-ttu-id="88c44-120">Toutefois, lorsqu’une technique de programmation est spécifique à VBScript, elle est appelée out.</span><span class="sxs-lookup"><span data-stu-id="88c44-120">When a programming technique is specific to VBScript, however, it will be called out.</span></span>

    <span data-ttu-id="88c44-121">VBScript a essentiellement deux manières différentes d’accéder à WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-121">VBScript has essentially two separate ways of accessing WMI.</span></span> <span data-ttu-id="88c44-122">Le premier utilise un objet [**SWbemLocator**](swbemlocator.md) pour se connecter à WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-122">The first is using an [**SWbemLocator**](swbemlocator.md) object to connect to WMI.</span></span> <span data-ttu-id="88c44-123">Vous pouvez également utiliser [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) et un moniker.</span><span class="sxs-lookup"><span data-stu-id="88c44-123">Alternately, you can use [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) and a moniker.</span></span> <span data-ttu-id="88c44-124">Un moniker est une chaîne qui peut décrire un certain nombre d’éléments : vos informations d’identification, les paramètres d’emprunt d’identité, l’ordinateur auquel vous souhaitez vous connecter, l' [*espace de noms*](gloss-n.md) WMI (c’est-à-dire l’emplacement général où WMI stocke des groupes d’objets) et l’objet WMI que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="88c44-124">A moniker is a string that can describe a number of elements: your credentials, impersonation settings, what computer you want to connect to, the WMI [*namespace*](gloss-n.md) (ie, the general location where WMI stores groups of objects), and what WMI object you want to retrieve.</span></span> <span data-ttu-id="88c44-125">La plupart des exemples ci-dessous décrivent ces deux techniques.</span><span class="sxs-lookup"><span data-stu-id="88c44-125">Many of the examples below describe both techniques.</span></span> <span data-ttu-id="88c44-126">Pour plus d’informations, consultez [construction d’une chaîne de moniker](constructing-a-moniker-string.md) et [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-126">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md) and [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

    <span data-ttu-id="88c44-127">Quelle que soit la technique que vous utilisez pour vous connecter à WMI, vous récupérerez probablement un ou plusieurs objets à partir de l’API de script.</span><span class="sxs-lookup"><span data-stu-id="88c44-127">Regardless of what technique you use to connect to WMI, you will likely retrieve one or more objects from the Scripting API.</span></span> <span data-ttu-id="88c44-128">Le plus courant est [**SWbemObject**](swbemobject.md), que WMI utilise pour décrire un objet WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-128">The most common is [**SWbemObject**](swbemobject.md), which WMI uses to describe a WMI object.</span></span> <span data-ttu-id="88c44-129">Vous pouvez également utiliser un objet [**SWbemServices**](swbemservices.md) pour décrire le service WMI lui-même, ou un objet [**SWbemObjectPath**](swbemobjectpath.md) pour décrire l’emplacement d’un objet WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-129">Alternately, you may use an [**SWbemServices**](swbemservices.md) object to describe the WMI service itself, or an [**SWbemObjectPath**](swbemobjectpath.md) object to describe the location of a WMI object.</span></span> <span data-ttu-id="88c44-130">Pour plus d’informations, consultez l' [écriture de scripts avec SWbemObject](scripting-with-swbemobject.md) et les [objets d’assistance de script](scripting-helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-130">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md) and [Scripting Helper Objects](scripting-helper-objects.md).</span></span>

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a><span data-ttu-id="88c44-131">À l’aide de WMI et d’un langage de script, comment...</span><span class="sxs-lookup"><span data-stu-id="88c44-131">Using WMI and a Scripting Language, How Do I...</span></span>

<dl> <dt>

<span data-ttu-id="88c44-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... se connecter à WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...connect to WMI?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-133">Pour VBScript et l’API de script pour WMI, récupérez un objet [**SWbemServices**](swbemservices.md) avec moniker et un appel à [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span><span class="sxs-lookup"><span data-stu-id="88c44-133">For VBScript and the Scripting API for WMI, retrieve an [**SWbemServices**](swbemservices.md) object with a moniker and a call to [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span></span> <span data-ttu-id="88c44-134">Vous pouvez également vous connecter au serveur à l’aide d’un appel à [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="88c44-134">Alternately, you can connect to the server with a call to [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="88c44-135">Vous pouvez ensuite utiliser l’objet pour accéder à un espace de noms WMI spécifique ou à une instance de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-135">You can then use the object to access a specific WMI namespace or WMI class instance.</span></span>

<span data-ttu-id="88c44-136">Pour PowerShell, la connexion à WMI est généralement effectuée directement dans l’appel d’applet de commande. par conséquent, aucune étape supplémentaire n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="88c44-136">For PowerShell, connecting to WMI is generally done directly in the cmdlet call; as such, no additional steps are necessary.</span></span>

<span data-ttu-id="88c44-137">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md), [construction d’une chaîne de moniker](constructing-a-moniker-string.md)et [connexion à WMI avec VBScript](connecting-to-wmi-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-137">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md), [Constructing a Moniker String](constructing-a-moniker-string.md), and [Connecting to WMI with VBScript](connecting-to-wmi-with-vbscript.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span data-ttu-id="88c44-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... récupérer des informations à partir de WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...retrieve information from WMI?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-139">Pour VBScript et l’API de script pour WMI, utilisez une fonction de récupération, telle que [**WbemServices. obtenir**](swbemservices-get.md) ou [**WbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-139">For VBScript and the Scripting API for WMI, use a retrieval function, such as [**WbemServices.Get**](swbemservices-get.md) or [**WbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span> <span data-ttu-id="88c44-140">Vous pouvez également placer le nom de classe de l’objet à récupérer dans un moniker, ce qui peut être plus efficace.</span><span class="sxs-lookup"><span data-stu-id="88c44-140">You may also place the class name of the object to retrieve in a moniker, which may be more efficient.</span></span>

<span data-ttu-id="88c44-141">Pour PowerShell, utilisez le paramètre *-Class* .</span><span class="sxs-lookup"><span data-stu-id="88c44-141">For PowerShell, use the *-Class* parameter.</span></span> <span data-ttu-id="88c44-142">Notez que-Class est le paramètre par défaut ; par conséquent, vous n’avez pas besoin de l’indiquer explicitement.</span><span class="sxs-lookup"><span data-stu-id="88c44-142">Note that -Class is the default parameter; as such, you don't need to explicitly state it.</span></span>

<span data-ttu-id="88c44-143">Pour plus d’informations, consultez [récupération de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-143">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span data-ttu-id="88c44-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... créer une requête WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...create a WMI query?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-145">Pour VBScript et l’API de script pour WMI, utilisez la méthode [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .</span><span class="sxs-lookup"><span data-stu-id="88c44-145">For VBScript and the Scripting API for WMI, use the [**SWbemServices.ExecQuery**](swbemservices-execquery.md) method.</span></span>

<span data-ttu-id="88c44-146">Pour PowerShell, utilisez le paramètre *-query* .</span><span class="sxs-lookup"><span data-stu-id="88c44-146">For PowerShell, use the *-Query* parameter.</span></span> <span data-ttu-id="88c44-147">Vous pouvez également filtrer à l’aide du paramètre *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="88c44-147">You can also filter using the *-Filter* parameter.</span></span>

<span data-ttu-id="88c44-148">Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-148">For more information, see [Querying WMI](querying-wmi.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span data-ttu-id="88c44-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... énumérer une liste d’objets WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...enumerate through a list of WMI objects?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-150">Pour VBScript et l’API de script pour WMI, utilisez l’objet de conteneur [**SWbemObjectSet**](swbemobjectset.md) , qui est traité dans le script en tant que collection pouvant être énumérée.</span><span class="sxs-lookup"><span data-stu-id="88c44-150">For VBScript and the Scripting API for WMI, use the [**SWbemObjectSet**](swbemobjectset.md) container object, which is treated in script as a collection that can be enumerated.</span></span> <span data-ttu-id="88c44-151">Vous pouvez récupérer une **SWbemObjectSet** à partir d’un appel de [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-151">You can retrieve an **SWbemObjectSet** from a call from [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="88c44-152">PowerShell est en mesure de récupérer et de gérer les énumérations comme tout autre objet. WMI n’a rien d’particulier.</span><span class="sxs-lookup"><span data-stu-id="88c44-152">PowerShell is able to retrieve and handle enumerations as it would any other object; there is nothing particularly unique to WMI.</span></span>

<span data-ttu-id="88c44-153">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-153">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span data-ttu-id="88c44-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... accéder à un autre espace de noms WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...access a different WMI namespace?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-155">Pour VBScript et l’API de script pour WMI, indiquez l’espace de noms dans le moniker, sinon vous pouvez déclarer explicitement l’espace de noms dans l’appel à [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="88c44-155">For VBScript and the Scripting API for WMI, state the namespace in the moniker, or else you can explicitly state the namespace in the call to [**SwbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

<span data-ttu-id="88c44-156">Pour PowerShell, utilisez le paramètre *-namespace* .</span><span class="sxs-lookup"><span data-stu-id="88c44-156">For PowerShell, use the *-Namespace* parameter.</span></span> <span data-ttu-id="88c44-157">L’espace de noms par défaut est « root \\ cimV2 ». Toutefois, de nombreuses classes plus anciennes sont stockées dans « root \\ default ».</span><span class="sxs-lookup"><span data-stu-id="88c44-157">The default namespace is "root\\cimV2"; however, many older classes are stored in "root\\default".</span></span>

<span data-ttu-id="88c44-158">Pour Rechercher l’emplacement d’une classe WMI donnée, consultez la page de référence.</span><span class="sxs-lookup"><span data-stu-id="88c44-158">To find the location of a given WMI class, look at the reference page.</span></span> <span data-ttu-id="88c44-159">Vous pouvez également explorer manuellement un espace de noms à l’aide de la mise en route.</span><span class="sxs-lookup"><span data-stu-id="88c44-159">Alternately, you can manually explore a namespace using get-WmiObject.</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span data-ttu-id="88c44-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... récupérer toutes les instances enfants d’une classe ?</span><span class="sxs-lookup"><span data-stu-id="88c44-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...retrieve all child instances of a class?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-161">Pour les langages qui utilisent directement l’API de script pour WMI et PowerShell, WMI prend en charge la récupération des classes enfants d’une classe de base.</span><span class="sxs-lookup"><span data-stu-id="88c44-161">For languages that directly use the Scripting API for WMI and PowerShell, WMI supports retrieving the child classes of a base class.</span></span> <span data-ttu-id="88c44-162">Par conséquent, pour récupérer les instances enfants, vous devez uniquement Rechercher la classe parente.</span><span class="sxs-lookup"><span data-stu-id="88c44-162">As such, in order to retrieve the child instances, you need to only search for the parent class.</span></span> <span data-ttu-id="88c44-163">L’exemple suivant recherche le [**\_ disque logique CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), qui est une classe WMI préinstallée qui représente des disques logiques sur un système informatique Windows.</span><span class="sxs-lookup"><span data-stu-id="88c44-163">The following example searches for [**CIM\_LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), which is a preinstalled WMI class that represents logical disks on a Windows-based computer system.</span></span> <span data-ttu-id="88c44-164">Par conséquent, la recherche de cette classe parente retourne également des instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), ce que Windows utilise pour décrire les disques durs.</span><span class="sxs-lookup"><span data-stu-id="88c44-164">As such, searching for this parent class also returns instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which is what Windows uses to describe hard drives.</span></span> <span data-ttu-id="88c44-165">Pour plus d’informations, consultez [Common Information Model](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-165">For more information, see [Common Information Model](common-information-model.md).</span></span> <span data-ttu-id="88c44-166">WMI fournit un schéma entier de ces classes préinstallées qui vous permettent d’accéder aux objets managés et de les contrôler.</span><span class="sxs-lookup"><span data-stu-id="88c44-166">WMI supplies an entire schema of such preinstalled classes that allow you to access and control managed objects.</span></span> <span data-ttu-id="88c44-167">Pour plus d’informations, consultez [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider) et [classes WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-167">For more information, see [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) and [WMI Classes](wmi-classes.md)..</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span data-ttu-id="88c44-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... localiser un objet WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...locate a WMI object?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-169">Pour l’API de script pour WMI et PowerShell, WMI utilise une combinaison d’espace de noms, de nom de classe et de propriétés de clé pour identifier de façon unique une instance WMI donnée.</span><span class="sxs-lookup"><span data-stu-id="88c44-169">For both the Scripting API for WMI and PowerShell, WMI uses a combination of namespace, class name, and key properties to uniquely identify a given WMI instance.</span></span> <span data-ttu-id="88c44-170">Ensemble, c’est ce que l’on appelle le chemin de l’objet WMI.</span><span class="sxs-lookup"><span data-stu-id="88c44-170">Together, this is known as the WMI object path.</span></span> <span data-ttu-id="88c44-171">Pour VBScript, la propriété [**SWbemObject. \_ path**](swbemobject-path-.md) décrit le chemin d’accès d’un objet donné retourné par l’API de script.</span><span class="sxs-lookup"><span data-stu-id="88c44-171">For VBScript, the [**SWbemObject.Path\_**](swbemobject-path-.md) property describes the path for any given object returned by the scripting API.</span></span> <span data-ttu-id="88c44-172">Pour PowerShell, chaque objet WMI aura une \_ \_ propriété Path.</span><span class="sxs-lookup"><span data-stu-id="88c44-172">For PowerShell, every WMI object will have a \_\_PATH property.</span></span> <span data-ttu-id="88c44-173">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md) .</span><span class="sxs-lookup"><span data-stu-id="88c44-173">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md)</span></span>

<span data-ttu-id="88c44-174">En plus de l’espace de noms et du nom de classe, un objet WMI aura également une propriété de clé, qui identifie de façon unique cette instance par rapport à d’autres instances sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="88c44-174">In addition to namespace and class name, a WMI object will also have a key property, which uniquely identifies that instance compared to other instances on your machine.</span></span> <span data-ttu-id="88c44-175">Par exemple, la propriété **DeviceID** est la propriété de clé pour la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="88c44-175">For example, the **DeviceID** property is the key property for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="88c44-176">Pour plus d’informations, consultez [format MOF (MOF)](managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-176">For more information, see [Managed Object Format (MOF)](managed-object-format--mof-.md).</span></span>

<span data-ttu-id="88c44-177">Enfin, le chemin d’accès relatif est simplement une forme raccourcie du chemin d’accès et comprend le nom de la classe et la valeur de la clé.</span><span class="sxs-lookup"><span data-stu-id="88c44-177">Finally, the Relative path is simply a shortened form of the path, and includes the class name and key value.</span></span> <span data-ttu-id="88c44-178">Dans les exemples ci-dessous, le chemin d’accès peut être « \\ \\ nom_ordinateur \\ root \\ cimv2 : Win32 \_ LogicalDisk. DeviceID = "d :" », alors que le chemin d’accès relatif est « Win32LogicalDisk. DeviceID = "d" " ».</span><span class="sxs-lookup"><span data-stu-id="88c44-178">In the examples below, the path may be "\\\\computerName\\root\\cimv2:Win32\_LogicalDisk.DeviceID="D:"", while the relative path would be ""Win32LogicalDisk.DeviceID="D""".</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span data-ttu-id="88c44-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... définir des informations dans WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...set information in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-180">Pour VBScript et l’API de script pour WMI, utilisez la méthode [**SWbemObject. \_ put**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="88c44-180">For VBScript and the Scripting API for WMI, use the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span>

<span data-ttu-id="88c44-181">Pour PowerShell, vous pouvez utiliser la méthode put ou [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="88c44-181">For PowerShell, you can either use the Put method, or else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

<span data-ttu-id="88c44-182">Pour plus d’informations, consultez [modification d’une propriété d’instance](modifying-an-instance-property.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-182">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span data-ttu-id="88c44-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... utiliser d’autres informations d’identification ?</span><span class="sxs-lookup"><span data-stu-id="88c44-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...use different credentials?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-184">Pour VBScript et l’API de script pour WMI, utilisez les paramètres *username* et *Password* dans la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="88c44-184">For VBScript and the Scripting API for WMI, use the *UserName* and *Password* parameters in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

<span data-ttu-id="88c44-185">Pour PowerShell, utilisez le paramètre *-Credential* .</span><span class="sxs-lookup"><span data-stu-id="88c44-185">For PowerShell, use the *-Credential* parameter.</span></span>

<span data-ttu-id="88c44-186">Notez que vous pouvez uniquement utiliser d’autres informations d’identification sur un système distant.</span><span class="sxs-lookup"><span data-stu-id="88c44-186">Note that you can only use alternate credentials on a remote system.</span></span> <span data-ttu-id="88c44-187">Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-187">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="88c44-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... accéder à un ordinateur distant ?</span><span class="sxs-lookup"><span data-stu-id="88c44-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...access a remote computer?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-189">Pour VBScript et l’API de script pour WMI, indiquez explicitement le nom de l’ordinateur dans le moniker, ou sinon dans l’appel à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-189">For VBScript and the Scripting API for WMI, explicitly state the name of the computer in either the moniker, or else in the call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="88c44-190">Pour plus d’informations, consultez [connexion à WMI à distance avec VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-190">For more information, see [Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span></span>

<span data-ttu-id="88c44-191">Pour PowerShell, utilisez le paramètre *-ComputerName* .</span><span class="sxs-lookup"><span data-stu-id="88c44-191">For PowerShell, use the *-ComputerName* parameter.</span></span> <span data-ttu-id="88c44-192">Pour plus d’informations, consultez [connexion à WMI à distance avec PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-192">For more information, see [Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="88c44-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... définir les niveaux d’authentification et d’emprunt d’identité ?</span><span class="sxs-lookup"><span data-stu-id="88c44-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...set the Authentication and Impersonation levels?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-194">Pour VBScript et l’API de script pour WMI, utilisez la propriété [**SWbemServices. \_ Security**](swbemlocator-security-.md) sur l’objet serveur retourné, ou définissez les valeurs pertinentes dans le moniker.</span><span class="sxs-lookup"><span data-stu-id="88c44-194">For VBScript and the Scripting API for WMI, use the [**SWbemServices.Security\_**](swbemlocator-security-.md) property on the returned server object, or else set the relevant values in the moniker.</span></span>

<span data-ttu-id="88c44-195">Pour PowerShell, utilisez respectivement les paramètres *d’authentification et d’emprunt d'* *identité* .</span><span class="sxs-lookup"><span data-stu-id="88c44-195">For PowerShell, use the *-Authentication* and *-Impersonation* parameters, respectively.</span></span> <span data-ttu-id="88c44-196">Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-196">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="88c44-197">Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-197">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="88c44-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... gérer les erreurs dans WMI ?</span><span class="sxs-lookup"><span data-stu-id="88c44-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...handle errors in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="88c44-199">Pour l’API de script pour WMI, le fournisseur peut fournir un objet [**SWbemLastError**](swbemlasterror.md) pour donner plus d’informations sur une erreur.</span><span class="sxs-lookup"><span data-stu-id="88c44-199">For the Scripting API for WMI, the provider may supply an [**SWbemLastError**](swbemlasterror.md) object to give further information on an error.</span></span>

<span data-ttu-id="88c44-200">En particulier, dans VBScript, la gestion des erreurs est également prise en charge à l’aide de l’objet **Err** natif.</span><span class="sxs-lookup"><span data-stu-id="88c44-200">In VBScript in particular, error handling is also supported using the native **Err** object.</span></span> <span data-ttu-id="88c44-201">Vous pouvez également accéder à l’objet [**SWbemLastError**](swbemlasterror.md), comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="88c44-201">You may also access the [**SWbemLastError**](swbemlasterror.md)object, as described above.</span></span> <span data-ttu-id="88c44-202">Pour plus d’informations, consultez [extraction d’un code d’erreur](retrieving-an-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="88c44-202">For more information, see [Retrieving an Error Code](retrieving-an-error-code.md).</span></span>

<span data-ttu-id="88c44-203">Pour PowerShell, vous pouvez utiliser les techniques de gestion des erreurs PowerShell standard.</span><span class="sxs-lookup"><span data-stu-id="88c44-203">For PowerShell, you can use the standard PowerShell error handling techniques.</span></span> <span data-ttu-id="88c44-204">Pour plus d’informations, consultez [Introduction à la gestion des erreurs dans PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="88c44-204">For more information, see [An Introduction to Error Handling in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span></span>


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
