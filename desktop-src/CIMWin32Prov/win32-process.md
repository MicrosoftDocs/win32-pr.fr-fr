---
Description: Le \_ processus Win32&\# 32 ; La classe WMI représente un processus sur un système d’exploitation.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Win32_Process, classe
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525221"
---
# <a name="win32_process-class"></a><span data-ttu-id="93ff1-103">\_Classe de processus Win32</span><span class="sxs-lookup"><span data-stu-id="93ff1-103">Win32\_Process class</span></span>

<span data-ttu-id="93ff1-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ processus Win32** représente un processus sur un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="93ff1-104">The **Win32\_Process** [WMI class](../wmisdk/retrieving-a-class.md) represents a process on an operating system.</span></span>

<span data-ttu-id="93ff1-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="93ff1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

> [!NOTE]
> <span data-ttu-id="93ff1-106">Pour une discussion générale sur les processus et les threads dans Windows, consultez la rubrique [processus et threads](/ProcThread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-106">For a general discussion on Processes and Threads within Windows, please see the topic [Processes and Threads](/ProcThread/processes-and-threads.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="93ff1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93ff1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a><span data-ttu-id="93ff1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="93ff1-108">Members</span></span>

<span data-ttu-id="93ff1-109">La classe de **\_ processus Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="93ff1-109">The **Win32\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="93ff1-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="93ff1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="93ff1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93ff1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="93ff1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="93ff1-112">Methods</span></span>

<span data-ttu-id="93ff1-113">La classe de **\_ processus Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="93ff1-113">The **Win32\_Process** class has these methods.</span></span>



| <span data-ttu-id="93ff1-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="93ff1-114">Method</span></span>                                                                   | <span data-ttu-id="93ff1-115">Description</span><span class="sxs-lookup"><span data-stu-id="93ff1-115">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93ff1-116">**AttachDebugger**</span><span class="sxs-lookup"><span data-stu-id="93ff1-116">**AttachDebugger**</span></span>](attachdebugger-method-in-class-win32-process.md)   | <span data-ttu-id="93ff1-117">Lance le débogueur actuellement inscrit pour un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-117">Launches the currently registered debugger for a process.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="93ff1-118">**Créés**</span><span class="sxs-lookup"><span data-stu-id="93ff1-118">**Create**</span></span>](create-method-in-class-win32-process.md)                   | <span data-ttu-id="93ff1-119">Crée un nouveau processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-119">Creates a new process.</span></span><br/>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="93ff1-120">**GetAvailableVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="93ff1-120">**GetAvailableVirtualSize**</span></span>](getavailablevirtualsize-win32-process.md) | <span data-ttu-id="93ff1-121">Récupère la taille actuelle, en octets, de l’espace d’adressage virtuel libre disponible pour le processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-121">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span><br/> <span data-ttu-id="93ff1-122">**Windows server 2012, Windows 8, Windows 7, Windows server 2008 et Windows Vista :** Cette méthode n’est pas prise en charge avant Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="93ff1-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 and Windows Vista:** This method is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="93ff1-123">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="93ff1-123">**GetOwner**</span></span>](getowner-method-in-class-win32-process.md)               | <span data-ttu-id="93ff1-124">Récupère le nom d’utilisateur et le nom de domaine sous lesquels le processus s’exécute.</span><span class="sxs-lookup"><span data-stu-id="93ff1-124">Retrieves the user name and domain name under which the process is running.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="93ff1-125">**GetOwnerSid**</span><span class="sxs-lookup"><span data-stu-id="93ff1-125">**GetOwnerSid**</span></span>](getownersid-method-in-class-win32-process.md)         | <span data-ttu-id="93ff1-126">Récupère l’identificateur de sécurité (SID) pour le propriétaire d’un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-126">Retrieves the security identifier (SID) for the owner of a process.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="93ff1-127">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="93ff1-127">**SetPriority**</span></span>](setpriority-method-in-class-win32-process.md)         | <span data-ttu-id="93ff1-128">Modifie la priorité d’exécution d’un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-128">Changes the execution priority of a process.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="93ff1-129">**Terminate**</span><span class="sxs-lookup"><span data-stu-id="93ff1-129">**Terminate**</span></span>](terminate-method-in-class-win32-process.md)             | <span data-ttu-id="93ff1-130">Met fin à un processus et à tous ses threads.</span><span class="sxs-lookup"><span data-stu-id="93ff1-130">Terminates a process and all of its threads.</span></span><br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="93ff1-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93ff1-131">Properties</span></span>

<span data-ttu-id="93ff1-132">La classe de **\_ processus Win32** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="93ff1-132">The **Win32\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93ff1-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="93ff1-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-136">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-136">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-137">Description succincte d’un objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="93ff1-137">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="93ff1-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-139">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="93ff1-139">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-142">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« ligne de commande pour démarrer le processus »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-142">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Command Line To Start Process")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-143">Ligne de commande utilisée pour démarrer un processus spécifique, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="93ff1-143">Command line used to start a specific process, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-144">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93ff1-144">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-147">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="93ff1-147">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-148">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="93ff1-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="93ff1-149">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="93ff1-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="93ff1-150">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-150">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-151">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="93ff1-151">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-152">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93ff1-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-154">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span><span class="sxs-lookup"><span data-stu-id="93ff1-154">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-155">Date à laquelle le processus commence à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="93ff1-155">Date the process begins executing.</span></span>

<span data-ttu-id="93ff1-156">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-156">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-157">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93ff1-157">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-160">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="93ff1-160">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-161">Nom de la classe de création du système d’étendue de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="93ff1-161">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="93ff1-162">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-162">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-163">**CSName**</span><span class="sxs-lookup"><span data-stu-id="93ff1-163">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-166">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="93ff1-166">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-167">Nom du système informatique d’étendue.</span><span class="sxs-lookup"><span data-stu-id="93ff1-167">Name of the scoping computer system.</span></span>

