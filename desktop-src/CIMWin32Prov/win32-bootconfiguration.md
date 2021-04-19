---
description: La \_ classe WMI BootConfiguration WMI représente la configuration de démarrage d’un système informatique exécutant Windows.
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Classe Win32_BootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514361"
---
# <a name="win32_bootconfiguration-class"></a><span data-ttu-id="1cf7a-103">\_Classe BootConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="1cf7a-103">Win32\_BootConfiguration class</span></span>

<span data-ttu-id="1cf7a-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BootConfiguration** WMI représente la configuration de démarrage d’un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-104">The **Win32\_BootConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the boot configuration of a computer system running Windows.</span></span>

<span data-ttu-id="1cf7a-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1cf7a-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf7a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cf7a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a><span data-ttu-id="1cf7a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="1cf7a-108">Members</span></span>

<span data-ttu-id="1cf7a-109">La classe **Win32 \_ BootConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1cf7a-109">The **Win32\_BootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="1cf7a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cf7a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cf7a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cf7a-111">Properties</span></span>

<span data-ttu-id="1cf7a-112">La classe **Win32 \_ BootConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-112">The **Win32\_BootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cf7a-113">**BootDirectory**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-113">**BootDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-116">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| Process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir »)</span><span class="sxs-lookup"><span data-stu-id="1cf7a-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-117">Chemin d’accès aux fichiers système requis pour le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-117">Path to the system files required for booting the system.</span></span>

<span data-ttu-id="1cf7a-118">Exemple : « C : \\ Windows »</span><span class="sxs-lookup"><span data-stu-id="1cf7a-118">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1cf7a-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-123">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-123">Short textual description of the current object.</span></span>

<span data-ttu-id="1cf7a-124">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1cf7a-124">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-125">**ConfigurationPath**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-125">**ConfigurationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| Process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir »)</span><span class="sxs-lookup"><span data-stu-id="1cf7a-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-129">Chemin d’accès aux fichiers de configuration.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-129">Path to the configuration files.</span></span> <span data-ttu-id="1cf7a-130">Cette valeur peut être similaire à la valeur de la propriété **BootDirectory** .</span><span class="sxs-lookup"><span data-stu-id="1cf7a-130">This value may be similar to the value in the **BootDirectory** property.</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-134">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-134">Textual description of the current object.</span></span>

<span data-ttu-id="1cf7a-135">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1cf7a-135">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-136">**LastDrive**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-136">**LastDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions de fichier \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="1cf7a-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-140">Dernière lettre de lecteur à laquelle un lecteur physique est attribué.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-140">Last drive letter to which a physical drive is assigned.</span></span>

<span data-ttu-id="1cf7a-141">Exemple : « E : »</span><span class="sxs-lookup"><span data-stu-id="1cf7a-141">Example: "E:"</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-145">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="1cf7a-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-146">Nom de la configuration de démarrage.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-146">Name of the boot configuration.</span></span> <span data-ttu-id="1cf7a-147">Il s’agit d’un identificateur pour la configuration de démarrage.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-147">It is an identifier for the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-148">**ScratchDirectory**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-148">**ScratchDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-151">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions de fichier \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="1cf7a-151">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-152">Répertoire dans lequel les fichiers temporaires peuvent résider au moment du démarrage.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-152">Directory where temporary files can reside during boot time.</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-153">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-153">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-156">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1cf7a-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-157">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-157">Identifier by which the current object is known.</span></span>

<span data-ttu-id="1cf7a-158">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1cf7a-158">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cf7a-159">**TempDirectory**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-159">**TempDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cf7a-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cf7a-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cf7a-162">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| , fonctions de fichier \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="1cf7a-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="1cf7a-163">Répertoire dans lequel sont stockés les fichiers temporaires.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-163">Directory where temporary files are stored.</span></span>

<span data-ttu-id="1cf7a-164">Exemple : « C : \\ temp »</span><span class="sxs-lookup"><span data-stu-id="1cf7a-164">Example: "C:\\TEMP"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cf7a-165">Notes</span><span class="sxs-lookup"><span data-stu-id="1cf7a-165">Remarks</span></span>

<span data-ttu-id="1cf7a-166">La classe **Win32 \_ BootConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1cf7a-166">The **Win32\_BootConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1cf7a-167">Exemples</span><span class="sxs-lookup"><span data-stu-id="1cf7a-167">Examples</span></span>

<span data-ttu-id="1cf7a-168">La [liste des propriétés de configuration de démarrage d’un exemple perl d’ordinateur](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) retourne les informations de configuration de démarrage pour un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-168">The [List the Boot Configuration Properties of a Computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl sample returns boot configuration information for a computer.</span></span>

<span data-ttu-id="1cf7a-169">L’exemple VBScript suivant retourne les informations de configuration de démarrage d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1cf7a-169">The following VBScript sample returns boot configuration information for a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



<span data-ttu-id="1cf7a-170">L’exemple de code suivant illustre l’utilisation de la classe WMI **Win32 \_ BootConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="1cf7a-170">The following code sample demonstrates the use of the **Win32\_BootConfiguration** WMI class.</span></span>


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



<span data-ttu-id="1cf7a-171">L’exemple de code précédent crée la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="1cf7a-171">The previous code sample creates the following output:</span></span>

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a><span data-ttu-id="1cf7a-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cf7a-172">Requirements</span></span>



| <span data-ttu-id="1cf7a-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cf7a-173">Requirement</span></span> | <span data-ttu-id="1cf7a-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cf7a-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf7a-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf7a-175">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf7a-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cf7a-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1cf7a-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf7a-177">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf7a-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cf7a-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1cf7a-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1cf7a-179">Namespace</span></span><br/>                | <span data-ttu-id="1cf7a-180">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1cf7a-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1cf7a-181">MOF</span><span class="sxs-lookup"><span data-stu-id="1cf7a-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cf7a-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cf7a-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cf7a-183">DLL</span><span class="sxs-lookup"><span data-stu-id="1cf7a-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cf7a-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cf7a-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf7a-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cf7a-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf7a-186">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="1cf7a-186">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="1cf7a-187">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1cf7a-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

