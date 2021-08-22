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
ms.openlocfilehash: a56eca450757086b3d334d8f64fa41c4cf297f903963498afe958bee802705eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464189"
---
# <a name="creating-a-wmi-script"></a>Création d’un script WMI

Vous pouvez afficher ou manipuler les informations rendues disponibles par le biais de WMI à l’aide de scripts. les scripts peuvent être écrits dans n’importe quel langage de script prenant en charge Microsoft ActiveX script hosting, y compris Visual Basic scripting Edition (VBScript), PowerShell et Perl. Windows Script Host (WSH), Active Server pages et Internet Explorer peuvent tous héberger des scripts WMI.

> [!Note]
>
> Le langage de script principal actuellement pris en charge par WMI est PowerShell. Toutefois, WMI contient également un ensemble robuste de prise en charge des scripts pour VBScript et d’autres langages qui accèdent à l' [API de script pour WMI](scripting-api-for-wmi.md).

 

## <a name="wmi-scripting-languages"></a>Langages de script WMI

les deux principaux langages pris en charge par WMI sont PowerShell et VBScript (via le Windows Script Host ou WSH).

-   **PowerShell** a été conçu avec une intégration étroite avec WMI à l’esprit. Ainsi, la plupart des éléments sous-jacents de WMI sont intégrés aux applets de commande WMI : l’applet de commande Set- [WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)et [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1). Le tableau suivant décrit les processus généraux utilisés pour accéder aux informations WMI. Notez que, bien que la plupart de ces exemples utilisent l’applet de commande-WMIObject, la plupart des applets de commande PowerShell WMI ont les mêmes paramètres, tels que *-Class* ou *-Credentials*. Par conséquent, un grand nombre de ces processus fonctionnent également pour d’autres objets. pour une discussion plus approfondie de PowerShell et wmi, consultez utilisation de [l’applet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) de commande Get-WMiObject et [Windows PowerShell-la connexion wmi](/previous-versions/technet-magazine/cc162365(v=msdn.10)).

-   **VBScript**, en revanche, effectue explicitement des appels à l' [API de script pour WMI](scripting-api-for-wmi.md), comme indiqué ci-dessus. D’autres langages, tels que Perl, peuvent également utiliser l’API de script pour WMI. Toutefois, dans le cadre de cette documentation, la plupart des exemples qui illustrent l’API de script pour WMI utilisent VBScript. Toutefois, lorsqu’une technique de programmation est spécifique à VBScript, elle est appelée out.

    VBScript a essentiellement deux manières différentes d’accéder à WMI. Le premier utilise un objet [**SWbemLocator**](swbemlocator.md) pour se connecter à WMI. Vous pouvez également utiliser [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) et un moniker. Un moniker est une chaîne qui peut décrire un certain nombre d’éléments : vos informations d’identification, les paramètres d’emprunt d’identité, l’ordinateur auquel vous souhaitez vous connecter, l' [*espace de noms*](gloss-n.md) WMI (c’est-à-dire l’emplacement général où WMI stocke des groupes d’objets) et l’objet WMI que vous souhaitez récupérer. La plupart des exemples ci-dessous décrivent ces deux techniques. Pour plus d’informations, consultez [construction d’une chaîne de moniker](constructing-a-moniker-string.md) et [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

    Quelle que soit la technique que vous utilisez pour vous connecter à WMI, vous récupérerez probablement un ou plusieurs objets à partir de l’API de script. Le plus courant est [**SWbemObject**](swbemobject.md), que WMI utilise pour décrire un objet WMI. Vous pouvez également utiliser un objet [**SWbemServices**](swbemservices.md) pour décrire le service WMI lui-même, ou un objet [**SWbemObjectPath**](swbemobjectpath.md) pour décrire l’emplacement d’un objet WMI. Pour plus d’informations, consultez l' [écriture de scripts avec SWbemObject](scripting-with-swbemobject.md) et les [objets d’assistance de script](scripting-helper-objects.md).

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>À l’aide de WMI et d’un langage de script, comment...

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... se connecter à WMI ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, récupérez un objet [**SWbemServices**](swbemservices.md) avec moniker et un appel à [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)). Vous pouvez également vous connecter au serveur à l’aide d’un appel à [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Vous pouvez ensuite utiliser l’objet pour accéder à un espace de noms WMI spécifique ou à une instance de classe WMI.

Pour PowerShell, la connexion à WMI est généralement effectuée directement dans l’appel d’applet de commande. par conséquent, aucune étape supplémentaire n’est nécessaire.

Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md), [construction d’une chaîne de moniker](constructing-a-moniker-string.md)et [connexion à WMI avec VBScript](connecting-to-wmi-with-vbscript.md).


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

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... récupérer des informations à partir de WMI ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, utilisez une fonction de récupération, telle que [**WbemServices. obtenir**](swbemservices-get.md) ou [**WbemServices. InstancesOf**](swbemservices-instancesof.md). Vous pouvez également placer le nom de classe de l’objet à récupérer dans un moniker, ce qui peut être plus efficace.

Pour PowerShell, utilisez le paramètre *-Class* . Notez que-Class est le paramètre par défaut ; par conséquent, vous n’avez pas besoin de l’indiquer explicitement.

Pour plus d’informations, consultez [récupération de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).


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

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... créer une requête WMI ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, utilisez la méthode [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .

Pour PowerShell, utilisez le paramètre *-query* . Vous pouvez également filtrer à l’aide du paramètre *-Filter* .

Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).


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

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... énumérer une liste d’objets WMI ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, utilisez l’objet de conteneur [**SWbemObjectSet**](swbemobjectset.md) , qui est traité dans le script en tant que collection pouvant être énumérée. Vous pouvez récupérer une **SWbemObjectSet** à partir d’un appel de [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md).