<span data-ttu-id="93ff1-168">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-168">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-169">**Description**</span><span class="sxs-lookup"><span data-stu-id="93ff1-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-172">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="93ff1-172">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-173">Description d’un objet.</span><span class="sxs-lookup"><span data-stu-id="93ff1-173">Description of an object.</span></span>

<span data-ttu-id="93ff1-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-175">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="93ff1-175">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-178">Qualificateurs : [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Tool Help structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("exécutable path")</span><span class="sxs-lookup"><span data-stu-id="93ff1-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)\|szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Executable Path")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-179">Chemin d’accès au fichier exécutable du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-179">Path to the executable file of the process.</span></span>

<span data-ttu-id="93ff1-180">Exemple : « C : \\ \\ système Windows \\Explorer.Exe »</span><span class="sxs-lookup"><span data-stu-id="93ff1-180">Example: "C:\\Windows\\System\\Explorer.Exe"</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-181">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="93ff1-181">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93ff1-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-184">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« état d’exécution »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-185">État de fonctionnement actuel du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-185">Current operating condition of the process.</span></span>

<span data-ttu-id="93ff1-186">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-186">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93ff1-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="93ff1-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="93ff1-188">Unknown</span><span class="sxs-lookup"><span data-stu-id="93ff1-188">Unknown</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93ff1-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="93ff1-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="93ff1-190">Autres</span><span class="sxs-lookup"><span data-stu-id="93ff1-190">Other</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="93ff1-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Prêt** (2)</span><span class="sxs-lookup"><span data-stu-id="93ff1-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="93ff1-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="93ff1-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="93ff1-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqué** (4)</span><span class="sxs-lookup"><span data-stu-id="93ff1-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93ff1-194">Bloqué</span><span class="sxs-lookup"><span data-stu-id="93ff1-194">Blocked</span></span>

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="93ff1-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspendu bloqué** (5)</span><span class="sxs-lookup"><span data-stu-id="93ff1-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="93ff1-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspendu prêt** (6)</span><span class="sxs-lookup"><span data-stu-id="93ff1-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="93ff1-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminé** (7)</span><span class="sxs-lookup"><span data-stu-id="93ff1-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="93ff1-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (8)</span><span class="sxs-lookup"><span data-stu-id="93ff1-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="93ff1-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Développement** (9)</span><span class="sxs-lookup"><span data-stu-id="93ff1-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93ff1-200">**Handle**</span><span class="sxs-lookup"><span data-stu-id="93ff1-200">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-203">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« handle »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-203">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-204">Identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-204">Process identifier.</span></span>

<span data-ttu-id="93ff1-205">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-205">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-206">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-206">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-207">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-209">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("handle Count")</span><span class="sxs-lookup"><span data-stu-id="93ff1-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-210">Nombre total de handles ouverts détenus par le processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-210">Total number of open handles owned by the process.</span></span> <span data-ttu-id="93ff1-211">**HandleCount** est la somme des handles actuellement ouverts par chaque thread dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-211">**HandleCount** is the sum of the handles currently open by each thread in this process.</span></span> <span data-ttu-id="93ff1-212">Un descripteur est utilisé pour examiner ou modifier les ressources système.</span><span class="sxs-lookup"><span data-stu-id="93ff1-212">A handle is used to examine or modify the system resources.</span></span> <span data-ttu-id="93ff1-213">Chaque descripteur a une entrée dans une table qui est gérée en interne.</span><span class="sxs-lookup"><span data-stu-id="93ff1-213">Each handle has an entry in a table that is maintained internally.</span></span> <span data-ttu-id="93ff1-214">Les entrées contiennent les adresses des ressources et des données pour identifier le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="93ff1-214">Entries contain the addresses of the resources and data to identify the resource type.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93ff1-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-216">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93ff1-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-218">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="93ff1-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-219">Date d’installation d’un objet.</span><span class="sxs-lookup"><span data-stu-id="93ff1-219">Date an object is installed.</span></span> <span data-ttu-id="93ff1-220">L’objet peut être installé sans qu’une valeur ne soit écrite dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="93ff1-220">The object may be installed without a value being written to this property.</span></span>

<span data-ttu-id="93ff1-221">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-222">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="93ff1-222">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-223">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-225">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="93ff1-225">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-226">Temps en mode noyau, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="93ff1-226">Time in kernel mode, in milliseconds.</span></span> <span data-ttu-id="93ff1-227">Si ces informations ne sont pas disponibles, utilisez la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="93ff1-227">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="93ff1-228">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-228">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-229">**MaximumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="93ff1-229">**MaximumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-230">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-232">Qualificateurs : [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| winnt. H \| limites de quota \_ \| MaximumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" taille maximale de la plage de travail "), [**unités**](../wmisdk/standard-qualifiers.md) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="93ff1-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Maximum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-233">Taille maximale du jeu de travail du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-233">Maximum working set size of the process.</span></span> <span data-ttu-id="93ff1-234">La plage de travail d’un processus correspond à l’ensemble des pages mémoire visibles par le processus dans la mémoire RAM physique.</span><span class="sxs-lookup"><span data-stu-id="93ff1-234">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="93ff1-235">Ces pages sont résidentes et peuvent être utilisées par une application sans déclencher une erreur de page.</span><span class="sxs-lookup"><span data-stu-id="93ff1-235">These pages are resident, and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="93ff1-236">Exemple : 1413120</span><span class="sxs-lookup"><span data-stu-id="93ff1-236">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-237">**MinimumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="93ff1-237">**MinimumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-238">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-238">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-240">Qualificateurs : [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| winnt. H \| limites de quota \_ \| MinimumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" taille minimale du jeu de travail "), [**unités**](../wmisdk/standard-qualifiers.md) (" kilo-octets ")</span><span class="sxs-lookup"><span data-stu-id="93ff1-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Minimum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-241">Taille minimale du jeu de travail du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-241">Minimum working set size of the process.</span></span> <span data-ttu-id="93ff1-242">La plage de travail d’un processus correspond à l’ensemble des pages mémoire visibles par le processus dans la mémoire RAM physique.</span><span class="sxs-lookup"><span data-stu-id="93ff1-242">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="93ff1-243">Ces pages résident et peuvent être utilisées par une application sans déclencher de défaillance de page.</span><span class="sxs-lookup"><span data-stu-id="93ff1-243">These pages are resident and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="93ff1-244">Exemple : 20480</span><span class="sxs-lookup"><span data-stu-id="93ff1-244">Example: 20480</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-245">**Nom**</span><span class="sxs-lookup"><span data-stu-id="93ff1-245">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-248">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="93ff1-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-249">Nom du fichier exécutable responsable du processus, équivalent à la propriété nom de l’image dans le gestionnaire des tâches.</span><span class="sxs-lookup"><span data-stu-id="93ff1-249">Name of the executable file responsible for the process, equivalent to the Image Name property in Task Manager.</span></span>

