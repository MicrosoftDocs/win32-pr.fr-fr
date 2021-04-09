---
description: La \_ classe WMI singleton de WMISetting Win32 contient les paramètres opérationnels du service WMI. Cette classe ne peut avoir qu’une seule instance, qui existe toujours pour chaque système Windows et ne peut pas être supprimée. Impossible de créer des instances supplémentaires.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Classe Win32_WMISetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860682"
---
# <a name="win32_wmisetting-class"></a><span data-ttu-id="3574e-105">\_Classe WMISetting Win32</span><span class="sxs-lookup"><span data-stu-id="3574e-105">Win32\_WMISetting class</span></span>

<span data-ttu-id="3574e-106">La [classe WMI](../wmisdk/retrieving-a-class.md) singleton de **\_ WMISetting Win32** contient les paramètres opérationnels du service WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-106">The **Win32\_WMISetting** singleton [WMI class](../wmisdk/retrieving-a-class.md) contains the operational parameters for the WMI service.</span></span> <span data-ttu-id="3574e-107">Cette classe ne peut avoir qu’une seule instance, qui existe toujours pour chaque système Windows et ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="3574e-107">This class can only have one instance, which always exists for each Windows system and cannot be deleted.</span></span> <span data-ttu-id="3574e-108">Impossible de créer des instances supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3574e-108">Additional instances cannot be created.</span></span>

<span data-ttu-id="3574e-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3574e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3574e-110">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3574e-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3574e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3574e-111">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a><span data-ttu-id="3574e-112">Membres</span><span class="sxs-lookup"><span data-stu-id="3574e-112">Members</span></span>

<span data-ttu-id="3574e-113">La classe **Win32 \_ WMISetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3574e-113">The **Win32\_WMISetting** class has these types of members:</span></span>

-   [<span data-ttu-id="3574e-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3574e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3574e-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3574e-115">Properties</span></span>

<span data-ttu-id="3574e-116">La classe **Win32 \_ WMISetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3574e-116">The **Win32\_WMISetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3574e-117">**ASPScriptDefaultNamespace**</span><span class="sxs-lookup"><span data-stu-id="3574e-117">**ASPScriptDefaultNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-120">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| default namespace »)</span><span class="sxs-lookup"><span data-stu-id="3574e-120">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Default Namespace")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-121">Espace de noms de script par défaut.</span><span class="sxs-lookup"><span data-stu-id="3574e-121">Default script namespace.</span></span> <span data-ttu-id="3574e-122">Cette propriété contient l’espace de noms utilisé par les appels de l’API de script pour WMI si aucun n’est spécifié par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="3574e-122">This property contains the namespace used by calls from the Scripting API for WMI if none is specified by the caller.</span></span>

<span data-ttu-id="3574e-123">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-123">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-124">**HKEY \_ Logiciel de l' \_ ordinateur local** espace de \\  \\  \\  \\ **\| noms par défaut de script** WBEM Microsoft    </span><span class="sxs-lookup"><span data-stu-id="3574e-124">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **scripting\|Default Namespace**</span></span>

<span data-ttu-id="3574e-125">Exemple : root \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3574e-125">Example: root\\cimv2</span></span>

<span data-ttu-id="3574e-126">Pour obtenir un exemple de script qui utilise cette propriété, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3574e-126">For an example script that uses this property, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-127">**ASPScriptEnabled**</span><span class="sxs-lookup"><span data-stu-id="3574e-127">**ASPScriptEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3574e-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-130">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ Scripting \| Enable for ASP »)</span><span class="sxs-lookup"><span data-stu-id="3574e-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Enable for ASP")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-131">Si la **valeur est true**, les scripts WMI peuvent être utilisés sur des Pages de Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="3574e-131">If **True**, WMI scripting can be used on Active Server Pages (ASP).</span></span> <span data-ttu-id="3574e-132">Cette propriété est valide sur les systèmes exécutant des versions de Windows non prises en charge uniquement.</span><span class="sxs-lookup"><span data-stu-id="3574e-132">This property is valid on systems running unsupported versions of Windows only.</span></span> <span data-ttu-id="3574e-133">Pour les systèmes Windows pris en charge, les scripts WMI sont toujours autorisés sur ASP.</span><span class="sxs-lookup"><span data-stu-id="3574e-133">For supported Windows systems, WMI scripting is always allowed on ASP.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-134">**AutorecoverMofs**</span><span class="sxs-lookup"><span data-stu-id="3574e-134">**AutorecoverMofs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-135">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="3574e-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3574e-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-137">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM Microsoft WBEM \\ \\ \| AutoRecover" MOF ")</span><span class="sxs-lookup"><span data-stu-id="3574e-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Autorecover MOFs")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-138">Liste des noms de fichiers MOF complets utilisés pour initialiser ou récupérer l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-138">List of fully qualified MOF file names used to initialize or recover the WMI repository.</span></span> <span data-ttu-id="3574e-139">La liste détermine l’ordre dans lequel les fichiers MOF sont compilés.</span><span class="sxs-lookup"><span data-stu-id="3574e-139">The list determines the order in which MOF files are compiled.</span></span>