PowerShell est en mesure de récupérer et de gérer les énumérations comme tout autre objet. WMI n’a rien d’particulier.

Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).


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

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... accéder à un autre espace de noms WMI ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, indiquez l’espace de noms dans le moniker, sinon vous pouvez déclarer explicitement l’espace de noms dans l’appel à [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

Pour PowerShell, utilisez le paramètre *-namespace* . L’espace de noms par défaut est « root \\ cimV2 ». Toutefois, de nombreuses classes plus anciennes sont stockées dans « root \\ default ».

Pour Rechercher l’emplacement d’une classe WMI donnée, consultez la page de référence. Vous pouvez également explorer manuellement un espace de noms à l’aide de la mise en route.


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

<span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... récupérer toutes les instances enfants d’une classe ?
</dt> <dd>

Pour les langages qui utilisent directement l’API de script pour WMI et PowerShell, WMI prend en charge la récupération des classes enfants d’une classe de base. Par conséquent, pour récupérer les instances enfants, vous devez uniquement Rechercher la classe parente. l’exemple suivant recherche le [**\_ disque logique CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), qui est une classe WMI préinstallée qui représente les disques logiques sur un système informatique basé sur Windows. par conséquent, la recherche de cette classe parente retourne également des instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), ce que Windows utilise pour décrire les disques durs. Pour plus d’informations, consultez [Common Information Model](common-information-model.md). WMI fournit un schéma entier de ces classes préinstallées qui vous permettent d’accéder aux objets managés et de les contrôler. Pour plus d’informations, consultez [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider) et [classes WMI](wmi-classes.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... localiser un objet WMI ?
</dt> <dd>

Pour l’API de script pour WMI et PowerShell, WMI utilise une combinaison d’espace de noms, de nom de classe et de propriétés de clé pour identifier de façon unique une instance WMI donnée. Ensemble, c’est ce que l’on appelle le chemin de l’objet WMI. Pour VBScript, la propriété [**SWbemObject. \_ path**](swbemobject-path-.md) décrit le chemin d’accès d’un objet donné retourné par l’API de script. Pour PowerShell, chaque objet WMI aura une \_ \_ propriété Path. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md) .

En plus de l’espace de noms et du nom de classe, un objet WMI aura également une propriété de clé, qui identifie de façon unique cette instance par rapport à d’autres instances sur votre ordinateur. Par exemple, la propriété **DeviceID** est la propriété de clé pour la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Pour plus d’informations, consultez [format MOF (MOF)](managed-object-format--mof-.md).

Enfin, le chemin d’accès relatif est simplement une forme raccourcie du chemin d’accès et comprend le nom de la classe et la valeur de la clé. Dans les exemples ci-dessous, le chemin d’accès peut être « \\ \\ nom_ordinateur \\ root \\ cimv2 : Win32 \_ LogicalDisk. DeviceID = "d :" », alors que le chemin d’accès relatif est « Win32LogicalDisk. DeviceID = "d" " ».


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

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... définir des informations dans WMI ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, utilisez la méthode [**SWbemObject. \_ put**](swbemobject-put-.md) .

Pour PowerShell, vous pouvez utiliser la méthode put ou [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

Pour plus d’informations, consultez [modification d’une propriété d’instance](modifying-an-instance-property.md).


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

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... utiliser d’autres informations d’identification ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, utilisez les paramètres *username* et *Password* dans la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

Pour PowerShell, utilisez le paramètre *-Credential* .

Notez que vous pouvez uniquement utiliser d’autres informations d’identification sur un système distant. Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).


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

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... accéder à un ordinateur distant ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, indiquez explicitement le nom de l’ordinateur dans le moniker, ou sinon dans l’appel à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Pour plus d’informations, consultez [connexion à WMI à distance avec VBScript](connecting-to-wmi-remotely-with-vbscript.md).

Pour PowerShell, utilisez le paramètre *-ComputerName* . Pour plus d’informations, consultez [connexion à WMI à distance avec PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).


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

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... définir les niveaux d’authentification et d’emprunt d’identité ?
</dt> <dd>

Pour VBScript et l’API de script pour WMI, utilisez la propriété [**SWbemServices. \_ Security**](swbemlocator-security-.md) sur l’objet serveur retourné, ou définissez les valeurs pertinentes dans le moniker.

Pour PowerShell, utilisez respectivement les paramètres *d’authentification et d’emprunt d'* *identité* . Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).

Pour plus d’informations, consultez [sécurisation des scripts pour les clients](securing-scripting-clients.md).


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

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... gérer les erreurs dans WMI ?
</dt> <dd>

Pour l’API de script pour WMI, le fournisseur peut fournir un objet [**SWbemLastError**](swbemlasterror.md) pour donner plus d’informations sur une erreur.

En particulier, dans VBScript, la gestion des erreurs est également prise en charge à l’aide de l’objet **Err** natif. Vous pouvez également accéder à l’objet [**SWbemLastError**](swbemlasterror.md), comme décrit ci-dessus. Pour plus d’informations, consultez [extraction d’un code d’erreur](retrieving-an-error-code.md).

Pour PowerShell, vous pouvez utiliser les techniques de gestion des erreurs PowerShell standard. Pour plus d’informations, consultez [Introduction à la gestion des erreurs dans PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).


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

 

 
