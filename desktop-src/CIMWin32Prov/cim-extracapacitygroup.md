---
description: La \_ classe CIM ExtraCapacityGroup est dérivée d’un groupe de redondance qui indique que les éléments agrégés ont plus de capacité ou de capacité que nécessaire.
ms.assetid: fbbbd6ed-4a67-4917-8b0e-3cba4cac3b45
ms.tgt_platform: multiple
title: Classe CIM_ExtraCapacityGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExtraCapacityGroup
- CIM_ExtraCapacityGroup.Caption
- CIM_ExtraCapacityGroup.Description
- CIM_ExtraCapacityGroup.InstallDate
- CIM_ExtraCapacityGroup.Name
- CIM_ExtraCapacityGroup.Status
- CIM_ExtraCapacityGroup.CreationClassName
- CIM_ExtraCapacityGroup.RedundancyStatus
- CIM_ExtraCapacityGroup.MinNumberNeeded
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78f9aa79cfcc7b93d176859069d1b71f5adf450e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201030"
---
# <a name="cim_extracapacitygroup-class"></a><span data-ttu-id="52934-103">\_Classe CIM ExtraCapacityGroup</span><span class="sxs-lookup"><span data-stu-id="52934-103">CIM\_ExtraCapacityGroup class</span></span>

<span data-ttu-id="52934-104">La classe **CIM \_ ExtraCapacityGroup** est dérivée d’un groupe de redondance qui indique que les éléments agrégés ont plus de capacité ou de capacité que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="52934-104">The **CIM\_ExtraCapacityGroup** class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="52934-105">Voici un exemple de ce type de redondance : l’installation de N + 1 alimentations ou de ventilateurs dans un système.</span><span class="sxs-lookup"><span data-stu-id="52934-105">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52934-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="52934-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="52934-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="52934-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="52934-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="52934-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="52934-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="52934-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="52934-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52934-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{570ED2E8-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ExtraCapacityGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint32   MinNumberNeeded;
};
```

## <a name="members"></a><span data-ttu-id="52934-111">Membres</span><span class="sxs-lookup"><span data-stu-id="52934-111">Members</span></span>

<span data-ttu-id="52934-112">La classe **CIM \_ ExtraCapacityGroup** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="52934-112">The **CIM\_ExtraCapacityGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="52934-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52934-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52934-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52934-114">Properties</span></span>

<span data-ttu-id="52934-115">La classe **CIM \_ ExtraCapacityGroup** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="52934-115">The **CIM\_ExtraCapacityGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52934-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="52934-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52934-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52934-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52934-119">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="52934-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="52934-120">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52934-120">A short textual description of the object.</span></span>

<span data-ttu-id="52934-121">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52934-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52934-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="52934-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52934-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52934-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52934-125">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="52934-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="52934-126">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="52934-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="52934-127">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="52934-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="52934-128">Cette propriété est héritée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="52934-128">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="52934-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="52934-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52934-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52934-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52934-132">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="52934-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="52934-133">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52934-133">A textual description of the object.</span></span>

<span data-ttu-id="52934-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52934-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52934-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="52934-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-136">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52934-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52934-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52934-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="52934-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="52934-139">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="52934-139">Indicates when the object was installed.</span></span> <span data-ttu-id="52934-140">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="52934-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="52934-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52934-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52934-142">**MinNumberNeeded**</span><span class="sxs-lookup"><span data-stu-id="52934-142">**MinNumberNeeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52934-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52934-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52934-145">Plus petit nombre d’éléments qui doivent être opérationnels pour avoir une redondance.</span><span class="sxs-lookup"><span data-stu-id="52934-145">Smallest number of elements that must be operational to have redundancy.</span></span> <span data-ttu-id="52934-146">Par exemple, dans une relation de redondance N + 1, cette propriété doit être définie sur N.</span><span class="sxs-lookup"><span data-stu-id="52934-146">For example, in an N+1 redundancy relationship, this property should be set equal to N.</span></span>

</dd> <dt>

<span data-ttu-id="52934-147">**Nom**</span><span class="sxs-lookup"><span data-stu-id="52934-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52934-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52934-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52934-150">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="52934-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="52934-151">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="52934-151">Label by which the object is known.</span></span> <span data-ttu-id="52934-152">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="52934-152">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="52934-153">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52934-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52934-154">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="52934-154">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-155">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52934-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52934-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52934-157">Informations sur l’état du groupe de redondance.</span><span class="sxs-lookup"><span data-stu-id="52934-157">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="52934-158">Cette propriété est héritée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="52934-158">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52934-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="52934-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="52934-160">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="52934-160">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="52934-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="52934-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52934-162">Autre.</span><span class="sxs-lookup"><span data-stu-id="52934-162">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="52934-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Entièrement redondant** (2)</span><span class="sxs-lookup"><span data-stu-id="52934-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52934-164">Toute la redondance configurée est disponible.</span><span class="sxs-lookup"><span data-stu-id="52934-164">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="52934-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redondance dégradée** (3)</span><span class="sxs-lookup"><span data-stu-id="52934-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="52934-166">Une quantité réduite de redondance est disponible en raison de défaillances.</span><span class="sxs-lookup"><span data-stu-id="52934-166">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="52934-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redondance perdue** (4)</span><span class="sxs-lookup"><span data-stu-id="52934-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="52934-168">La redondance n’est pas disponible en raison d’un nombre suffisant d’échecs.</span><span class="sxs-lookup"><span data-stu-id="52934-168">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="52934-169">L’échec suivant entraîne une défaillance globale.</span><span class="sxs-lookup"><span data-stu-id="52934-169">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52934-170">**État**</span><span class="sxs-lookup"><span data-stu-id="52934-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52934-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52934-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52934-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52934-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52934-173">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="52934-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="52934-174">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52934-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="52934-175">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="52934-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="52934-176">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="52934-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="52934-177">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="52934-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="52934-178">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="52934-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="52934-179">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="52934-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="52934-180">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="52934-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="52934-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52934-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="52934-182">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="52934-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="52934-183">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="52934-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="52934-184">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="52934-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="52934-185">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="52934-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52934-186">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="52934-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="52934-187">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="52934-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="52934-188">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="52934-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="52934-189">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="52934-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="52934-190">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="52934-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="52934-191">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="52934-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="52934-192">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="52934-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="52934-193">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="52934-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="52934-194">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="52934-194">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="52934-195"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="52934-195"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="52934-196">Notes</span><span class="sxs-lookup"><span data-stu-id="52934-196">Remarks</span></span>

<span data-ttu-id="52934-197">La classe **CIM \_ ExtraCapacityGroup** est dérivée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="52934-197">The **CIM\_ExtraCapacityGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="52934-198">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="52934-198">WMI does not implement this class.</span></span>

<span data-ttu-id="52934-199">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="52934-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="52934-200">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="52934-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="52934-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52934-201">Requirements</span></span>



| <span data-ttu-id="52934-202">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52934-202">Requirement</span></span> | <span data-ttu-id="52934-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="52934-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52934-204">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52934-204">Minimum supported client</span></span><br/> | <span data-ttu-id="52934-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52934-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52934-206">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52934-206">Minimum supported server</span></span><br/> | <span data-ttu-id="52934-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52934-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52934-208">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52934-208">Namespace</span></span><br/>                | <span data-ttu-id="52934-209">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="52934-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="52934-210">MOF</span><span class="sxs-lookup"><span data-stu-id="52934-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52934-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52934-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="52934-212">DLL</span><span class="sxs-lookup"><span data-stu-id="52934-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52934-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52934-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52934-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52934-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52934-215">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="52934-215">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

