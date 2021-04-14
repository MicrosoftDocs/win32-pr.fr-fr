---
description: La \_ classe CIM SystemResource représente une entité gérée par le BIOS, ou un système d’exploitation qui peut être utilisé par des périphériques logiciels et logiques.
ms.assetid: f232c940-532d-4723-8e1e-09f983664b84
ms.tgt_platform: multiple
title: Classe CIM_SystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemResource
- CIM_SystemResource.Caption
- CIM_SystemResource.Description
- CIM_SystemResource.InstallDate
- CIM_SystemResource.Name
- CIM_SystemResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0c111aa0d69119a7d9182732fb18dd5109d3dde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201046"
---
# <a name="cim_systemresource-class"></a><span data-ttu-id="545ea-103">\_Classe CIM SystemResource</span><span class="sxs-lookup"><span data-stu-id="545ea-103">CIM\_SystemResource class</span></span>

<span data-ttu-id="545ea-104">La classe **CIM \_ SystemResource** représente une entité gérée par le BIOS, ou un système d’exploitation qui peut être utilisé par des périphériques logiciels et logiques.</span><span class="sxs-lookup"><span data-stu-id="545ea-104">The **CIM\_SystemResource** class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="545ea-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="545ea-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="545ea-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="545ea-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="545ea-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="545ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="545ea-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="545ea-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="545ea-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="545ea-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C519-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SystemResource : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="545ea-110">Membres</span><span class="sxs-lookup"><span data-stu-id="545ea-110">Members</span></span>

<span data-ttu-id="545ea-111">La classe **CIM \_ SystemResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="545ea-111">The **CIM\_SystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="545ea-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="545ea-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="545ea-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="545ea-113">Properties</span></span>

<span data-ttu-id="545ea-114">La classe **CIM \_ SystemResource** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="545ea-114">The **CIM\_SystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="545ea-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="545ea-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="545ea-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="545ea-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="545ea-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="545ea-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="545ea-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="545ea-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="545ea-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="545ea-119">A short textual description of the object.</span></span>

<span data-ttu-id="545ea-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="545ea-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="545ea-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="545ea-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="545ea-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="545ea-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="545ea-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="545ea-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="545ea-124">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="545ea-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="545ea-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="545ea-125">A textual description of the object.</span></span>

<span data-ttu-id="545ea-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="545ea-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="545ea-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="545ea-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="545ea-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="545ea-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="545ea-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="545ea-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="545ea-130">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="545ea-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="545ea-131">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="545ea-131">Indicates when the object was installed.</span></span> <span data-ttu-id="545ea-132">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="545ea-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="545ea-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="545ea-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="545ea-134">**Nom**</span><span class="sxs-lookup"><span data-stu-id="545ea-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="545ea-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="545ea-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="545ea-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="545ea-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="545ea-137">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="545ea-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="545ea-138">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="545ea-138">Label by which the object is known.</span></span> <span data-ttu-id="545ea-139">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="545ea-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="545ea-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="545ea-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="545ea-141">**État**</span><span class="sxs-lookup"><span data-stu-id="545ea-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="545ea-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="545ea-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="545ea-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="545ea-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="545ea-144">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="545ea-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="545ea-145">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="545ea-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="545ea-146">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="545ea-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="545ea-147">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="545ea-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="545ea-148">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="545ea-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="545ea-149">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="545ea-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="545ea-150">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="545ea-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="545ea-151">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="545ea-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="545ea-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="545ea-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="545ea-153">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="545ea-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="545ea-154">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="545ea-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="545ea-155">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="545ea-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="545ea-156">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="545ea-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="545ea-157">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="545ea-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="545ea-158">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="545ea-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="545ea-159">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="545ea-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="545ea-160">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="545ea-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="545ea-161">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="545ea-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="545ea-162">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="545ea-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="545ea-163">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="545ea-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="545ea-164">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="545ea-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="545ea-165">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="545ea-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="545ea-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="545ea-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="545ea-167">Notes</span><span class="sxs-lookup"><span data-stu-id="545ea-167">Remarks</span></span>

<span data-ttu-id="545ea-168">La classe **CIM \_ SystemResource** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="545ea-168">The **CIM\_SystemResource** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="545ea-169">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="545ea-169">WMI does not implement this class.</span></span> <span data-ttu-id="545ea-170">Pour les classes WMI dérivées de **CIM \_ SystemResource**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="545ea-170">For WMI classes derived from **CIM\_SystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="545ea-171">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="545ea-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="545ea-172">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="545ea-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="545ea-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="545ea-173">Requirements</span></span>



| <span data-ttu-id="545ea-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="545ea-174">Requirement</span></span> | <span data-ttu-id="545ea-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="545ea-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="545ea-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="545ea-176">Minimum supported client</span></span><br/> | <span data-ttu-id="545ea-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="545ea-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="545ea-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="545ea-178">Minimum supported server</span></span><br/> | <span data-ttu-id="545ea-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="545ea-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="545ea-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="545ea-180">Namespace</span></span><br/>                | <span data-ttu-id="545ea-181">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="545ea-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="545ea-182">MOF</span><span class="sxs-lookup"><span data-stu-id="545ea-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="545ea-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="545ea-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="545ea-184">DLL</span><span class="sxs-lookup"><span data-stu-id="545ea-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="545ea-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="545ea-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="545ea-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="545ea-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545ea-187">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="545ea-187">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

