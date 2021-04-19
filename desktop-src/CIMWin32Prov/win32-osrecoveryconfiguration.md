---
description: Le \_ OSRecoveryConfiguration Win32&\# 8194 ; La classe WMI représente les types d’informations qui seront collectées à partir de la mémoire en cas d’échec du système d’exploitation. Cela comprend les échecs de démarrage et les pannes du système.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Classe Win32_OSRecoveryConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2371ba7ee449497e2d695e60d75c59454282d54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517200"
---
# <a name="win32_osrecoveryconfiguration-class"></a><span data-ttu-id="068ee-104">\_Classe OSRecoveryConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="068ee-104">Win32\_OSRecoveryConfiguration class</span></span>

<span data-ttu-id="068ee-105">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OSRecoveryConfiguration** WMI représente les types d’informations qui seront collectées à partir de la mémoire en cas d’échec du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="068ee-105">The **Win32\_OSRecoveryConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the types of information that will be gathered from memory when the operating system fails.</span></span> <span data-ttu-id="068ee-106">Cela comprend les échecs de démarrage et les pannes du système.</span><span class="sxs-lookup"><span data-stu-id="068ee-106">This includes boot failures and system crashes.</span></span>

<span data-ttu-id="068ee-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="068ee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="068ee-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="068ee-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="068ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="068ee-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="068ee-110">Membres</span><span class="sxs-lookup"><span data-stu-id="068ee-110">Members</span></span>

<span data-ttu-id="068ee-111">La classe **Win32 \_ OSRecoveryConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="068ee-111">The **Win32\_OSRecoveryConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="068ee-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="068ee-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="068ee-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="068ee-113">Properties</span></span>

<span data-ttu-id="068ee-114">La classe **Win32 \_ OSRecoveryConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="068ee-114">The **Win32\_OSRecoveryConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="068ee-115">**Redémarrage**</span><span class="sxs-lookup"><span data-stu-id="068ee-115">**AutoReboot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="068ee-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-118">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| reboot")</span><span class="sxs-lookup"><span data-stu-id="068ee-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-119">Le système redémarre automatiquement au cours d’une opération de récupération.</span><span class="sxs-lookup"><span data-stu-id="068ee-119">System will automatically reboot during a recovery operation.</span></span>

</dd> <dt>

<span data-ttu-id="068ee-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="068ee-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="068ee-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068ee-123">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="068ee-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="068ee-124">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="068ee-124">Short textual description of the current object.</span></span>

<span data-ttu-id="068ee-125">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="068ee-125">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="068ee-126">**DebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="068ee-126">**DebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-129">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| dumpfile")</span><span class="sxs-lookup"><span data-stu-id="068ee-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|DumpFile")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-130">Chemin d’accès complet au fichier de débogage.</span><span class="sxs-lookup"><span data-stu-id="068ee-130">Full path to the debug file.</span></span> <span data-ttu-id="068ee-131">Un fichier de débogage est créé avec l’état de la mémoire de l’ordinateur après une défaillance de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="068ee-131">A debug file is created with the memory state of the computer after a computer failure.</span></span>

<span data-ttu-id="068ee-132">Exemple : « C : \\ Windows \\ Memory. dmp »</span><span class="sxs-lookup"><span data-stu-id="068ee-132">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="068ee-133">**DebugInfoType**</span><span class="sxs-lookup"><span data-stu-id="068ee-133">**DebugInfoType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="068ee-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="068ee-136">Type d’informations de débogage écrites dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="068ee-136">Type of debugging information written to the log file.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="068ee-137">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="068ee-137">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

<span data-ttu-id="068ee-138">**Image mémoire complète** (1)</span><span class="sxs-lookup"><span data-stu-id="068ee-138">**Complete memory dump** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

<span data-ttu-id="068ee-139">**Image mémoire du noyau** (2)</span><span class="sxs-lookup"><span data-stu-id="068ee-139">**Kernel memory dump** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

<span data-ttu-id="068ee-140">**Image mémoire réduite** (3)</span><span class="sxs-lookup"><span data-stu-id="068ee-140">**Small memory dump** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="068ee-141">**Description**</span><span class="sxs-lookup"><span data-stu-id="068ee-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="068ee-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="068ee-144">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="068ee-144">Textual description of the current object.</span></span>

<span data-ttu-id="068ee-145">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="068ee-145">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="068ee-146">**ExpandedDebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="068ee-146">**ExpandedDebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="068ee-149">Version développée de la propriété **DebugFilePath** .</span><span class="sxs-lookup"><span data-stu-id="068ee-149">Expanded version of the **DebugFilePath** property.</span></span>

<span data-ttu-id="068ee-150">Exemple : « C : \\ Windows \\ Memory. dmp »</span><span class="sxs-lookup"><span data-stu-id="068ee-150">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="068ee-151">**ExpandedMiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="068ee-151">**ExpandedMiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="068ee-154">Version développée de la propriété **MiniDumpDirectory** .</span><span class="sxs-lookup"><span data-stu-id="068ee-154">Expanded version of the **MiniDumpDirectory** property.</span></span>

