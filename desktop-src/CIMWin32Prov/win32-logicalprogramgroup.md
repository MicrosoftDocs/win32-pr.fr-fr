---
description: Le \_ LogicalProgramGroup Win32&\# 8194 ; La classe WMI représente un groupe de programmes sur un système informatique exécutant Windows. Par exemple, accessoires ou Startup.
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861501"
---
# <a name="win32_logicalprogramgroup-class"></a><span data-ttu-id="b4699-104">\_Classe LogicalProgramGroup Win32</span><span class="sxs-lookup"><span data-stu-id="b4699-104">Win32\_LogicalProgramGroup class</span></span>

<span data-ttu-id="b4699-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ LogicalProgramGroup** représente un groupe de programmes sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="b4699-105">The **Win32\_LogicalProgramGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a program group in a computer system running Windows.</span></span> <span data-ttu-id="b4699-106">Par exemple, accessoires ou Startup.</span><span class="sxs-lookup"><span data-stu-id="b4699-106">For example, Accessories or Startup.</span></span>

<span data-ttu-id="b4699-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b4699-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b4699-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b4699-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4699-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4699-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="b4699-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b4699-110">Members</span></span>

<span data-ttu-id="b4699-111">La classe **Win32 \_ LogicalProgramGroup** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b4699-111">The **Win32\_LogicalProgramGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="b4699-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4699-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4699-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4699-113">Properties</span></span>

<span data-ttu-id="b4699-114">La classe **Win32 \_ LogicalProgramGroup** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b4699-114">The **Win32\_LogicalProgramGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4699-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b4699-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4699-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4699-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4699-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4699-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4699-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="b4699-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b4699-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4699-119">A short textual description of the object.</span></span>

<span data-ttu-id="b4699-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4699-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4699-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="b4699-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4699-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4699-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4699-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4699-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4699-124">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b4699-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b4699-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4699-125">A textual description of the object.</span></span>

<span data-ttu-id="b4699-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4699-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4699-127">**GroupName**</span><span class="sxs-lookup"><span data-stu-id="b4699-127">**GroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4699-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4699-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4699-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4699-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4699-130">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue, méthodes de classe \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="b4699-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="b4699-131">Nom du groupe de programmes Windows.</span><span class="sxs-lookup"><span data-stu-id="b4699-131">Name of the Windows program group.</span></span> <span data-ttu-id="b4699-132">Les groupes de programmes sont implémentés en tant que dossiers de fichiers dans Win32.</span><span class="sxs-lookup"><span data-stu-id="b4699-132">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="b4699-133">Exemple : « \\ Outils système accessoires »</span><span class="sxs-lookup"><span data-stu-id="b4699-133">Example: "Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="b4699-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b4699-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4699-135">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4699-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4699-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4699-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4699-137">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="b4699-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b4699-138">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="b4699-138">Indicates when the object was installed.</span></span> <span data-ttu-id="b4699-139">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="b4699-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b4699-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4699-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4699-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b4699-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4699-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4699-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4699-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4699-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4699-144">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue Class Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="b4699-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="b4699-145">Nom affecté par l’utilisateur, suivi du nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="b4699-145">User-assigned name followed by the group name.</span></span> <span data-ttu-id="b4699-146">Les groupes de programmes sont implémentés en tant que dossiers de fichiers dans Win32.</span><span class="sxs-lookup"><span data-stu-id="b4699-146">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="b4699-147">Exemple : « tous les utilisateurs : \\ Outils système accessoires »</span><span class="sxs-lookup"><span data-stu-id="b4699-147">Example: "All Users:Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="b4699-148">**État**</span><span class="sxs-lookup"><span data-stu-id="b4699-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4699-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4699-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4699-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4699-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4699-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b4699-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b4699-152">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4699-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="b4699-153">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="b4699-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b4699-154">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="b4699-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b4699-155">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="b4699-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b4699-156">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="b4699-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b4699-157">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="b4699-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b4699-158">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="b4699-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b4699-159">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4699-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b4699-160">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4699-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b4699-161">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="b4699-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b4699-162">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="b4699-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b4699-163">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="b4699-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4699-164">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="b4699-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b4699-165">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="b4699-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b4699-166">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="b4699-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b4699-167">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="b4699-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b4699-168">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="b4699-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b4699-169">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="b4699-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b4699-170">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="b4699-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b4699-171">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="b4699-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b4699-172">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="b4699-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4699-173">**UserName**</span><span class="sxs-lookup"><span data-stu-id="b4699-173">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4699-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4699-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4699-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4699-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4699-176">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue, méthodes de classe \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="b4699-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="b4699-177">Utilisateurs qui peuvent accéder au groupe de programmes Windows.</span><span class="sxs-lookup"><span data-stu-id="b4699-177">Users who can access the Windows program group.</span></span> <span data-ttu-id="b4699-178">Les groupes de programmes sont implémentés en tant que dossiers de fichiers dans Win32.</span><span class="sxs-lookup"><span data-stu-id="b4699-178">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="b4699-179">Exemple : « tous les utilisateurs »</span><span class="sxs-lookup"><span data-stu-id="b4699-179">Example: "All Users"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4699-180">Notes</span><span class="sxs-lookup"><span data-stu-id="b4699-180">Remarks</span></span>

<span data-ttu-id="b4699-181">La classe **Win32 \_ LogicalProgramGroup** est dérivée de [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="b4699-181">The **Win32\_LogicalProgramGroup** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="b4699-182">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="b4699-182">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="b4699-183">Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="b4699-183">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="b4699-184">Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="b4699-184">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4699-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4699-185">Requirements</span></span>



| <span data-ttu-id="b4699-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4699-186">Requirement</span></span> | <span data-ttu-id="b4699-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4699-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4699-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4699-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b4699-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4699-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4699-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4699-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b4699-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4699-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4699-192">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b4699-192">Namespace</span></span><br/>                | <span data-ttu-id="b4699-193">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b4699-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4699-194">MOF</span><span class="sxs-lookup"><span data-stu-id="b4699-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4699-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4699-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4699-196">DLL</span><span class="sxs-lookup"><span data-stu-id="b4699-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4699-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4699-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4699-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4699-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4699-199">**\_ProgramGroupOrItem Win32**</span><span class="sxs-lookup"><span data-stu-id="b4699-199">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="b4699-200">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b4699-200">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