<span data-ttu-id="3574e-140">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-140">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-141">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM- \| récupération automatique (MOF** )    </span><span class="sxs-lookup"><span data-stu-id="3574e-141">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Autorecover MOFs**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-142">**AutoStartWin9X**</span><span class="sxs-lookup"><span data-stu-id="3574e-142">**AutoStartWin9X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-145">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X »)</span><span class="sxs-lookup"><span data-stu-id="3574e-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|AutostartWin9X")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-146">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3574e-146">Not supported.</span></span>

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

<span data-ttu-id="3574e-147">**Ne pas démarrer** (0)</span><span class="sxs-lookup"><span data-stu-id="3574e-147">**Don't start** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

<span data-ttu-id="3574e-148">**Démarrage automatique** (1)</span><span class="sxs-lookup"><span data-stu-id="3574e-148">**Autostart** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

<span data-ttu-id="3574e-149">**Démarrer lors du redémarrage** (2)</span><span class="sxs-lookup"><span data-stu-id="3574e-149">**Start on reboot** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3574e-150">**Sauvegarde voulu**</span><span class="sxs-lookup"><span data-stu-id="3574e-150">**BackupInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-153">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Backup intervalle Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="3574e-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-154">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3574e-154">Not supported.</span></span> <span data-ttu-id="3574e-155">Au lieu de cela, sauvegardez manuellement le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-155">Instead, backup the WMI repository manually.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-156">**BackupLastTime**</span><span class="sxs-lookup"><span data-stu-id="3574e-156">**BackupLastTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-157">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3574e-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-159">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Time Functions \| GetTimeZoneInformation")</span><span class="sxs-lookup"><span data-stu-id="3574e-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Functions\|GetTimeZoneInformation")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-160">Date et heure de la dernière sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="3574e-160">Date and time the last backup was performed.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-161">**BuildVersion**</span><span class="sxs-lookup"><span data-stu-id="3574e-161">**BuildVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-164">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Build »)</span><span class="sxs-lookup"><span data-stu-id="3574e-164">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Build")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-165">Informations de version pour le service WMI actuellement installé.</span><span class="sxs-lookup"><span data-stu-id="3574e-165">Version information for the currently installed WMI service.</span></span>

<span data-ttu-id="3574e-166">Durée écoulée entre les sauvegardes de la base de données WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-166">Length of time that elapses between backups of the WMI database.</span></span>

<span data-ttu-id="3574e-167">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-167">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-168">**HKEY \_ \_** \\  \\  \\ **\| Build WBEM** du logiciel de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="3574e-168">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Build**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3574e-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-172">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3574e-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3574e-173">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="3574e-173">Short textual description of the current object.</span></span>

<span data-ttu-id="3574e-174">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3574e-174">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3574e-175">**DatabaseDirectory**</span><span class="sxs-lookup"><span data-stu-id="3574e-175">**DatabaseDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-178">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM le \\ \\ \| Répertoire de référentiel CIMOM »)</span><span class="sxs-lookup"><span data-stu-id="3574e-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Repository Directory")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-179">Chemin d’accès au répertoire qui contient l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-179">Directory path that contains the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-180">**DatabaseMaxSize**</span><span class="sxs-lookup"><span data-stu-id="3574e-180">**DatabaseMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-181">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-183">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| maximum DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilo-octets")</span><span class="sxs-lookup"><span data-stu-id="3574e-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-184">Taille maximale de l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-184">Maximum size of the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-185">**Description**</span><span class="sxs-lookup"><span data-stu-id="3574e-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3574e-188">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="3574e-188">Textual description of the current object.</span></span>