<span data-ttu-id="93ff1-250">Lorsqu’elle est héritée par une sous-classe, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="93ff1-250">When inherited by a subclass, the property can be overridden to be a key property.</span></span> <span data-ttu-id="93ff1-251">Le nom est codé en dur dans l’application elle-même et n’est pas affecté par la modification du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="93ff1-251">The name is hard-coded into the application itself and is not affected by changing the file name.</span></span> <span data-ttu-id="93ff1-252">Par exemple, même si vous renommez Calc.exe, le nom Calc.exe apparaîtra toujours dans le gestionnaire des tâches et dans tous les scripts WMI qui récupèrent le nom du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-252">For example, even if you rename Calc.exe, the name Calc.exe will still appear in Task Manager and in any WMI scripts that retrieve the process name.</span></span>

<span data-ttu-id="93ff1-253">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-254">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93ff1-254">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-257">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom de la classe du système d’exploitation ")</span><span class="sxs-lookup"><span data-stu-id="93ff1-257">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-258">Nom de la classe de création du système d’exploitation d’étendue.</span><span class="sxs-lookup"><span data-stu-id="93ff1-258">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="93ff1-259">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-259">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-260">**OSName**</span><span class="sxs-lookup"><span data-stu-id="93ff1-260">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-263">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système d’exploitation ")</span><span class="sxs-lookup"><span data-stu-id="93ff1-263">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-264">Nom du système d’exploitation de portée.</span><span class="sxs-lookup"><span data-stu-id="93ff1-264">Name of the scoping operating system.</span></span>

<span data-ttu-id="93ff1-265">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-265">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-266">**OtherOperationCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-266">**OtherOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-267">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-269">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span><span class="sxs-lookup"><span data-stu-id="93ff1-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-270">Nombre d’opérations d’e/s effectuées qui ne sont pas des opérations de lecture ou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="93ff1-270">Number of I/O operations performed that are not read or write operations.</span></span>

<span data-ttu-id="93ff1-271">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-271">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-272">**OtherTransferCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-272">**OtherTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-273">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-273">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-275">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="93ff1-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-276">Quantité de données transférées pendant les opérations qui ne sont pas des opérations de lecture ou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="93ff1-276">Amount of data transferred during operations that are not read or write operations.</span></span>

<span data-ttu-id="93ff1-277">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-277">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-278">**PageFaults**</span><span class="sxs-lookup"><span data-stu-id="93ff1-278">**PageFaults**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-279">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-281">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nombre de défauts de page")</span><span class="sxs-lookup"><span data-stu-id="93ff1-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-282">Nombre de défauts de page générés par un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-282">Number of page faults that a process generates.</span></span>

<span data-ttu-id="93ff1-283">Exemple : 10</span><span class="sxs-lookup"><span data-stu-id="93ff1-283">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-284">**PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="93ff1-284">**PageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-285">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-287">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("page file usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilo-octets")</span><span class="sxs-lookup"><span data-stu-id="93ff1-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-288">Quantité d’espace de fichier d’échange actuellement utilisée par un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-288">Amount of page file space that a process is using currently.</span></span> <span data-ttu-id="93ff1-289">Cette valeur est cohérente avec la valeur **VMSize** dans TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="93ff1-289">This value is consistent with the **VMSize** value in TaskMgr.exe.</span></span>

<span data-ttu-id="93ff1-290">Exemple : 102435</span><span class="sxs-lookup"><span data-stu-id="93ff1-290">Example: 102435</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-291">**ParentProcessId**</span><span class="sxs-lookup"><span data-stu-id="93ff1-291">**ParentProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-292">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-294">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api process \| Status \| System \_ process \_ information \| InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("parent Process ID")</span><span class="sxs-lookup"><span data-stu-id="93ff1-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-295">Identificateur unique du processus qui crée un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-295">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="93ff1-296">Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-296">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="93ff1-297">Il est possible que le processus identifié par **ParentProcessId** soit terminé, de sorte que **ParentProcessId** ne peut pas faire référence à un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="93ff1-297">It is possible that the process identified by **ParentProcessId** is terminated, so **ParentProcessId** may not refer to a running process.</span></span> <span data-ttu-id="93ff1-298">Il est également possible que **ParentProcessId** fasse incorrectement référence à un processus qui réutilise un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-298">It is also possible that **ParentProcessId** incorrectly refers to a process that reuses a process identifier.</span></span> <span data-ttu-id="93ff1-299">Vous pouvez utiliser la propriété **CreationDate** pour déterminer si le parent spécifié a été créé après la création du processus représenté par cette instance de **\_ processus Win32** .</span><span class="sxs-lookup"><span data-stu-id="93ff1-299">You can use the **CreationDate** property to determine whether the specified parent was created after the process represented by this **Win32\_Process** instance was created.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-300">**PeakPageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="93ff1-300">**PeakPageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-301">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-303">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("PIC utilisation du fichier d’échange"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilo-octets")</span><span class="sxs-lookup"><span data-stu-id="93ff1-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-304">Quantité maximale d’espace de fichier d’échange utilisée pendant la durée de vie d’un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-304">Maximum amount of page file space used during the life of a process.</span></span>

