---
description: Le \_ LogicalProgramGroupItem Win32&\# 8194 ; La classe WMI représente un élément contenu par un \_ LogicalProgramGroup Win32 qui n’est pas également une autre \_ instance LogicalProgramGroup Win32.
ms.assetid: 70b127bf-4e94-4c1a-98ff-909bdfe0f009
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItem
- Win32_LogicalProgramGroupItem.Caption
- Win32_LogicalProgramGroupItem.Description
- Win32_LogicalProgramGroupItem.InstallDate
- Win32_LogicalProgramGroupItem.Status
- Win32_LogicalProgramGroupItem.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1afd78ba17e444520d8dec81eac05fffa103aede
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524276"
---
# <a name="win32_logicalprogramgroupitem-class"></a><span data-ttu-id="fd4d9-103">\_Classe LogicalProgramGroupItem Win32</span><span class="sxs-lookup"><span data-stu-id="fd4d9-103">Win32\_LogicalProgramGroupItem class</span></span>

<span data-ttu-id="fd4d9-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ LogicalProgramGroupItem Win32** représente un élément contenu par [**un \_ LogicalProgramGroup Win32**](win32-logicalprogramgroup.md) qui n’est pas également une autre instance de **\_ LogicalProgramGroup Win32** .</span><span class="sxs-lookup"><span data-stu-id="fd4d9-104">The **Win32\_LogicalProgramGroupItem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an element contained by a [**Win32\_LogicalProgramGroup**](win32-logicalprogramgroup.md) that is not also another **Win32\_LogicalProgramGroup** instance.</span></span>

<span data-ttu-id="fd4d9-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fd4d9-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd4d9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{86E30E82-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItem : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="fd4d9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fd4d9-108">Members</span></span>

<span data-ttu-id="fd4d9-109">La classe **Win32 \_ LogicalProgramGroupItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fd4d9-109">The **Win32\_LogicalProgramGroupItem** class has these types of members:</span></span>

-   [<span data-ttu-id="fd4d9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd4d9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd4d9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd4d9-111">Properties</span></span>

<span data-ttu-id="fd4d9-112">La classe **Win32 \_ LogicalProgramGroupItem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-112">The **Win32\_LogicalProgramGroupItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd4d9-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd4d9-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd4d9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-116">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fd4d9-117">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-117">A short textual description of the object.</span></span>

<span data-ttu-id="fd4d9-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d9-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd4d9-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd4d9-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd4d9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-122">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fd4d9-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fd4d9-123">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-123">A textual description of the object.</span></span>

<span data-ttu-id="fd4d9-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d9-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd4d9-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd4d9-126">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd4d9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="fd4d9-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fd4d9-129">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-129">Indicates when the object was installed.</span></span> <span data-ttu-id="fd4d9-130">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fd4d9-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d9-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd4d9-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd4d9-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd4d9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-135">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="fd4d9-135">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="fd4d9-136">Instance au sein d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-136">Instance within a computer system.</span></span> <span data-ttu-id="fd4d9-137">Les groupes de programmes sont implémentés en tant que dossiers de fichiers dans Win32.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-137">Program groups are implemented as file folders in Win32.</span></span> <span data-ttu-id="fd4d9-138">Les noms de chemin d’accès complets doivent être fournis.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-138">Full path names should be provided.</span></span>

<span data-ttu-id="fd4d9-139">Exemple : « C : \\ Users \\ *quelqu’un* \\ AppData \\ Roaming \\ Microsoft \\ Windows \\ start menu \\ Program \\ Accessories \\ notepad. lnk »</span><span class="sxs-lookup"><span data-stu-id="fd4d9-139">Example: "C:\\Users\\*someone*\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Accessories\\NotePad.Lnk"</span></span>

</dd> <dt>

<span data-ttu-id="fd4d9-140">**État**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd4d9-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fd4d9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd4d9-143">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="fd4d9-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fd4d9-144">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="fd4d9-145">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fd4d9-146">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="fd4d9-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fd4d9-147">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="fd4d9-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fd4d9-148">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="fd4d9-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fd4d9-149">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fd4d9-150">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fd4d9-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d9-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fd4d9-152">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd4d9-152">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fd4d9-153">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-153">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fd4d9-154">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-154">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fd4d9-155">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-155">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd4d9-156">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="fd4d9-156">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fd4d9-157">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-157">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fd4d9-158">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-158">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fd4d9-159">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-159">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fd4d9-160">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-160">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fd4d9-161">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-161">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fd4d9-162">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-162">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fd4d9-163">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-163">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fd4d9-164">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="fd4d9-164">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="fd4d9-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fd4d9-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="fd4d9-166">Notes</span><span class="sxs-lookup"><span data-stu-id="fd4d9-166">Remarks</span></span>

<span data-ttu-id="fd4d9-167">La classe **Win32 \_ LogicalProgramGroupItem** est dérivée de [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="fd4d9-167">The **Win32\_LogicalProgramGroupItem** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="fd4d9-168">Le processus appelant qui utilise cette classe doit avoir le privilège **se \_ Restore \_ Name** sur l’ordinateur où se trouve le registre.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-168">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="fd4d9-169">Par exemple, si vous énumérez cette classe sur l’ordinateur local, le compte sous lequel votre application s’exécute doit disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="fd4d9-169">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="fd4d9-170">Pour plus d’informations, consultez [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="fd4d9-170">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd4d9-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd4d9-171">Requirements</span></span>



| <span data-ttu-id="fd4d9-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd4d9-172">Requirement</span></span> | <span data-ttu-id="fd4d9-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd4d9-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd4d9-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd4d9-174">Minimum supported client</span></span><br/> | <span data-ttu-id="fd4d9-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd4d9-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd4d9-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd4d9-176">Minimum supported server</span></span><br/> | <span data-ttu-id="fd4d9-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd4d9-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd4d9-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fd4d9-178">Namespace</span></span><br/>                | <span data-ttu-id="fd4d9-179">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fd4d9-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd4d9-180">MOF</span><span class="sxs-lookup"><span data-stu-id="fd4d9-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd4d9-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd4d9-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd4d9-182">DLL</span><span class="sxs-lookup"><span data-stu-id="fd4d9-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd4d9-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd4d9-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd4d9-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd4d9-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd4d9-185">**\_ProgramGroupOrItem Win32**</span><span class="sxs-lookup"><span data-stu-id="fd4d9-185">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="fd4d9-186">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd4d9-186">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