<span data-ttu-id="3574e-189">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3574e-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3574e-190">**EnableAnonWin9xConnections**</span><span class="sxs-lookup"><span data-stu-id="3574e-190">**EnableAnonWin9xConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-191">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3574e-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-193">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections »)</span><span class="sxs-lookup"><span data-stu-id="3574e-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableAnonConnections")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-194">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3574e-194">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-195">**EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="3574e-195">**EnableEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3574e-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-197">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-198">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| « EnableEvents »)</span><span class="sxs-lookup"><span data-stu-id="3574e-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableEvents")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-199">Si la **valeur est true**, le sous-système d’événements WMI doit être activé.</span><span class="sxs-lookup"><span data-stu-id="3574e-199">If **True**, the WMI event subsystem should be enabled.</span></span>

<span data-ttu-id="3574e-200">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-200">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-201">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="3574e-201">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|EnableEvents**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-202">**EnableStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="3574e-202">**EnableStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-203">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3574e-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-204">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-204">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-205">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation »)</span><span class="sxs-lookup"><span data-stu-id="3574e-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableStartupHeapPreallocation")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-206">Si la valeur est **true**, WMI crée un segment de mémoire pré-alloué avec la taille de la valeur **LastStartupHeapPreallocation** lors de l’initialisation de WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-206">If **True**, WMI creates a pre-allocated heap with the size of the **LastStartupHeapPreallocation** value when WMI is initialized.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-207">**HighThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="3574e-207">**HighThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-209">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-210">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| Highst Threshold on client Objects »), [**Units**](../wmisdk/standard-qualifiers.md) (« Objects per second »)</span><span class="sxs-lookup"><span data-stu-id="3574e-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-211">Vitesse maximale à laquelle les objets créés par le fournisseur peuvent être remis aux clients.</span><span class="sxs-lookup"><span data-stu-id="3574e-211">Maximum rate at which provider-created objects can be delivered to clients.</span></span> <span data-ttu-id="3574e-212">Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI conserve les objets dans les files d’attente avant de les transmettre aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="3574e-212">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="3574e-213">Pour plus d’efficacité, les consommateurs doivent collecter les objets à un rythme qui correspond au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3574e-213">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="3574e-214">Si la mémoire détenue par les objets non collectés atteint **LowThresholdOnObjects**, WMI ralentit l’ajout de nouveaux objets dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="3574e-214">If the memory held by uncollected objects reaches **LowThresholdOnObjects**, then WMI slows down the addition of new objects into the queue.</span></span> <span data-ttu-id="3574e-215">Si les événements non collectés continuent à s’accumuler et que la durée maximale de remise des événements dans **MaxWaitOnClientObjects** est atteinte alors que la mémoire utilisée est à la valeur dans **HighThresholdOnClientObjects**, WMI n’accepte aucun autre objet des fournisseurs et retourne la **mémoire WBEM E à la \_ \_ \_ \_ mémoire des** clients.</span><span class="sxs-lookup"><span data-stu-id="3574e-215">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnClientObjects** is reached while the memory used is at the value in **HighThresholdOnClientObjects**, then WMI accepts no more objects from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-216">**HighThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="3574e-216">**HighThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-217">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-218">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-218">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-219">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| High Threshold on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("Events per sec")</span><span class="sxs-lookup"><span data-stu-id="3574e-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-220">Vitesse maximale à laquelle les événements doivent être remis aux clients.</span><span class="sxs-lookup"><span data-stu-id="3574e-220">Maximum rate at which events are to be delivered to clients.</span></span> <span data-ttu-id="3574e-221">Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI met en file d’attente les événements avant de les transmettre aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="3574e-221">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="3574e-222">Pour plus d’efficacité, les consommateurs doivent collecter les événements à un rythme qui correspond au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3574e-222">For more efficiency, consumers must collect the events at a pace that matches the provider.</span></span> <span data-ttu-id="3574e-223">Si la mémoire détenue par les événements non collectés atteint **LowThresholdOnObjects**, WMI ralentit l’ajout de nouveaux événements dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="3574e-223">If the memory held by uncollected events reaches **LowThresholdOnObjects**, then WMI slows down the addition of new events into the queue.</span></span> <span data-ttu-id="3574e-224">Si les événements non collectés continuent à s’accumuler et que la durée maximale de remise des événements dans **MaxWaitOnEvents** est atteinte alors que la mémoire utilisée est à la valeur de **HighThresholdOnEvents**, WMI n’accepte plus d’événements des fournisseurs et retourne la **mémoire WBEM E à la \_ \_ \_ \_ mémoire des** clients.</span><span class="sxs-lookup"><span data-stu-id="3574e-224">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnEvents** is reached while the memory used is at the value in **HighThresholdOnEvents**, WMI accepts no more events from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