<span data-ttu-id="068ee-155">Exemple : « C : \\ \\ Minidump Windows »</span><span class="sxs-lookup"><span data-stu-id="068ee-155">Example: "C:\\Windows\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="068ee-156">**KernelDumpOnly**</span><span class="sxs-lookup"><span data-stu-id="068ee-156">**KernelDumpOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-157">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="068ee-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-159">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| KernelDumpOnly")</span><span class="sxs-lookup"><span data-stu-id="068ee-159">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|KernelDumpOnly")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-160">Seules les informations de débogage du noyau sont écrites dans le fichier journal de débogage.</span><span class="sxs-lookup"><span data-stu-id="068ee-160">Only kernel debug information will be written to the debug log file.</span></span> <span data-ttu-id="068ee-161">Si la **valeur est true**, seul l’état du noyau est écrit dans un fichier en cas de défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="068ee-161">If **TRUE**, then only the state of the kernel is written to a file in the event of a system failure.</span></span> <span data-ttu-id="068ee-162">Si la **valeur est false**, le système tente d’enregistrer l’état de la mémoire et tous les appareils qui peuvent fournir des informations sur le système en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="068ee-162">If **FALSE**, the system will try to log the state of the memory, and any devices that can provide information about the system when it failed.</span></span>

</dd> <dt>

<span data-ttu-id="068ee-163">**MiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="068ee-163">**MiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-166">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| MiniDumpDir")</span><span class="sxs-lookup"><span data-stu-id="068ee-166">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|MiniDumpDir")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-167">Répertoire où les petits fichiers de vidage de mémoire seront enregistrés et accumulés.</span><span class="sxs-lookup"><span data-stu-id="068ee-167">Directory where small memory dump files will be recorded and accumulated.</span></span>

<span data-ttu-id="068ee-168">Exemple : « % systemRoot% \\ minidump »</span><span class="sxs-lookup"><span data-stu-id="068ee-168">Example: "%systemRoot%\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="068ee-169">**Nom**</span><span class="sxs-lookup"><span data-stu-id="068ee-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="068ee-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068ee-172">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="068ee-172">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-173">Nom identifiant cette instance de la **classe \_ OSRecoveryConfiguration Win32** .</span><span class="sxs-lookup"><span data-stu-id="068ee-173">Identifying name for this instance of the **Win32\_OSRecoveryConfiguration** class.</span></span>

</dd> <dt>

<span data-ttu-id="068ee-174">**OverwriteExistingDebugFile**</span><span class="sxs-lookup"><span data-stu-id="068ee-174">**OverwriteExistingDebugFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-175">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="068ee-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-176">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-177">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| overwrite")</span><span class="sxs-lookup"><span data-stu-id="068ee-177">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|Overwrite")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-178">Le nouveau fichier de débogage remplace un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="068ee-178">New debug file will overwrite an existing one.</span></span>

</dd> <dt>

<span data-ttu-id="068ee-179">**SendAdminAlert**</span><span class="sxs-lookup"><span data-stu-id="068ee-179">**SendAdminAlert**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="068ee-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-182">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| SendAlert")</span><span class="sxs-lookup"><span data-stu-id="068ee-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|SendAlert")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-183">Le message d’alerte sera envoyé à l’administrateur système en cas de défaillance du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="068ee-183">Alert message will be sent to the system administrator in the event of an operating system failure.</span></span>

</dd> <dt>

<span data-ttu-id="068ee-184">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="068ee-184">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="068ee-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="068ee-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="068ee-187">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="068ee-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="068ee-188">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="068ee-188">Identifier by which the current object is known.</span></span>

<span data-ttu-id="068ee-189">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="068ee-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="068ee-190">**WriteDebugInfo**</span><span class="sxs-lookup"><span data-stu-id="068ee-190">**WriteDebugInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-191">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="068ee-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-193">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| CrashDumpEnabled")</span><span class="sxs-lookup"><span data-stu-id="068ee-193">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|CrashDumpEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-194">Les informations de débogage doivent être écrites dans un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="068ee-194">Debugging information is to be written to a log file.</span></span>

</dd> <dt>

<span data-ttu-id="068ee-195">**WriteToSystemLog**</span><span class="sxs-lookup"><span data-stu-id="068ee-195">**WriteToSystemLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="068ee-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="068ee-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="068ee-197">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="068ee-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="068ee-198">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent")</span><span class="sxs-lookup"><span data-stu-id="068ee-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|LogEvent")</span></span>
</dt> </dl>

<span data-ttu-id="068ee-199">Les événements seront écrits dans un journal système.</span><span class="sxs-lookup"><span data-stu-id="068ee-199">Events will be written to a system log.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="068ee-200">Notes</span><span class="sxs-lookup"><span data-stu-id="068ee-200">Remarks</span></span>

<span data-ttu-id="068ee-201">La classe **Win32 \_ OSRecoveryConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="068ee-201">The **Win32\_OSRecoveryConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="068ee-202">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="068ee-202">Requirements</span></span>



| <span data-ttu-id="068ee-203">Condition requise</span><span class="sxs-lookup"><span data-stu-id="068ee-203">Requirement</span></span> | <span data-ttu-id="068ee-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="068ee-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="068ee-205">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="068ee-205">Minimum supported client</span></span><br/> | <span data-ttu-id="068ee-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="068ee-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="068ee-207">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="068ee-207">Minimum supported server</span></span><br/> | <span data-ttu-id="068ee-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="068ee-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="068ee-209">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="068ee-209">Namespace</span></span><br/>                | <span data-ttu-id="068ee-210">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="068ee-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="068ee-211">MOF</span><span class="sxs-lookup"><span data-stu-id="068ee-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="068ee-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="068ee-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="068ee-213">DLL</span><span class="sxs-lookup"><span data-stu-id="068ee-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="068ee-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="068ee-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068ee-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="068ee-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068ee-216">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="068ee-216">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="068ee-217">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="068ee-217">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
