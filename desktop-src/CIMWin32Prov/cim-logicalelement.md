---
description: La \_ classe CIM LogicalElement est la classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.
ms.assetid: 81b2788a-96e8-4570-9a13-d11d229ad789
ms.tgt_platform: multiple
title: CIM_LogicalElement, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 281ba9f97dafb246917d602fcfe1061f4cb03f86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860765"
---
# <a name="cim_logicalelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="da40d-103">CIM_LogicalElement, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="da40d-103">CIM_LogicalElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="da40d-104">La classe **CIM \_ LogicalElement** est la classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="da40d-104">The **CIM\_LogicalElement** class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da40d-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="da40d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="da40d-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="da40d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="da40d-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="da40d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="da40d-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="da40d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="da40d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da40d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Logical Elements (CIM)"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="da40d-110">Membres</span><span class="sxs-lookup"><span data-stu-id="da40d-110">Members</span></span>

<span data-ttu-id="da40d-111">La classe **CIM \_ LogicalElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="da40d-111">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="da40d-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="da40d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da40d-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="da40d-113">Properties</span></span>

<span data-ttu-id="da40d-114">La classe **CIM \_ LogicalElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="da40d-114">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da40d-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="da40d-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da40d-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da40d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da40d-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da40d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da40d-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="da40d-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="da40d-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="da40d-119">A short textual description of the object.</span></span>

<span data-ttu-id="da40d-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da40d-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="da40d-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da40d-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da40d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da40d-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da40d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da40d-124">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="da40d-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="da40d-125">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="da40d-125">A textual description of the object.</span></span>

<span data-ttu-id="da40d-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da40d-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="da40d-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da40d-128">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da40d-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da40d-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da40d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da40d-130">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="da40d-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="da40d-131">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="da40d-131">Indicates when the object was installed.</span></span> <span data-ttu-id="da40d-132">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="da40d-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="da40d-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da40d-134">**Nom**</span><span class="sxs-lookup"><span data-stu-id="da40d-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da40d-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da40d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da40d-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da40d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da40d-137">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="da40d-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="da40d-138">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="da40d-138">Label by which the object is known.</span></span> <span data-ttu-id="da40d-139">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="da40d-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="da40d-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da40d-141">**État**</span><span class="sxs-lookup"><span data-stu-id="da40d-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da40d-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="da40d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da40d-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="da40d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da40d-144">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="da40d-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="da40d-145">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="da40d-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="da40d-146">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="da40d-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="da40d-147">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="da40d-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="da40d-148">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="da40d-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="da40d-149">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="da40d-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="da40d-150">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="da40d-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="da40d-151">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="da40d-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="da40d-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="da40d-153">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="da40d-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="da40d-154">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="da40d-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="da40d-155">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="da40d-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="da40d-156">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="da40d-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="da40d-157">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="da40d-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="da40d-158">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="da40d-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="da40d-159">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="da40d-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="da40d-160">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="da40d-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="da40d-161">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="da40d-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="da40d-162">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="da40d-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="da40d-163">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="da40d-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="da40d-164">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="da40d-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="da40d-165">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="da40d-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="da40d-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="da40d-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="da40d-167">Notes</span><span class="sxs-lookup"><span data-stu-id="da40d-167">Remarks</span></span>

<span data-ttu-id="da40d-168">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="da40d-168">WMI does not implement this class.</span></span> <span data-ttu-id="da40d-169">Pour les classes dérivées de **CIM \_ LogicalElement**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="da40d-169">For classes derived from **CIM\_LogicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="da40d-170">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="da40d-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="da40d-171">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="da40d-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="da40d-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da40d-172">Requirements</span></span>



| <span data-ttu-id="da40d-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da40d-173">Requirement</span></span> | <span data-ttu-id="da40d-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="da40d-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da40d-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da40d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="da40d-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da40d-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da40d-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da40d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="da40d-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da40d-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da40d-179">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="da40d-179">Namespace</span></span><br/>                | <span data-ttu-id="da40d-180">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="da40d-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da40d-181">MOF</span><span class="sxs-lookup"><span data-stu-id="da40d-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da40d-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da40d-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da40d-183">DLL</span><span class="sxs-lookup"><span data-stu-id="da40d-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da40d-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da40d-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da40d-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da40d-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da40d-186">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="da40d-186">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