> [!Note]  
> <span data-ttu-id="3574e-225">La limitation est effectuée uniquement pour les consommateurs d’événements permanents, de sorte que les consommateurs temporaires ne doivent pas s’attendre à une limitation lorsque les événements sont sauvegardés dans la file d’attente d’événements internes WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-225">Throttling is only done for Permanent Event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="3574e-226">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-226">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-227">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\ **\| seuil supérieur de CIMOM Microsoft WBEM sur les objets clients (B)**    </span><span class="sxs-lookup"><span data-stu-id="3574e-227">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-228">**InstallationDirectory**</span><span class="sxs-lookup"><span data-stu-id="3574e-228">**InstallationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-231">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| installation Directory »)</span><span class="sxs-lookup"><span data-stu-id="3574e-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Installation Directory")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-232">Chemin d’accès au répertoire où le logiciel WMI a été installé.</span><span class="sxs-lookup"><span data-stu-id="3574e-232">Directory path where the WMI software has been installed.</span></span> <span data-ttu-id="3574e-233">L’emplacement par défaut est \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="3574e-233">The default location is \\System32\\Wbem.</span></span>

<span data-ttu-id="3574e-234">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-234">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-235">**HKEY \_ \_** Répertoire d' \\  \\  \\ **\| installation WBEM** du logiciel de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="3574e-235">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Installation Directory**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-236">**LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="3574e-236">**LastStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-237">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-239">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3574e-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-240">Taille du tas pré-alloué créé par WMI pendant l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="3574e-240">Size of the pre-allocated heap created by WMI during initialization.</span></span>

<span data-ttu-id="3574e-241">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-241">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-242">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="3574e-242">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|LastStartupHeapPreallocation**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-243">**LoggingDirectory**</span><span class="sxs-lookup"><span data-stu-id="3574e-243">**LoggingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-245">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-246">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging Directory »)</span><span class="sxs-lookup"><span data-stu-id="3574e-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging Directory")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-247">Chemin d’accès au répertoire qui contient l’emplacement des fichiers journaux système WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-247">Directory path that contains the location of the WMI system log files.</span></span>

<span data-ttu-id="3574e-248">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-248">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-249">**HKEY \_ Logiciel de l' \_ ordinateur local** répertoire de \\  \\  \\ **\| \| journalisation CIMOM Microsoft WBEM**</span><span class="sxs-lookup"><span data-stu-id="3574e-249">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging Directory**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-250">**LoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="3574e-250">**LoggingLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-251">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-252">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-252">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-253">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging »)</span><span class="sxs-lookup"><span data-stu-id="3574e-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-254">L’activation de la journalisation des événements et le niveau de détail de la journalisation utilisé.</span><span class="sxs-lookup"><span data-stu-id="3574e-254">Enabling of event logging and the verbosity level of logging used.</span></span>

<span data-ttu-id="3574e-255">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-255">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-256">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ **\| \| journalisation CIMOM Microsoft WBEM**</span><span class="sxs-lookup"><span data-stu-id="3574e-256">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging**</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="3574e-257">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="3574e-257">**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

<span data-ttu-id="3574e-258">**Journalisation des erreurs** (1)</span><span class="sxs-lookup"><span data-stu-id="3574e-258">**Error logging** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

