---
description: La \_ classe MANAGEDSYSTEMELEMENT CIM est la classe de base pour la hiérarchie des éléments système. Tout composant système distinctif est un candidat pour l’inclusion dans cette classe.
ms.assetid: f1b952f4-4bed-4420-ad5d-62478846be8e
ms.tgt_platform: multiple
title: CIM_ManagedSystemElement, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60684d131a034f809a18898ec05ccc5f73f253f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110827"
---
# <a name="cim_managedsystemelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="8194b-104">CIM_ManagedSystemElement, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8194b-104">CIM_ManagedSystemElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8194b-105">La **classe \_ ManagedSystemElement CIM** est la classe de base pour la hiérarchie des éléments système.</span><span class="sxs-lookup"><span data-stu-id="8194b-105">The **CIM\_ManagedSystemElement** class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="8194b-106">Tout composant système distinctif est un candidat pour l’inclusion dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="8194b-106">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="8194b-107">Les exemples incluent des composants logiciels, tels que des fichiers ; appareils, tels que les lecteurs de disque et les contrôleurs ; et les composants physiques, tels que les puces et les cartes.</span><span class="sxs-lookup"><span data-stu-id="8194b-107">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8194b-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8194b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8194b-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8194b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8194b-110">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8194b-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8194b-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8194b-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8194b-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8194b-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Managed System Elements (CIM)"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8194b-113">Membres</span><span class="sxs-lookup"><span data-stu-id="8194b-113">Members</span></span>

<span data-ttu-id="8194b-114">La **classe \_ ManagedSystemElement CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8194b-114">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="8194b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8194b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8194b-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8194b-116">Properties</span></span>

<span data-ttu-id="8194b-117">La **classe \_ ManagedSystemElement CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8194b-117">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8194b-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8194b-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8194b-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8194b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8194b-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8194b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8194b-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="8194b-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8194b-122">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8194b-122">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="8194b-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="8194b-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8194b-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8194b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8194b-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8194b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8194b-126">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8194b-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8194b-127">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8194b-127">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="8194b-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8194b-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8194b-129">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8194b-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8194b-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8194b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8194b-131">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="8194b-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8194b-132">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="8194b-132">Indicates when the object was installed.</span></span> <span data-ttu-id="8194b-133">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="8194b-133">Lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="8194b-134">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8194b-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8194b-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8194b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8194b-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8194b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8194b-137">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8194b-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8194b-138">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="8194b-138">Label by which the object is known.</span></span> <span data-ttu-id="8194b-139">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="8194b-139">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="8194b-140">**État**</span><span class="sxs-lookup"><span data-stu-id="8194b-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8194b-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8194b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8194b-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8194b-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8194b-143">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8194b-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8194b-144">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8194b-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="8194b-145">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="8194b-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8194b-146">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="8194b-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8194b-147">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="8194b-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8194b-148">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="8194b-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8194b-149">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="8194b-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8194b-150">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="8194b-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8194b-151">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8194b-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8194b-152">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="8194b-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8194b-153">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="8194b-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8194b-154">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8194b-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8194b-155">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="8194b-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8194b-156">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8194b-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8194b-157">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8194b-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8194b-158">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8194b-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8194b-159">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="8194b-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8194b-160">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="8194b-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8194b-161">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="8194b-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8194b-162">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="8194b-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8194b-163">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="8194b-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8194b-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8194b-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8194b-165">Notes</span><span class="sxs-lookup"><span data-stu-id="8194b-165">Remarks</span></span>

<span data-ttu-id="8194b-166">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8194b-166">WMI does not implement this class.</span></span> <span data-ttu-id="8194b-167">Pour les classes WMI dérivées de cette classe, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8194b-167">For WMI classes derived from this class, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8194b-168">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8194b-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8194b-169">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8194b-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8194b-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8194b-170">Requirements</span></span>



| <span data-ttu-id="8194b-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8194b-171">Requirement</span></span> | <span data-ttu-id="8194b-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="8194b-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8194b-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8194b-173">Minimum supported client</span></span><br/> | <span data-ttu-id="8194b-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8194b-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8194b-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8194b-175">Minimum supported server</span></span><br/> | <span data-ttu-id="8194b-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8194b-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8194b-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8194b-177">Namespace</span></span><br/>                | <span data-ttu-id="8194b-178">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8194b-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8194b-179">MOF</span><span class="sxs-lookup"><span data-stu-id="8194b-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8194b-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8194b-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8194b-181">DLL</span><span class="sxs-lookup"><span data-stu-id="8194b-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8194b-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8194b-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