<span data-ttu-id="93ff1-305">Exemple : 102367</span><span class="sxs-lookup"><span data-stu-id="93ff1-305">Example: 102367</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-306">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="93ff1-306">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-307">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-309">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("PIC utilisation de l’espace d’adressage virtuelle"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="93ff1-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-310">Espace d’adressage virtuel maximal qu’un processus utilise à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="93ff1-310">Maximum virtual address space a process uses at any one time.</span></span> <span data-ttu-id="93ff1-311">L’utilisation de l’espace d’adressage virtuel n’implique pas nécessairement l’utilisation correspondante du disque ou des pages de mémoire principales.</span><span class="sxs-lookup"><span data-stu-id="93ff1-311">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="93ff1-312">Toutefois, l’espace virtuel est fini, et en utilisant trop de temps, le processus peut ne pas être en mesure de charger des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="93ff1-312">However, virtual space is finite, and by using too much the process might not be able to load libraries.</span></span>

<span data-ttu-id="93ff1-313">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-313">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-314">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="93ff1-314">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-315">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-317">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| PeakWorkingSetSize »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Peak Working Set Size »), [**Units**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-318">Taille maximale de la plage de travail d’un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-318">Peak working set size of a process.</span></span>

<span data-ttu-id="93ff1-319">Exemple : 1413120</span><span class="sxs-lookup"><span data-stu-id="93ff1-319">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-320">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="93ff1-320">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-321">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-323">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (« Priority »), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| BasePriority »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Priority »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-323">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-324">Priorité de planification d’un processus dans un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="93ff1-324">Scheduling priority of a process within an operating system.</span></span> <span data-ttu-id="93ff1-325">Plus la valeur est élevée, plus le processus reçoit la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="93ff1-325">The higher the value, the higher priority a process receives.</span></span> <span data-ttu-id="93ff1-326">Les valeurs de priorité peuvent être comprises entre 0 (zéro), qui est la priorité la plus faible à 31, qui est la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="93ff1-326">Priority values can range from 0 (zero), which is the lowest priority to 31, which is highest priority.</span></span>

<span data-ttu-id="93ff1-327">Exemple : 7</span><span class="sxs-lookup"><span data-stu-id="93ff1-327">Example: 7</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-328">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-328">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-329">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-331">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private page Count")</span><span class="sxs-lookup"><span data-stu-id="93ff1-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-332">Nombre actuel de pages allouées qui sont uniquement accessibles au processus représenté par cette instance de **\_ processus Win32** .</span><span class="sxs-lookup"><span data-stu-id="93ff1-332">Current number of pages allocated that are only accessible to the process represented by this **Win32\_Process** instance.</span></span>

<span data-ttu-id="93ff1-333">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-334">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="93ff1-334">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-335">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-337">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| [**process \_ information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="93ff1-337">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)\|dwProcessId "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-338">Identificateur numérique utilisé pour distinguer un processus d’un autre.</span><span class="sxs-lookup"><span data-stu-id="93ff1-338">Numeric identifier used to distinguish one process from another.</span></span> <span data-ttu-id="93ff1-339">Les ProcessIDs sont valides à partir de l’heure de création du processus pour traiter l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="93ff1-339">ProcessIDs are valid from process creation time to process termination.</span></span> <span data-ttu-id="93ff1-340">Lors de l’arrêt, ce même identificateur numérique peut être appliqué à un nouveau processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-340">Upon termination, that same numeric identifier can be applied to a new process.</span></span>

<span data-ttu-id="93ff1-341">Cela signifie que vous ne pouvez pas utiliser ProcessID seul pour surveiller un processus particulier.</span><span class="sxs-lookup"><span data-stu-id="93ff1-341">This means that you cannot use ProcessID alone to monitor a particular process.</span></span> <span data-ttu-id="93ff1-342">Par exemple, une application peut avoir un ProcessID de 7, puis échouer.</span><span class="sxs-lookup"><span data-stu-id="93ff1-342">For example, an application could have a ProcessID of 7, and then fail.</span></span> <span data-ttu-id="93ff1-343">Lors du démarrage d’un nouveau processus, ProcessID 7 peut être affecté au nouveau processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-343">When a new process is started, the new process could be assigned ProcessID 7.</span></span> <span data-ttu-id="93ff1-344">Un script qui vérifie uniquement un ProcessID spécifié peut donc être « trompeur » pour penser que l’application d’origine était toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="93ff1-344">A script that checked only for a specified ProcessID could thus be "fooled" into thinking that the original application was still running.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-345">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="93ff1-345">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-346">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-348">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota d’utilisation de réserve non paginée")</span><span class="sxs-lookup"><span data-stu-id="93ff1-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-349">Quota d’utilisation de la réserve non paginée pour un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-349">Quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="93ff1-350">Exemple : 15</span><span class="sxs-lookup"><span data-stu-id="93ff1-350">Example: 15</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-351">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="93ff1-351">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-352">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-354">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("quota d’utilisation de la réserve paginée")</span><span class="sxs-lookup"><span data-stu-id="93ff1-354">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-355">Quota d’utilisation de la réserve paginée pour un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-355">Quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="93ff1-356">Exemple : 22</span><span class="sxs-lookup"><span data-stu-id="93ff1-356">Example: 22</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-357">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="93ff1-357">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-358">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-360">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| QuotaPeakNonPagedPoolUsage »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« quota de pic d’utilisation du pool non paginé »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-361">Quota de pic d’utilisation de la réserve non paginée pour un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-361">Peak quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="93ff1-362">Exemple : 31</span><span class="sxs-lookup"><span data-stu-id="93ff1-362">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-363">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="93ff1-363">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-364">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-366">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| QuotaPeakPagedPoolUsage »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« quota d’utilisation maximale de la réserve paginée »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-366">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-367">Quota de pic d’utilisation de la réserve paginée pour un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-367">Peak quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="93ff1-368">Exemple : 31</span><span class="sxs-lookup"><span data-stu-id="93ff1-368">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-369">**ReadOperationCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-369">**ReadOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-370">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-372">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span><span class="sxs-lookup"><span data-stu-id="93ff1-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-373">Nombre d’opérations de lecture effectuées.</span><span class="sxs-lookup"><span data-stu-id="93ff1-373">Number of read operations performed.</span></span>

<span data-ttu-id="93ff1-374">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-374">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-375">**ReadTransferCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-375">**ReadTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-376">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-376">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-378">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="93ff1-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-379">Quantité de données lues.</span><span class="sxs-lookup"><span data-stu-id="93ff1-379">Amount of data read.</span></span>

<span data-ttu-id="93ff1-380">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-381">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="93ff1-381">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-382">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-384">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process status \| System \_ process \_ information \| SessionID »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« ID de session »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-384">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Session Id")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-385">Identificateur unique généré par un système d’exploitation lors de la création d’une session.</span><span class="sxs-lookup"><span data-stu-id="93ff1-385">Unique identifier that an operating system generates when a session is created.</span></span> <span data-ttu-id="93ff1-386">Une session s’étend sur un laps de temps à partir d’une ouverture de session jusqu’à la fermeture d’un système spécifique.</span><span class="sxs-lookup"><span data-stu-id="93ff1-386">A session spans a period of time from logon until logoff from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-387">**État**</span><span class="sxs-lookup"><span data-stu-id="93ff1-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-390">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="93ff1-390">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-391">Cette propriété n’est pas implémentée et n’est pas remplie pour une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="93ff1-391">This property is not implemented and does not get populated for any instance of this class.</span></span> <span data-ttu-id="93ff1-392">La valeur est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="93ff1-392">It is always **NULL**.</span></span>

<span data-ttu-id="93ff1-393">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-393">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="93ff1-394">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="93ff1-394">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="93ff1-395">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-395">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="93ff1-396">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-396">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="93ff1-397">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-397">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93ff1-398">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="93ff1-398">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="93ff1-399">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-399">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="93ff1-400">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-400">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="93ff1-401">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-401">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="93ff1-402">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-402">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="93ff1-403">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-403">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="93ff1-404">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-404">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="93ff1-405">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-405">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="93ff1-406">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-406">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93ff1-407">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="93ff1-407">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-408">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93ff1-408">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-410">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("date d’arrêt")</span><span class="sxs-lookup"><span data-stu-id="93ff1-410">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-411">Le processus a été arrêté ou arrêté.</span><span class="sxs-lookup"><span data-stu-id="93ff1-411">Process was stopped or terminated.</span></span> <span data-ttu-id="93ff1-412">Pour obtenir l’heure de fin, un descripteur du processus doit être maintenu ouvert.</span><span class="sxs-lookup"><span data-stu-id="93ff1-412">To get the termination time, a handle to the process must be held open.</span></span> <span data-ttu-id="93ff1-413">Sinon, cette propriété retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="93ff1-413">Otherwise, this property returns **NULL**.</span></span>

<span data-ttu-id="93ff1-414">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-414">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-415">**ThreadCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-415">**ThreadCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-416">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93ff1-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-418">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nombre de threads")</span><span class="sxs-lookup"><span data-stu-id="93ff1-418">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-419">Nombre de threads actifs dans un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-419">Number of active threads in a process.</span></span> <span data-ttu-id="93ff1-420">Une instruction est l’unité d’exécution de base dans un processeur, et un thread est l’objet qui exécute une instruction.</span><span class="sxs-lookup"><span data-stu-id="93ff1-420">An instruction is the basic unit of execution in a processor, and a thread is the object that executes an instruction.</span></span> <span data-ttu-id="93ff1-421">Chaque processus en cours d’exécution possède au moins un thread.</span><span class="sxs-lookup"><span data-stu-id="93ff1-421">Each running process has at least one thread.</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-422">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="93ff1-422">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-423">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-423">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-425">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="93ff1-425">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-426">Heure en mode utilisateur, en unités de nanosecondes 100.</span><span class="sxs-lookup"><span data-stu-id="93ff1-426">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="93ff1-427">Si ces informations ne sont pas disponibles, utilisez la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="93ff1-427">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="93ff1-428">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-428">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-429">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="93ff1-429">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-430">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-432">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process status \| System \_ process \_ information \| VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("utilisation de l’espace d’adressage virtuel"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="93ff1-432">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-433">Taille actuelle de l’espace d’adressage virtuel utilisé par un processus, et non de la mémoire physique ou virtuelle réellement utilisée par le processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-433">Current size of the virtual address space that a process is using, not the physical or virtual memory actually used by the process.</span></span> <span data-ttu-id="93ff1-434">L’utilisation de l’espace d’adressage virtuel n’implique pas nécessairement l’utilisation correspondante du disque ou des pages de mémoire principales.</span><span class="sxs-lookup"><span data-stu-id="93ff1-434">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="93ff1-435">L’espace virtuel est fini, et en utilisant trop, le processus peut ne pas être en mesure de charger des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="93ff1-435">Virtual space is finite, and by using too much, the process might not be able to load libraries.</span></span> <span data-ttu-id="93ff1-436">Cette valeur est cohérente avec ce que vous voyez dans Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="93ff1-436">This value is consistent with what you see in Perfmon.exe.</span></span>