<span data-ttu-id="3574e-259">**Journalisation des erreurs détaillées** (2)</span><span class="sxs-lookup"><span data-stu-id="3574e-259">**Verbose Error logging** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3574e-260">**LowThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="3574e-260">**LowThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-261">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-262">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-263">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("Objects per sec")</span><span class="sxs-lookup"><span data-stu-id="3574e-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-264">Vitesse à laquelle WMI commence à ralentir la création de nouveaux objets créés pour les clients.</span><span class="sxs-lookup"><span data-stu-id="3574e-264">Rate at which WMI starts to slow the creation of new objects created for clients.</span></span> <span data-ttu-id="3574e-265">Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI conserve les objets dans les files d’attente avant de les transmettre aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="3574e-265">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="3574e-266">Pour plus d’efficacité, les consommateurs doivent collecter les objets à un rythme qui correspond au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3574e-266">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="3574e-267">Si le taux de demandes d’objets atteint **LowThresholdOnClientObjects**, WMI ralentit progressivement la création de nouveaux objets pour correspondre au taux d’utilisation du client.</span><span class="sxs-lookup"><span data-stu-id="3574e-267">If the rate of requests for objects reaches **LowThresholdOnClientObjects**, then WMI gradually slows down the creation of new objects to match the client's rate of use.</span></span> <span data-ttu-id="3574e-268">Ce ralentissement démarre lorsque la vitesse à laquelle les objets sont créés est supérieure à la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="3574e-268">This slowdown starts when the rate at which objects are being created exceeds the value of this property.</span></span> <span data-ttu-id="3574e-269">Consultez **HighThresholdOnClientObjects**.</span><span class="sxs-lookup"><span data-stu-id="3574e-269">See **HighThresholdOnClientObjects**.</span></span>

<span data-ttu-id="3574e-270">Cette propriété reflète la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-270">This property reflects the registry value.</span></span>

<span data-ttu-id="3574e-271">**Clé \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\ **\| seuil supérieur de CIMOM Microsoft WBEM sur les objets clients (B)**    </span><span class="sxs-lookup"><span data-stu-id="3574e-271">**KEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-272">**LowThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="3574e-272">**LowThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-273">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-274">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-274">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-275">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Low Threshold on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("Events per sec")</span><span class="sxs-lookup"><span data-stu-id="3574e-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-276">Vitesse à laquelle WMI commence à ralentir la remise de nouveaux événements.</span><span class="sxs-lookup"><span data-stu-id="3574e-276">Rate at which WMI starts to slow the delivery of new events.</span></span> <span data-ttu-id="3574e-277">Pour prendre en charge les différentiels de vitesse entre les fournisseurs et les clients, WMI met en file d’attente les événements avant de les transmettre aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="3574e-277">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="3574e-278">Pour plus d’efficacité, les consommateurs doivent collecter les objets à un rythme qui correspond au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3574e-278">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="3574e-279">Si la file d’attente augmente le contrôle, les limitations WMI sont ralenties : la remise des événements progressivement pour s’aligner sur le taux du client.</span><span class="sxs-lookup"><span data-stu-id="3574e-279">If the queue grows out of control, WMI throttles—slows down—the delivery of events gradually to align with the client rate.</span></span> <span data-ttu-id="3574e-280">Ce ralentissement démarre lorsque la vitesse à laquelle les événements sont générés dépasse la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="3574e-280">This slowdown starts when the rate at which events are generated exceeds the value of this property.</span></span> <span data-ttu-id="3574e-281">Consultez **HighThresholdOnEvents**.</span><span class="sxs-lookup"><span data-stu-id="3574e-281">See **HighThresholdOnEvents**.</span></span>

> [!Note]  
> <span data-ttu-id="3574e-282">La limitation est effectuée uniquement pour les consommateurs d’événements permanents, de sorte que les consommateurs temporaires ne doivent pas s’attendre à une limitation lorsque les événements sont sauvegardés dans la file d’attente d’événements internes WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-282">Throttling is only done for permanent event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="3574e-283">Cette propriété reflète la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-283">This property reflects the registry value.</span></span>

<span data-ttu-id="3574e-284">**HKEY \_ Logiciel de l' \_ ordinateur local**- \\  \\  \\  \\ **\| seuil supérieur de CIMOM Microsoft WBEM sur les objets clients {B}**    </span><span class="sxs-lookup"><span data-stu-id="3574e-284">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects {B}**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-285">**MaxLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="3574e-285">**MaxLogFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-286">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-287">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-288">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log file Max size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3574e-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-289">Taille maximale des fichiers journaux générés par le service WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-289">Maximum size of the log files produced by the WMI service.</span></span>

