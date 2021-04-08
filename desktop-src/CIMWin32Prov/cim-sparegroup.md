---
description: La \_ classe CIM SpareGroup est dérivée de la \_ classe CIM RedundancyGroup et indique qu’un ou plusieurs éléments agrégés peuvent être détachés.
ms.assetid: e60f8cab-a9e8-4f5a-b8d7-833c7832ef7e
ms.tgt_platform: multiple
title: Classe CIM_SpareGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SpareGroup
- CIM_SpareGroup.Caption
- CIM_SpareGroup.Description
- CIM_SpareGroup.InstallDate
- CIM_SpareGroup.Name
- CIM_SpareGroup.Status
- CIM_SpareGroup.CreationClassName
- CIM_SpareGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 17907c62ace9f75c8d807e56d35b91f4c28e5f42
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747829"
---
# <a name="cim_sparegroup-class"></a><span data-ttu-id="fba1d-103">\_Classe CIM SpareGroup</span><span class="sxs-lookup"><span data-stu-id="fba1d-103">CIM\_SpareGroup class</span></span>

<span data-ttu-id="fba1d-104">La classe **CIM \_ SpareGroup** est dérivée de la classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) et indique qu’un ou plusieurs éléments agrégés peuvent être détachés.</span><span class="sxs-lookup"><span data-stu-id="fba1d-104">The **CIM\_SpareGroup** class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span> <span data-ttu-id="fba1d-105">Les pièces de rechange sont définies à l’aide de l’Association [**CIM \_ ActsAsSpare**](cim-actsasspare.md) .</span><span class="sxs-lookup"><span data-stu-id="fba1d-105">Spares are defined using the [**CIM\_ActsAsSpare**](cim-actsasspare.md) association.</span></span> <span data-ttu-id="fba1d-106">Un exemple de rechange est l’utilisation de cartes réseau redondantes dans un système informatique, où une carte réseau est principale et l’autre un Spare.</span><span class="sxs-lookup"><span data-stu-id="fba1d-106">An example of a spare is the use of redundant NICs in a computer system, where one NIC is primary and the other is spare.</span></span> <span data-ttu-id="fba1d-107">La carte réseau principale est un membre du groupe Spare, associé à l’aide de la classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) , et l’autre carte réseau est associée à l’aide de la relation **CIM \_ ActsAsSpare** .</span><span class="sxs-lookup"><span data-stu-id="fba1d-107">The primary NIC would be a member of the spare group, associated using the [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class, and the other NIC would be associated using the **CIM\_ActsAsSpare** relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fba1d-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="fba1d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fba1d-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fba1d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fba1d-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fba1d-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fba1d-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fba1d-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba1d-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fba1d-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{64B86CA6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SpareGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
};
```

## <a name="members"></a><span data-ttu-id="fba1d-113">Membres</span><span class="sxs-lookup"><span data-stu-id="fba1d-113">Members</span></span>

<span data-ttu-id="fba1d-114">La classe **CIM \_ SpareGroup** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fba1d-114">The **CIM\_SpareGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="fba1d-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fba1d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fba1d-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fba1d-116">Properties</span></span>

<span data-ttu-id="fba1d-117">La classe **CIM \_ SpareGroup** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fba1d-117">The **CIM\_SpareGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fba1d-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fba1d-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba1d-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fba1d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fba1d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fba1d-122">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fba1d-122">A short textual description of the object.</span></span>

<span data-ttu-id="fba1d-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba1d-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fba1d-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba1d-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fba1d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fba1d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-127">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fba1d-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fba1d-128">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="fba1d-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fba1d-129">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="fba1d-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="fba1d-130">Cette propriété est héritée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba1d-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="fba1d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba1d-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fba1d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fba1d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-134">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fba1d-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fba1d-135">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fba1d-135">A textual description of the object.</span></span>

<span data-ttu-id="fba1d-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba1d-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fba1d-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba1d-138">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fba1d-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fba1d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="fba1d-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fba1d-141">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="fba1d-141">Indicates when the object was installed.</span></span> <span data-ttu-id="fba1d-142">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="fba1d-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fba1d-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba1d-144">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fba1d-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba1d-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fba1d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fba1d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-147">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fba1d-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fba1d-148">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="fba1d-148">Label by which the object is known.</span></span> <span data-ttu-id="fba1d-149">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="fba1d-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fba1d-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fba1d-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="fba1d-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba1d-152">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fba1d-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fba1d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fba1d-154">Informations sur l’état du groupe de redondance.</span><span class="sxs-lookup"><span data-stu-id="fba1d-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="fba1d-155">Cette propriété est héritée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fba1d-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="fba1d-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fba1d-157">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="fba1d-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fba1d-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="fba1d-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fba1d-159">Autre.</span><span class="sxs-lookup"><span data-stu-id="fba1d-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="fba1d-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Entièrement redondant** (2)</span><span class="sxs-lookup"><span data-stu-id="fba1d-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fba1d-161">Toute la redondance configurée est disponible.</span><span class="sxs-lookup"><span data-stu-id="fba1d-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="fba1d-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redondance dégradée** (3)</span><span class="sxs-lookup"><span data-stu-id="fba1d-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fba1d-163">Une quantité réduite de redondance est disponible en raison de défaillances.</span><span class="sxs-lookup"><span data-stu-id="fba1d-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="fba1d-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redondance perdue** (4)</span><span class="sxs-lookup"><span data-stu-id="fba1d-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fba1d-165">La redondance n’est pas disponible en raison d’un nombre suffisant d’échecs.</span><span class="sxs-lookup"><span data-stu-id="fba1d-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="fba1d-166">L’échec suivant entraîne une défaillance globale.</span><span class="sxs-lookup"><span data-stu-id="fba1d-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fba1d-167">**État**</span><span class="sxs-lookup"><span data-stu-id="fba1d-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba1d-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fba1d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fba1d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba1d-170">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="fba1d-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fba1d-171">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fba1d-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="fba1d-172">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="fba1d-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fba1d-173">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="fba1d-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fba1d-174">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="fba1d-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fba1d-175">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="fba1d-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fba1d-176">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="fba1d-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fba1d-177">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="fba1d-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fba1d-178">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fba1d-179">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fba1d-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fba1d-180">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fba1d-181">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fba1d-182">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fba1d-183">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="fba1d-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fba1d-184">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fba1d-185">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fba1d-186">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fba1d-187">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fba1d-188">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fba1d-189">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fba1d-190">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fba1d-191">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="fba1d-191">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="fba1d-192"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fba1d-192"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="fba1d-193">Notes</span><span class="sxs-lookup"><span data-stu-id="fba1d-193">Remarks</span></span>

<span data-ttu-id="fba1d-194">La classe **CIM \_ SpareGroup** est dérivée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="fba1d-194">The **CIM\_SpareGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="fba1d-195">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="fba1d-195">WMI does not implement this class.</span></span>

<span data-ttu-id="fba1d-196">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="fba1d-196">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fba1d-197">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fba1d-197">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba1d-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fba1d-198">Requirements</span></span>



| <span data-ttu-id="fba1d-199">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fba1d-199">Requirement</span></span> | <span data-ttu-id="fba1d-200">Valeur</span><span class="sxs-lookup"><span data-stu-id="fba1d-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fba1d-201">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba1d-201">Minimum supported client</span></span><br/> | <span data-ttu-id="fba1d-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fba1d-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fba1d-203">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba1d-203">Minimum supported server</span></span><br/> | <span data-ttu-id="fba1d-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fba1d-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fba1d-205">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fba1d-205">Namespace</span></span><br/>                | <span data-ttu-id="fba1d-206">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fba1d-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fba1d-207">MOF</span><span class="sxs-lookup"><span data-stu-id="fba1d-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba1d-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba1d-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba1d-209">DLL</span><span class="sxs-lookup"><span data-stu-id="fba1d-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba1d-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba1d-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba1d-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fba1d-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba1d-212">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="fba1d-212">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