<span data-ttu-id="93ff1-437">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-437">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-438">**WindowsVersion**</span><span class="sxs-lookup"><span data-stu-id="93ff1-438">**WindowsVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93ff1-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-441">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Process and thread Functions \| GetProcessVersion »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« version de Windows »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-442">Version de Windows dans laquelle le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="93ff1-442">Version of Windows in which the process is running.</span></span>

<span data-ttu-id="93ff1-443">Exemple : 4,0</span><span class="sxs-lookup"><span data-stu-id="93ff1-443">Example: 4.0</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-444">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="93ff1-444">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-445">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-447">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« taille de la plage de travail »), [**unités**](../wmisdk/standard-qualifiers.md) (« octets »)</span><span class="sxs-lookup"><span data-stu-id="93ff1-447">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-448">Quantité de mémoire en octets qu’un processus doit exécuter efficacement : pour un système d’exploitation qui utilise la gestion de la mémoire basée sur les pages.</span><span class="sxs-lookup"><span data-stu-id="93ff1-448">Amount of memory in bytes that a process needs to execute efficiently—for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="93ff1-449">Si le système ne dispose pas de suffisamment de mémoire (inférieure à la taille de la plage de travail), une surcharge se produit.</span><span class="sxs-lookup"><span data-stu-id="93ff1-449">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="93ff1-450">Si la taille de la plage de travail n’est pas connue, utilisez la **valeur null** ou 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="93ff1-450">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="93ff1-451">Si vous fournissez des données de jeu de travail, vous pouvez surveiller les informations pour comprendre les besoins en mémoire en constante évolution d’un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-451">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="93ff1-452">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-452">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="93ff1-453">Cette propriété est héritée [**du \_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-453">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-454">**WriteOperationCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-454">**WriteOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-455">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-455">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-456">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-457">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write opération Count")</span><span class="sxs-lookup"><span data-stu-id="93ff1-457">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-458">Nombre d’opérations d’écriture effectuées.</span><span class="sxs-lookup"><span data-stu-id="93ff1-458">Number of write operations performed.</span></span>

