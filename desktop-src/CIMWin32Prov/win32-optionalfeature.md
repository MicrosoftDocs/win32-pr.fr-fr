---
description: Représente l’état des fonctionnalités facultatives présentes sur le système d’exploitation.
ms.assetid: 3ac0c227-dfe1-4f33-b3d1-bcd1309c3635
ms.tgt_platform: multiple
title: Classe Win32_OptionalFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OptionalFeature
- Win32_OptionalFeature.Description
- Win32_OptionalFeature.InstallDate
- Win32_OptionalFeature.Status
- Win32_OptionalFeature.Caption
- Win32_OptionalFeature.Name
- Win32_OptionalFeature.InstallState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ee0a8fc631430401328170f15c0dd2653d0ce8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544593"
---
# <a name="win32_optionalfeature-class"></a><span data-ttu-id="e9fc9-103">\_Classe OptionalFeature Win32</span><span class="sxs-lookup"><span data-stu-id="e9fc9-103">Win32\_OptionalFeature class</span></span>

<span data-ttu-id="e9fc9-104">Représente l’état des fonctionnalités facultatives présentes sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-104">Represents the status of the optional features that are present on the operating system.</span></span>

<span data-ttu-id="e9fc9-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9fc9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9fc9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A2}"), AMENDMENT]
class Win32_OptionalFeature : CIM_LogicalElement
{
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Caption;
  string   Name;
  uint32   InstallState;
};
```

## <a name="members"></a><span data-ttu-id="e9fc9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e9fc9-107">Members</span></span>

<span data-ttu-id="e9fc9-108">La classe **Win32 \_ OptionalFeature** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e9fc9-108">The **Win32\_OptionalFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="e9fc9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9fc9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9fc9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9fc9-110">Properties</span></span>

<span data-ttu-id="e9fc9-111">La classe **Win32 \_ OptionalFeature** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-111">The **Win32\_OptionalFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9fc9-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9fc9-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9fc9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-115">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="e9fc9-116">Nom complet d’une fonctionnalité facultative.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-116">An optional feature display name.</span></span>

</dd> <dt>

<span data-ttu-id="e9fc9-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9fc9-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9fc9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-120">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e9fc9-120">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e9fc9-121">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-121">A textual description of the object.</span></span>

<span data-ttu-id="e9fc9-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9fc9-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9fc9-123">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-123">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9fc9-124">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9fc9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-126">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="e9fc9-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e9fc9-127">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-127">Indicates when the object was installed.</span></span> <span data-ttu-id="e9fc9-128">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-128">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e9fc9-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9fc9-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9fc9-130">**InstallState**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-130">**InstallState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9fc9-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9fc9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9fc9-133">Identifie l’état de la fonctionnalité facultative.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-133">Identifies the state of the optional feature.</span></span> <span data-ttu-id="e9fc9-134">Les États suivants sont possibles :</span><span class="sxs-lookup"><span data-stu-id="e9fc9-134">The following states are possible:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e9fc9-135">**Activé** (1)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-135">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e9fc9-136">**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-136">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>

<span data-ttu-id="e9fc9-137">**Absent** (3)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-137">**Absent** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9fc9-138">**Inconnu** (4)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-138">**Unknown** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9fc9-139">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9fc9-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9fc9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-142">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (Name), [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-142">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Name), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="e9fc9-143">Représente le nom de la fonctionnalité facultative.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-143">Represents the name of the optional feature.</span></span>

</dd> <dt>

<span data-ttu-id="e9fc9-144">**État**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9fc9-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9fc9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9fc9-147">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e9fc9-147">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e9fc9-148">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="e9fc9-149">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e9fc9-150">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="e9fc9-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e9fc9-151">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="e9fc9-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e9fc9-152">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e9fc9-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e9fc9-153">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e9fc9-154">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e9fc9-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e9fc9-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9fc9-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e9fc9-156">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9fc9-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e9fc9-157">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e9fc9-158">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e9fc9-159">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9fc9-160">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e9fc9-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e9fc9-161">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e9fc9-162">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e9fc9-163">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e9fc9-164">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e9fc9-165">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e9fc9-166">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e9fc9-167">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e9fc9-168">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="e9fc9-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="e9fc9-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e9fc9-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e9fc9-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9fc9-170">Requirements</span></span>



| <span data-ttu-id="e9fc9-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9fc9-171">Requirement</span></span> | <span data-ttu-id="e9fc9-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9fc9-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9fc9-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9fc9-173">Minimum supported client</span></span><br/> | <span data-ttu-id="e9fc9-174">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9fc9-174">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e9fc9-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9fc9-175">Minimum supported server</span></span><br/> | <span data-ttu-id="e9fc9-176">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9fc9-176">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e9fc9-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e9fc9-177">Namespace</span></span><br/>                | <span data-ttu-id="e9fc9-178">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e9fc9-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9fc9-179">MOF</span><span class="sxs-lookup"><span data-stu-id="e9fc9-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9fc9-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9fc9-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9fc9-181">DLL</span><span class="sxs-lookup"><span data-stu-id="e9fc9-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9fc9-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9fc9-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9fc9-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9fc9-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9fc9-184">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-184">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="e9fc9-185">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e9fc9-185">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="e9fc9-186">Interrogation de l’état des fonctionnalités facultatives</span><span class="sxs-lookup"><span data-stu-id="e9fc9-186">Querying the Status of Optional Features</span></span>](../wmisdk/querying-the-status-of-optional-features.md)
</dt> </dl>

 

 