<span data-ttu-id="3574e-290">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-290">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-291">**HKEY \_ \_** \\  \\  \\ **\| \| Taille maximale du fichier journal CIMOM Microsoft WBEM** de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="3574e-291">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Log File Max Size**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-292">**MaxWaitOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="3574e-292">**MaxWaitOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-293">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-294">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-294">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-295">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="3574e-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-296">Durée pendant laquelle un objet nouvellement créé attend d’être utilisé par le client avant d’être supprimé et une valeur d’erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="3574e-296">Amount of time a newly created object waits to be used by the client before it is discarded and an error value is returned.</span></span> <span data-ttu-id="3574e-297">Cette propriété interagit avec les propriétés **LowThresholdOnClientObjects** et **HighThresholdOnClientObjects** pour limiter, ralentir, la remise d’objets aux consommateurs lorsque le consommateur reçoit les objets trop lentement.</span><span class="sxs-lookup"><span data-stu-id="3574e-297">This property interacts with the **LowThresholdOnClientObjects** and **HighThresholdOnClientObjects** properties to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

</dd> <dt>

<span data-ttu-id="3574e-298">**MaxWaitOnEvents**</span><span class="sxs-lookup"><span data-stu-id="3574e-298">**MaxWaitOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-299">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3574e-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-300">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3574e-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3574e-301">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max Wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="3574e-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-302">Durée pendant laquelle un événement envoyé à un client est mis en file d’attente avant d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="3574e-302">Amount of time for which an event sent to a client is queued before being discarded.</span></span> <span data-ttu-id="3574e-303">Cette propriété interacts0 avec **LowThresholdOnEvents** et **HighThresholdOnEvents** pour limiter, ralentir, la remise d’objets aux consommateurs lorsque le consommateur reçoit les objets trop lentement.</span><span class="sxs-lookup"><span data-stu-id="3574e-303">This property interacts0 with **LowThresholdOnEvents** and **HighThresholdOnEvents** to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

<span data-ttu-id="3574e-304">Cette propriété reflète la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-304">This property reflects the registry value.</span></span>

<span data-ttu-id="3574e-305">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max Wait sur événements (MS)**    </span><span class="sxs-lookup"><span data-stu-id="3574e-305">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Max Wait On Events (ms)**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-306">**MofSelfInstallDirectory**</span><span class="sxs-lookup"><span data-stu-id="3574e-306">**MofSelfInstallDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-309">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory »)</span><span class="sxs-lookup"><span data-stu-id="3574e-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|MOF Self-Install Directory")</span></span>
</dt> </dl>

<span data-ttu-id="3574e-310">Chemin d’accès au répertoire des applications qui installent les fichiers MOF dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-310">Directory path for applications that install MOF files to the WMI repository.</span></span> <span data-ttu-id="3574e-311">WMI compile automatiquement tous les fichiers MOF placés dans ce répertoire et, en fonction de sa réussite, déplace le fichier MOF vers un sous-répertoire intitulé Good ou Bad.</span><span class="sxs-lookup"><span data-stu-id="3574e-311">WMI automatically compiles any MOF files placed in this directory and, depending on its success, moves the MOF to a subdirectory labeled good or bad.</span></span> <span data-ttu-id="3574e-312">Si la \# commande [pragma autoautorecover](../wmisdk/pragma-autorecover.md) est incluse, le nom de fichier complet est ajouté à la liste **AutorecoverMofs** utilisée lors de l’initialisation ou de la récupération du référentiel par WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-312">If the \# [pragma autorecover](../wmisdk/pragma-autorecover.md) command is included, the fully qualified file name is added to the **AutorecoverMofs** list used when WMI is initializing or recovering the repository.</span></span> <span data-ttu-id="3574e-313">La liste détermine l’ordre dans lequel les MOF sont compilés.</span><span class="sxs-lookup"><span data-stu-id="3574e-313">The list determines the order in which MOFs are compiled.</span></span>

<span data-ttu-id="3574e-314">Cette propriété reflète la valeur dans la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="3574e-314">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="3574e-315">**HKEY \_ \_Ordinateur local** \\ **logiciel** \\ **Microsoft** \\ **WBEM \| CIMOM \| fichier MOF-répertoire d’installation**</span><span class="sxs-lookup"><span data-stu-id="3574e-315">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|MOF Self=Install Directory**</span></span>

</dd> <dt>