<span data-ttu-id="93ff1-459">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-459">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="93ff1-460">**WriteTransferCount**</span><span class="sxs-lookup"><span data-stu-id="93ff1-460">**WriteTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93ff1-461">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93ff1-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-462">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93ff1-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93ff1-463">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process and thread structures \| System \_ process \_ information \| WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="93ff1-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93ff1-464">Quantité de données écrites.</span><span class="sxs-lookup"><span data-stu-id="93ff1-464">Amount of data written.</span></span>

<span data-ttu-id="93ff1-465">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-465">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93ff1-466">Notes</span><span class="sxs-lookup"><span data-stu-id="93ff1-466">Remarks</span></span>

<span data-ttu-id="93ff1-467">La classe de **\_ processus Win32** est dérivée du [**\_ processus CIM**](cim-process.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-467">The **Win32\_Process** class is derived from [**CIM\_Process**](cim-process.md).</span></span> <span data-ttu-id="93ff1-468">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="93ff1-468">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="93ff1-469">Pour plus d’informations, consultez [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-469">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

### <a name="overview"></a><span data-ttu-id="93ff1-470">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="93ff1-470">Overview</span></span>

<span data-ttu-id="93ff1-471">Les processus sous-tendent presque tout ce qui se produit sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="93ff1-471">Processes underlie almost everything that happens on a computer.</span></span> <span data-ttu-id="93ff1-472">En fait, la cause racine de la plupart des problèmes informatiques peut être tracée sur les processus. par exemple, un trop grand nombre de processus peuvent s’exécuter sur un ordinateur (et être en conflit avec un ensemble fini de ressources), ou un processus unique peut utiliser plus que son partage de ressources.</span><span class="sxs-lookup"><span data-stu-id="93ff1-472">In fact, the root cause of most computer problems can be traced to processes; for example, too many processes might be running on a computer (and contending for a finite set of resources), or a single process might be using more than its share of resources.</span></span> <span data-ttu-id="93ff1-473">Ces facteurs compliquent le suivi des processus en cours d’exécution sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="93ff1-473">These factors make it important to keep a close watch on the processes running on a computer.</span></span> <span data-ttu-id="93ff1-474">La surveillance des processus, l’activité principale de la gestion des processus, vous permet de déterminer ce qu’est réellement un ordinateur, les applications que l’ordinateur exécute et la manière dont ces applications sont affectées par les modifications dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="93ff1-474">Process monitoring, the main activity in process management, allows you to determine what a computer actually does, what applications the computer runs, and how those applications are affected by changes in the computing environment.</span></span>

### <a name="monitoring-a-process"></a><span data-ttu-id="93ff1-475">Surveillance d’un processus</span><span class="sxs-lookup"><span data-stu-id="93ff1-475">Monitoring a Process</span></span>

<span data-ttu-id="93ff1-476">La surveillance régulière des processus vous permet de vous assurer qu’un ordinateur fonctionne aux pics d’activité et qu’il exécute ses tâches nommées comme prévu.</span><span class="sxs-lookup"><span data-stu-id="93ff1-476">Monitoring processes on a regular basis helps you ensure that a computer runs at peak efficiency and that it carries out its appointed tasks as expected.</span></span> <span data-ttu-id="93ff1-477">Par exemple, en surveillant les processus, vous pouvez être averti immédiatement de toute application qui ne répond plus, puis prendre les mesures nécessaires pour terminer ce processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-477">For example, by monitoring processes you can be notified immediately of any application that has stopped responding, and then take steps to end that process.</span></span> <span data-ttu-id="93ff1-478">En outre, le processus d’analyse vous permet d’identifier les problèmes avant qu’ils ne se produisent.</span><span class="sxs-lookup"><span data-stu-id="93ff1-478">In addition, process monitoring enables you to identify problems before they occur.</span></span> <span data-ttu-id="93ff1-479">Par exemple, en vérifiant de manière répétée la quantité de mémoire utilisée par un processus, vous pouvez identifier une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="93ff1-479">For example, by repeatedly checking the amount of memory used by a process, you can identify a memory leak.</span></span> <span data-ttu-id="93ff1-480">Vous pouvez ensuite arrêter le processus avant que l’application errante n’utilise toute la mémoire disponible et met l’ordinateur en arrêt.</span><span class="sxs-lookup"><span data-stu-id="93ff1-480">You can then stop the process before the errant application uses all of the available memory and brings the computer to a halt.</span></span>

<span data-ttu-id="93ff1-481">La surveillance des processus permet également de réduire les perturbations causées par des interruptions planifiées des mises à niveau et de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="93ff1-481">Process monitoring also helps minimize the disruptions caused by planned outages for upgrades and maintenance.</span></span> <span data-ttu-id="93ff1-482">Par exemple, en vérifiant l’état d’une application de base de données qui s’exécute sur les ordinateurs clients, vous pouvez déterminer l’impact de la mise hors connexion de la base de données afin de mettre à niveau le logiciel.</span><span class="sxs-lookup"><span data-stu-id="93ff1-482">For example, by checking the status of a database application running on client computers, you can determine the impact of taking the database offline in order to upgrade the software.</span></span>

<span data-ttu-id="93ff1-483">Surveillance de la disponibilité du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-483">Monitoring process availability.</span></span> <span data-ttu-id="93ff1-484">Mesure le pourcentage de temps pendant lequel un processus est disponible.</span><span class="sxs-lookup"><span data-stu-id="93ff1-484">Measures the percentage of time that a process is available.</span></span> <span data-ttu-id="93ff1-485">La disponibilité est généralement surveillée à l’aide d’une sonde simple, qui indique si le processus est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="93ff1-485">Availability is typically monitored by use of a simple probe, which reports whether the process is still running.</span></span> <span data-ttu-id="93ff1-486">En effectuant le suivi des résultats de chaque sonde, vous pouvez calculer la disponibilité du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-486">By keeping track of the results of each probe, you can calculate the availability of the process.</span></span> <span data-ttu-id="93ff1-487">Par exemple, un processus qui est interrogé 100 fois et qui répond sur 95 de ces occasions a une disponibilité de 95%.</span><span class="sxs-lookup"><span data-stu-id="93ff1-487">For example, a process that is probed 100 times and responds on 95 of those occasions has an availability of 95 percent.</span></span> <span data-ttu-id="93ff1-488">Ce type de surveillance est généralement réservé aux bases de données, aux programmes de messagerie et aux autres applications censées s’exécuter à tout moment.</span><span class="sxs-lookup"><span data-stu-id="93ff1-488">This type of monitoring is typically reserved for databases, mail programs, and other applications that are expected to run at all times.</span></span> <span data-ttu-id="93ff1-489">Il n’est pas approprié pour les programmes de traitement de texte, les feuilles de calcul ou d’autres applications qui sont régulièrement démarrés et arrêtés plusieurs fois par jour.</span><span class="sxs-lookup"><span data-stu-id="93ff1-489">It is not appropriate for word processing programs, spreadsheets, or other applications that are routinely started and stopped several times a day.</span></span>

<span data-ttu-id="93ff1-490">Vous pouvez créer une instance de la classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) pour configurer le processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-490">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process.</span></span>

