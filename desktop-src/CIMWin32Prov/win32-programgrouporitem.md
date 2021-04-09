---
description: La \_ classe WMI ProgramGroupOrItem abstraite Win32 représente un regroupement logique de programmes dans le menu démarrer des programmes de l’utilisateur \\ . Il contient les groupes de programmes et les éléments de groupe de programmes.
ms.assetid: 48ec5436-e931-4f00-ab36-03b04ad33529
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupOrItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupOrItem
- Win32_ProgramGroupOrItem.Caption
- Win32_ProgramGroupOrItem.Description
- Win32_ProgramGroupOrItem.InstallDate
- Win32_ProgramGroupOrItem.Name
- Win32_ProgramGroupOrItem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb12576acbc8b50befa5d0856343b61e325b9478
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110226"
---
# <a name="win32_programgrouporitem-class"></a><span data-ttu-id="31053-104">\_Classe ProgramGroupOrItem Win32</span><span class="sxs-lookup"><span data-stu-id="31053-104">Win32\_ProgramGroupOrItem class</span></span>

<span data-ttu-id="31053-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ProgramGroupOrItem** abstraite Win32 représente un regroupement logique de programmes dans le menu **Démarrer des \\ programmes** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31053-105">The **Win32\_ProgramGroupOrItem** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a logical grouping of programs on the user's **Start\\Programs** menu.</span></span> <span data-ttu-id="31053-106">Il contient les groupes de programmes et les éléments de groupe de programmes.</span><span class="sxs-lookup"><span data-stu-id="31053-106">It contains program groups and program group items.</span></span>

<span data-ttu-id="31053-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="31053-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="31053-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="31053-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31053-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31053-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{86E30E86-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupOrItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="31053-110">Membres</span><span class="sxs-lookup"><span data-stu-id="31053-110">Members</span></span>

<span data-ttu-id="31053-111">La classe **Win32 \_ ProgramGroupOrItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="31053-111">The **Win32\_ProgramGroupOrItem** class has these types of members:</span></span>

-   [<span data-ttu-id="31053-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31053-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31053-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="31053-113">Properties</span></span>

<span data-ttu-id="31053-114">La classe **Win32 \_ ProgramGroupOrItem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="31053-114">The **Win32\_ProgramGroupOrItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31053-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="31053-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31053-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31053-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31053-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31053-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31053-118">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="31053-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="31053-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31053-119">A short textual description of the object.</span></span>

<span data-ttu-id="31053-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31053-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31053-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="31053-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31053-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31053-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31053-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31053-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31053-124">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="31053-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="31053-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31053-125">A textual description of the object.</span></span>

<span data-ttu-id="31053-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31053-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31053-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31053-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31053-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="31053-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31053-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31053-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31053-130">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="31053-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="31053-131">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="31053-131">Indicates when the object was installed.</span></span> <span data-ttu-id="31053-132">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="31053-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="31053-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31053-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31053-134">**Nom**</span><span class="sxs-lookup"><span data-stu-id="31053-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31053-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31053-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31053-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31053-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31053-137">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="31053-137">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="31053-138">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="31053-138">Label by which the object is known.</span></span> <span data-ttu-id="31053-139">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="31053-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="31053-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31053-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31053-141">**État**</span><span class="sxs-lookup"><span data-stu-id="31053-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31053-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="31053-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31053-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="31053-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31053-144">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="31053-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="31053-145">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31053-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="31053-146">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="31053-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="31053-147">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="31053-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="31053-148">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="31053-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="31053-149">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="31053-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="31053-150">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="31053-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="31053-151">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="31053-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="31053-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31053-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="31053-153">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="31053-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="31053-154">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="31053-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="31053-155">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="31053-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31053-156">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="31053-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31053-157">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="31053-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="31053-158">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="31053-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="31053-159">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="31053-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="31053-160">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="31053-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="31053-161">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="31053-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="31053-162">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="31053-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="31053-163">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="31053-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="31053-164">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="31053-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="31053-165">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="31053-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="31053-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="31053-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="31053-167">Notes</span><span class="sxs-lookup"><span data-stu-id="31053-167">Remarks</span></span>

<span data-ttu-id="31053-168">La classe **Win32 \_ ProgramGroupOrItem** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="31053-168">The **Win32\_ProgramGroupOrItem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31053-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31053-169">Requirements</span></span>



| <span data-ttu-id="31053-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31053-170">Requirement</span></span> | <span data-ttu-id="31053-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="31053-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31053-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31053-172">Minimum supported client</span></span><br/> | <span data-ttu-id="31053-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31053-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31053-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31053-174">Minimum supported server</span></span><br/> | <span data-ttu-id="31053-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31053-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31053-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="31053-176">Namespace</span></span><br/>                | <span data-ttu-id="31053-177">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="31053-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31053-178">MOF</span><span class="sxs-lookup"><span data-stu-id="31053-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31053-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31053-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31053-180">DLL</span><span class="sxs-lookup"><span data-stu-id="31053-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31053-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31053-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31053-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31053-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31053-183">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="31053-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="31053-184">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="31053-184">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