<span data-ttu-id="3574e-316">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="3574e-316">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3574e-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3574e-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3574e-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3574e-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3574e-319">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3574e-319">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3574e-320">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="3574e-320">Identifier by which the current object is known.</span></span>

<span data-ttu-id="3574e-321">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3574e-321">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3574e-322">Notes</span><span class="sxs-lookup"><span data-stu-id="3574e-322">Remarks</span></span>

<span data-ttu-id="3574e-323">La classe **Win32 \_ WMISetting** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3574e-323">The **Win32\_WMISetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span> <span data-ttu-id="3574e-324">Une seule instance de cette classe peut exister sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3574e-324">Only one instance of this class can exist on a computer.</span></span>

<span data-ttu-id="3574e-325">Il peut être très utile de savoir comment WMI est configuré sur un ordinateur pour déboguer des scripts ou résoudre des problèmes liés au service WMI lui-même.</span><span class="sxs-lookup"><span data-stu-id="3574e-325">Knowing how WMI is configured on a computer can be very useful when you are debugging scripts or troubleshooting problems with the WMI service itself.</span></span> <span data-ttu-id="3574e-326">Par exemple, de nombreux scripts WMI sont écrits en supposant que \\ la racine cimv2 est l’espace de noms par défaut sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="3574e-326">For example, many WMI scripts are written under the assumption that root\\cimv2 is the default namespace on the target computer.</span></span> <span data-ttu-id="3574e-327">Par conséquent, les writers de script qui ont besoin d’accéder à une classe dans « root \\ cimv2 » ne parviennent souvent pas à inclure l’espace de noms dans le moniker GetObject, comme illustré dans l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="3574e-327">As a result, script writers who need to access a class in "Root\\CIMv2" often fail to include the namespace in the GetObject moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

<span data-ttu-id="3574e-328">Si la racine \\ cimv2 n’est pas l’espace de noms par défaut sur l’ordinateur cible, ce script échouera.</span><span class="sxs-lookup"><span data-stu-id="3574e-328">If root\\cimv2 is not the default namespace on the target computer, this script will fail.</span></span> <span data-ttu-id="3574e-329">Pour éviter ce problème, l’espace de noms racine \\ cimv2 doit être inclus dans le moniker, comme illustré dans l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="3574e-329">To prevent this from happening, the namespace root\\cimv2 must be included in the moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

<span data-ttu-id="3574e-330">Si l’espace de noms par défaut sur l’ordinateur cible est différent de l’espace de noms utilisé par un script, le script échoue.</span><span class="sxs-lookup"><span data-stu-id="3574e-330">If the default namespace on the target computer is different from the namespace assumed by a script, the script will fail.</span></span> <span data-ttu-id="3574e-331">En plus de cela, l’utilisateur recevra le message d’erreur de type « classe non valide ».</span><span class="sxs-lookup"><span data-stu-id="3574e-331">On top of that, the user will be presented with the somewhat misleading error message "Invalid class."</span></span> <span data-ttu-id="3574e-332">En vérité, l’échec n’est pas dû au fait que la classe n’est pas valide mais que la classe est introuvable dans l’espace de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="3574e-332">In truth, the failure is not because the class is invalid but because the class cannot be found in the default namespace.</span></span> <span data-ttu-id="3574e-333">Il s’agit d’un problème difficile à résoudre, car vous devrez peut-être examiner les problèmes potentiels de la classe plutôt que des problèmes avec l’espace de noms (ou, dans le cas contraire, was) spécifié.</span><span class="sxs-lookup"><span data-stu-id="3574e-333">This is a difficult problem to troubleshoot, because you are likely to investigate possible problems with the class rather than problems with the namespace that was (or, in this case, was not) specified.</span></span>

<span data-ttu-id="3574e-334">Vous pouvez utiliser la classe **Win32 \_ WMISetting** pour déterminer le mode de configuration de WMI sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3574e-334">You can use the **Win32\_WMISetting** class to determine how WMI has been configured on a computer.</span></span> <span data-ttu-id="3574e-335">Des détails de configuration tels que l’espace de noms par défaut ou le numéro de build WMI peuvent être utiles pour résoudre les problèmes de script.</span><span class="sxs-lookup"><span data-stu-id="3574e-335">Configuration details such as the default namespace or the WMI build number can be useful in troubleshooting script problems.</span></span> <span data-ttu-id="3574e-336">Ces paramètres fournissent également des informations d’administration importantes, telles que la façon dont les erreurs WMI sont journalisées ou même si elles sont enregistrées sur un ordinateur et les fournisseurs WMI qui seront rechargés automatiquement si vous devez reconstruire le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-336">These settings also provide important administrative information such as how, or even whether, WMI errors are logged on a computer and which WMI providers will automatically be reloaded if you need to rebuild the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="3574e-337">Exemples</span><span class="sxs-lookup"><span data-stu-id="3574e-337">Examples</span></span>