<span data-ttu-id="93ff1-491">Vous pouvez surveiller les performances des processus avec la classe de [**\_ \_ \_ processus perfproc Win32 PerfFormattedData**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) et un objet d’actualisation WMI, tel que [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-491">You can monitor process performance with the [**Win32\_PerfFormattedData\_PerfProc\_Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) class and a WMI refresher object, such as [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span></span> <span data-ttu-id="93ff1-492">Pour plus d’informations, consultez [analyse des données de performances](../wmisdk/monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="93ff1-492">For more information, see [Monitoring Performance Data](../wmisdk/monitoring-performance-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="93ff1-493">Exemples</span><span class="sxs-lookup"><span data-stu-id="93ff1-493">Examples</span></span>

<span data-ttu-id="93ff1-494">La [liste des propriétés de l’exemple de code PowerShell des classes WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) dans la Galerie TechNet décrit la classe de **\_ processus Win32** et renvoie les résultats au format Excel.</span><span class="sxs-lookup"><span data-stu-id="93ff1-494">The [List the Properties of WMI Classes](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell code sample on TechNet Gallery describes the **Win32\_Process** class, and outputs the results in Excel format.</span></span>

<span data-ttu-id="93ff1-495">Le [processus de fin d’exécution sur plusieurs serveurs](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) met fin à un processus s’exécutant sur un ou plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="93ff1-495">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="93ff1-496">Dans l' [exemple : appel d’une](../wmisdk/example--calling-a-provider-method.md) rubrique de méthode de fournisseur, le code utilise C++ pour appeler le **\_ processus Win32** afin de créer un processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-496">In the [Example: Calling a Provider Method](../wmisdk/example--calling-a-provider-method.md) topic, the code uses C++ to call **Win32\_Process** to create a process.</span></span>

<span data-ttu-id="93ff1-497">La disponibilité est la forme la plus simple d’analyse de processus : avec cette approche, vous vous assurez simplement que le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="93ff1-497">Availability is the simplest form of process monitoring: with this approach, you simply ensure that the process is running.</span></span> <span data-ttu-id="93ff1-498">Lorsque vous surveillez la disponibilité du processus, vous récupérez généralement une liste des processus en cours d’exécution sur un ordinateur, puis vous vérifiez qu’un processus particulier est toujours actif.</span><span class="sxs-lookup"><span data-stu-id="93ff1-498">When you monitor for process availability, you typically retrieve a list of processes running on a computer and then verify that a particular process is still active.</span></span> <span data-ttu-id="93ff1-499">Si le processus est actif, il est considéré comme disponible.</span><span class="sxs-lookup"><span data-stu-id="93ff1-499">If the process is active, it is considered available.</span></span> <span data-ttu-id="93ff1-500">Si le processus n’est pas actif, il n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="93ff1-500">If the process is not active, it is not available.</span></span> <span data-ttu-id="93ff1-501">L’exemple VBScript suivant surveille la disponibilité des processus en vérifiant la liste des processus en cours d’exécution sur un ordinateur et en émettant une notification si le processus de Database.exe est introuvable.</span><span class="sxs-lookup"><span data-stu-id="93ff1-501">The following VBScript sample monitors process availability by checking the list of processes running on a computer and issuing a notification if the Database.exe process is not found.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



<span data-ttu-id="93ff1-502">L’exemple VBScript suivant surveille la création de processus à l’aide d’un consommateur d’événements temporaire.</span><span class="sxs-lookup"><span data-stu-id="93ff1-502">The following VBScript sample monitors process creation using a temporary event consumer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



<span data-ttu-id="93ff1-503">Le VBScript suivant surveille les informations sur les performances du processus.</span><span class="sxs-lookup"><span data-stu-id="93ff1-503">The following VBScript monitors process performance information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



<span data-ttu-id="93ff1-504">L’exemple de code VBScript suivant montre comment obtenir le propriétaire de chaque processus sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="93ff1-504">The following VBScript code example shows how to obtain the owner of each process on a local computer.</span></span> <span data-ttu-id="93ff1-505">Vous pouvez utiliser ce script pour obtenir des données à partir d’un ordinateur distant, par exemple, pour déterminer quels utilisateurs ont des processus exécutant Terminal Server, remplacez le nom de l’ordinateur distant par « . » sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="93ff1-505">You can use this script to obtain data from a remote computer, for example, to determine which users have processes running terminal server, substitute the name of the remote computer for "." in the first line.</span></span> <span data-ttu-id="93ff1-506">Vous devez également être administrateur sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="93ff1-506">You must also be an administrator on the remote machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



<span data-ttu-id="93ff1-507">L’exemple de code VBScript suivant montre comment obtenir la session d’ouverture de session associée à un processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="93ff1-507">The following VBScript code example shows how to obtain the logon session associated with a running process.</span></span> <span data-ttu-id="93ff1-508">Un processus doit être en cours d’exécution Notepad.exe avant le démarrage du script.</span><span class="sxs-lookup"><span data-stu-id="93ff1-508">A process must be running Notepad.exe before the script starts.</span></span> <span data-ttu-id="93ff1-509">L’exemple localise les instances de [**\_ LogonSession Win32**](win32-logonsession.md) associées au **\_ processus Win32** qui représente Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="93ff1-509">The example locates the instances of [**Win32\_LogonSession**](win32-logonsession.md) associated with the **Win32\_Process** that represents Notepad.exe.</span></span> <span data-ttu-id="93ff1-510">[**Win32 \_ SessionProcess**](win32-sessionprocess.md) est spécifié en tant que classe d’association.</span><span class="sxs-lookup"><span data-stu-id="93ff1-510">[**Win32\_SessionProcess**](win32-sessionprocess.md) is specified as the association class.</span></span> <span data-ttu-id="93ff1-511">Pour plus d’informations, consultez [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md)</span><span class="sxs-lookup"><span data-stu-id="93ff1-511">For more information, see [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md).</span></span>


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a><span data-ttu-id="93ff1-512">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93ff1-512">Requirements</span></span>



| <span data-ttu-id="93ff1-513">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93ff1-513">Requirement</span></span> | <span data-ttu-id="93ff1-514">Valeur</span><span class="sxs-lookup"><span data-stu-id="93ff1-514">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93ff1-515">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93ff1-515">Minimum supported client</span></span><br/> | <span data-ttu-id="93ff1-516">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93ff1-516">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93ff1-517">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93ff1-517">Minimum supported server</span></span><br/> | <span data-ttu-id="93ff1-518">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93ff1-518">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93ff1-519">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="93ff1-519">Namespace</span></span><br/>                | <span data-ttu-id="93ff1-520">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="93ff1-520">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93ff1-521">MOF</span><span class="sxs-lookup"><span data-stu-id="93ff1-521">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93ff1-522"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93ff1-522"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93ff1-523">DLL</span><span class="sxs-lookup"><span data-stu-id="93ff1-523">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ff1-524"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93ff1-524"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93ff1-525">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93ff1-525">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ff1-526">**\_Processus CIM**</span><span class="sxs-lookup"><span data-stu-id="93ff1-526">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dt>

[<span data-ttu-id="93ff1-527">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="93ff1-527">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="93ff1-528">Tâches WMI : processus</span><span class="sxs-lookup"><span data-stu-id="93ff1-528">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
