---
description: Le \_ Registre Win32&\# 8194 ; La classe WMI représente le registre système sur un système informatique exécutant Windows.
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Classe Win32_Registry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1dc5fd89ee589aabda5da5f97632d86b39f6beb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950471"
---
# <a name="win32_registry-class"></a><span data-ttu-id="ca864-103">\_Classe de Registre Win32</span><span class="sxs-lookup"><span data-stu-id="ca864-103">Win32\_Registry class</span></span>

<span data-ttu-id="ca864-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ du Registre Win32** représente le registre système sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="ca864-104">The **Win32\_Registry** [WMI class](../wmisdk/retrieving-a-class.md) represents the system registry on a computer system running Windows.</span></span>

<span data-ttu-id="ca864-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ca864-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ca864-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ca864-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca864-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca864-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a><span data-ttu-id="ca864-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ca864-108">Members</span></span>

<span data-ttu-id="ca864-109">La classe de **\_ Registre Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ca864-109">The **Win32\_Registry** class has these types of members:</span></span>

-   [<span data-ttu-id="ca864-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ca864-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca864-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ca864-111">Properties</span></span>

<span data-ttu-id="ca864-112">La classe de **\_ Registre Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ca864-112">The **Win32\_Registry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca864-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ca864-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca864-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca864-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca864-116">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="ca864-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca864-117">A short textual description of the object.</span></span>

<span data-ttu-id="ca864-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca864-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca864-119">**CurrentSize**</span><span class="sxs-lookup"><span data-stu-id="ca864-119">**CurrentSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca864-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca864-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca864-122">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemRegistryQuotaInformation"), [**unités**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)</span><span class="sxs-lookup"><span data-stu-id="ca864-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-123">Taille physique actuelle du Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="ca864-123">Current physical size of the Windows registry.</span></span>

<span data-ttu-id="ca864-124">Exemple : 10</span><span class="sxs-lookup"><span data-stu-id="ca864-124">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="ca864-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="ca864-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca864-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca864-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca864-128">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ca864-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-129">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca864-129">A textual description of the object.</span></span>

<span data-ttu-id="ca864-130">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca864-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca864-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ca864-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-132">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ca864-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca864-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca864-134">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="ca864-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-135">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="ca864-135">Indicates when the object was installed.</span></span> <span data-ttu-id="ca864-136">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ca864-136">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ca864-137">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca864-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca864-138">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="ca864-138">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca864-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca864-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca864-141">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("mégaoctets")</span><span class="sxs-lookup"><span data-stu-id="ca864-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-142">Taille maximale du Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="ca864-142">Maximum size of the Windows registry.</span></span> <span data-ttu-id="ca864-143">Si le système réussit à utiliser la propriété **proposedSize** , **MaximumSize** doit contenir la même valeur.</span><span class="sxs-lookup"><span data-stu-id="ca864-143">If the system is successful in using the **ProposedSize** property, **MaximumSize** should contain the same value.</span></span>

</dd> <dt>

<span data-ttu-id="ca864-144">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ca864-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca864-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca864-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca864-147">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="ca864-147">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-148">Nom du Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="ca864-148">Name of the Windows registry.</span></span> <span data-ttu-id="ca864-149">La longueur maximale est de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="ca864-149">The maximum length is 256 characters.</span></span>

</dd> <dt>

<span data-ttu-id="ca864-150">**ProposedSize**</span><span class="sxs-lookup"><span data-stu-id="ca864-150">**ProposedSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca864-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ca864-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ca864-153">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("mégaoctets")</span><span class="sxs-lookup"><span data-stu-id="ca864-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-154">Taille proposée du Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="ca864-154">Proposed size of the Windows registry.</span></span> <span data-ttu-id="ca864-155">C’est le seul paramètre de Registre qui peut être modifié et sa proposition est tentée lors du prochain démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="ca864-155">It is the only registry setting that can be modified, and its proposal is attempted the next time the system boots.</span></span>

</dd> <dt>

<span data-ttu-id="ca864-156">**État**</span><span class="sxs-lookup"><span data-stu-id="ca864-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca864-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ca864-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca864-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca864-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca864-159">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ca864-159">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ca864-160">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca864-160">String that indicates the current status of the object.</span></span> <span data-ttu-id="ca864-161">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="ca864-161">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ca864-162">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="ca864-162">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ca864-163">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="ca864-163">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ca864-164">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="ca864-164">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ca864-165">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="ca864-165">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ca864-166">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="ca864-166">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ca864-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca864-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ca864-168">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ca864-168">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ca864-169">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="ca864-169">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ca864-170">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="ca864-170">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ca864-171">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ca864-171">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca864-172">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="ca864-172">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ca864-173">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ca864-173">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ca864-174">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ca864-174">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ca864-175">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ca864-175">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ca864-176">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="ca864-176">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ca864-177">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="ca864-177">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ca864-178">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="ca864-178">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ca864-179">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="ca864-179">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ca864-180">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="ca864-180">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="ca864-181"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ca864-181"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ca864-182">Notes</span><span class="sxs-lookup"><span data-stu-id="ca864-182">Remarks</span></span>

<span data-ttu-id="ca864-183">La classe de **\_ Registre Win32** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ca864-183">The **Win32\_Registry** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca864-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca864-184">Requirements</span></span>



| <span data-ttu-id="ca864-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca864-185">Requirement</span></span> | <span data-ttu-id="ca864-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca864-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca864-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca864-187">Minimum supported client</span></span><br/> | <span data-ttu-id="ca864-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca864-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca864-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca864-189">Minimum supported server</span></span><br/> | <span data-ttu-id="ca864-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca864-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca864-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ca864-191">Namespace</span></span><br/>                | <span data-ttu-id="ca864-192">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ca864-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca864-193">MOF</span><span class="sxs-lookup"><span data-stu-id="ca864-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca864-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca864-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca864-195">DLL</span><span class="sxs-lookup"><span data-stu-id="ca864-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca864-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca864-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca864-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca864-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca864-198">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ca864-198">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="ca864-199">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ca864-199">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