<span data-ttu-id="3574e-338">L’exemple de code [modifier les paramètres WMI](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript dans la Galerie TechNet utilise la classe **Win32 \_ WMISetting** pour configurer l’intervalle de sauvegarde et le niveau de journalisation WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-338">The [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to configure the WMI backup interval and logging level.</span></span>

<span data-ttu-id="3574e-339">La liste de l’exemple de code VBScript de l' [espace de noms par défaut](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) sur la Galerie TechNet utilise la classe **Win32 \_ WMISetting** pour récupérer et afficher le paramètre WMI « espace de noms par défaut pour les scripts » WMI actuel.</span><span class="sxs-lookup"><span data-stu-id="3574e-339">The [List the Default Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to retrieve and display the current WMI "Default namespace for scripting" setting.</span></span>

<span data-ttu-id="3574e-340">La modification de l’exemple de code VBScript de l' [espace de noms WMI par défaut](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) dans la Galerie TechNet utilise la propriété **ASPScriptDefaultNamespace** pour définir le paramètre WMI « espace de noms par défaut pour les scripts » sur « root \\ cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="3574e-340">The [Modify the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript code example on the TechNet Gallery uses the **ASPScriptDefaultNamespace** property to set the WMI "Default namespace for scripting" setting to "root\\cimv2".</span></span>

<span data-ttu-id="3574e-341">L’exemple de code VBScript de la [liste tous les paramètres WMI](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste des paramètres WMI configurés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3574e-341">The [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="3574e-342">L’exemple de code JavaScript liste des informations sur les [paramètres WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste des paramètres WMI configurés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3574e-342">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="3574e-343">L’exemple de code de la [liste des informations de paramètres WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste des paramètres WMI configurés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3574e-343">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Python code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="3574e-344">L’exemple de code de l’objet de liste de paramètres [WMI](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) REXX utilise un certain nombre de propriétés sur **Win32 \_ WMISetting** pour retourner une liste des paramètres WMI configurés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3574e-344">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="3574e-345">L’exemple de code VBScript suivant montre comment obtenir la version de WMI en cours d’exécution sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3574e-345">The following VBScript code example shows how to obtain the version of WMI running on the local computer.</span></span> <span data-ttu-id="3574e-346">« Win32 \_ WMISetting = @ » indique l’instance unique de la classe.</span><span class="sxs-lookup"><span data-stu-id="3574e-346">The "Win32\_WMISetting=@" indicates the single instance of the class.</span></span> <span data-ttu-id="3574e-347">Pour plus d’informations, consultez versions de WMI.</span><span class="sxs-lookup"><span data-stu-id="3574e-347">For more information, see WMI versions.</span></span>


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a><span data-ttu-id="3574e-348">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3574e-348">Requirements</span></span>



| <span data-ttu-id="3574e-349">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3574e-349">Requirement</span></span> | <span data-ttu-id="3574e-350">Valeur</span><span class="sxs-lookup"><span data-stu-id="3574e-350">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3574e-351">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3574e-351">Minimum supported client</span></span><br/> | <span data-ttu-id="3574e-352">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3574e-352">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3574e-353">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3574e-353">Minimum supported server</span></span><br/> | <span data-ttu-id="3574e-354">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3574e-354">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3574e-355">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3574e-355">Namespace</span></span><br/>                | <span data-ttu-id="3574e-356">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3574e-356">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3574e-357">MOF</span><span class="sxs-lookup"><span data-stu-id="3574e-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3574e-358"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3574e-358"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3574e-359">DLL</span><span class="sxs-lookup"><span data-stu-id="3574e-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3574e-360"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3574e-360"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3574e-361">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3574e-361">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3574e-362">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="3574e-362">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="3574e-363">Classes de gestion des services WMI</span><span class="sxs-lookup"><span data-stu-id="3574e-363">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
