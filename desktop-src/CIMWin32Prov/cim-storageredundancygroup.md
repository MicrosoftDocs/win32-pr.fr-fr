---
description: La \_ classe CIM StorageRedundancyGroup représente des informations de redondance relatives au stockage de masse.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: Classe CIM_StorageRedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515919"
---
# <a name="cim_storageredundancygroup-class"></a><span data-ttu-id="0e4ad-103">\_Classe CIM StorageRedundancyGroup</span><span class="sxs-lookup"><span data-stu-id="0e4ad-103">CIM\_StorageRedundancyGroup class</span></span>

<span data-ttu-id="0e4ad-104">La classe **CIM \_ StorageRedundancyGroup** représente des informations de redondance relatives au stockage de masse.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-104">The **CIM\_StorageRedundancyGroup** class represents mass storage-related redundancy information.</span></span> <span data-ttu-id="0e4ad-105">Les groupes de redondance de stockage sont utilisés pour protéger les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-105">Storage redundancy groups are used to protect user data.</span></span> <span data-ttu-id="0e4ad-106">Ils sont constitués d’une ou de plusieurs extensions physiques, ou d’une ou de plusieurs extensions physiques agrégées.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-106">They are made up of one or more physical extents, or one or more aggregate physical extents.</span></span> <span data-ttu-id="0e4ad-107">Les groupes de redondance de stockage peuvent se chevaucher ; Toutefois, les étendues sous-jacentes dans le chevauchement ne doivent pas contenir de données de vérification.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-107">Storage redundancy groups may overlap; however, the underlying extents within the overlap should not contain any check data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e4ad-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0e4ad-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0e4ad-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0e4ad-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e4ad-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e4ad-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a><span data-ttu-id="0e4ad-113">Membres</span><span class="sxs-lookup"><span data-stu-id="0e4ad-113">Members</span></span>

<span data-ttu-id="0e4ad-114">La classe **CIM \_ StorageRedundancyGroup** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e4ad-114">The **CIM\_StorageRedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="0e4ad-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e4ad-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e4ad-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e4ad-116">Properties</span></span>

<span data-ttu-id="0e4ad-117">La classe **CIM \_ StorageRedundancyGroup** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-117">The **CIM\_StorageRedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e4ad-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-122">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-122">A short textual description of the object.</span></span>

<span data-ttu-id="0e4ad-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e4ad-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-127">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-128">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0e4ad-129">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0e4ad-130">Cette propriété est héritée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e4ad-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-134">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0e4ad-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-135">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-135">A textual description of the object.</span></span>

<span data-ttu-id="0e4ad-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e4ad-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-138">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0e4ad-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-141">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-141">Indicates when the object was installed.</span></span> <span data-ttu-id="0e4ad-142">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0e4ad-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e4ad-144">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-147">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0e4ad-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-148">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-148">Label by which the object is known.</span></span> <span data-ttu-id="0e4ad-149">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0e4ad-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e4ad-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-152">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-154">Informations sur l’état du groupe de redondance.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="0e4ad-155">Cette propriété est héritée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e4ad-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e4ad-157">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e4ad-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e4ad-159">Autre.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="0e4ad-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Entièrement redondant** (2)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e4ad-161">Toute la redondance configurée est disponible.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="0e4ad-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redondance dégradée** (3)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e4ad-163">Une quantité réduite de redondance est disponible en raison de défaillances.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="0e4ad-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redondance perdue** (4)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e4ad-165">La redondance n’est pas disponible en raison d’un nombre suffisant d’échecs.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="0e4ad-166">L’échec suivant entraîne une défaillance globale.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e4ad-167">**État**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-170">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0e4ad-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-171">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="0e4ad-172">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0e4ad-173">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="0e4ad-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0e4ad-174">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0e4ad-175">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0e4ad-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0e4ad-176">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0e4ad-177">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0e4ad-178">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0e4ad-179">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e4ad-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0e4ad-180">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0e4ad-181">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e4ad-182">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e4ad-183">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0e4ad-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0e4ad-184">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0e4ad-185">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0e4ad-186">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0e4ad-187">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0e4ad-188">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0e4ad-189">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0e4ad-190">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0e4ad-191">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e4ad-192">**TypeOfAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-192">**TypeOfAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e4ad-193">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e4ad-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e4ad-195">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Groupe de redondance DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="0e4ad-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Redundancy Group\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="0e4ad-196">Algorithme utilisé pour la redondance et la reconstruction des données.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-196">Algorithm used for data redundancy and reconstruction.</span></span> <span data-ttu-id="0e4ad-197">La valeur 0 n’est pas valide dans le schéma CIM, car elle indique qu’il n’existe aucune redondance dans DMI.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-197">The value 0 is not valid in the CIM schema since it represents that no redundancy exists in DMI.</span></span> <span data-ttu-id="0e4ad-198">Dans ce cas, l’objet ne doit pas être instancié.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-198">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="0e4ad-199">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-199">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e4ad-200">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-200">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e4ad-201">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-201">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="0e4ad-202">**Copier** (3)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-202">**Copy** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

<span data-ttu-id="0e4ad-203">**Xor** (4)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-203">**XOR** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

<span data-ttu-id="0e4ad-204">**P + Q** (5)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-204">**P+Q** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

<span data-ttu-id="0e4ad-205">**S** (6)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-205">**S** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

<span data-ttu-id="0e4ad-206">**P + S** (7)</span><span class="sxs-lookup"><span data-stu-id="0e4ad-206">**P+S** (7)</span></span>


<span data-ttu-id="0e4ad-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0e4ad-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0e4ad-208">Notes</span><span class="sxs-lookup"><span data-stu-id="0e4ad-208">Remarks</span></span>

<span data-ttu-id="0e4ad-209">La classe **CIM \_ StorageRedundancyGroup** est dérivée de [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="0e4ad-209">The **CIM\_StorageRedundancyGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="0e4ad-210">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-210">WMI does not implement this class.</span></span>

<span data-ttu-id="0e4ad-211">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-211">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0e4ad-212">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0e4ad-212">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e4ad-213">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e4ad-213">Requirements</span></span>



| <span data-ttu-id="0e4ad-214">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e4ad-214">Requirement</span></span> | <span data-ttu-id="0e4ad-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e4ad-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e4ad-216">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e4ad-216">Minimum supported client</span></span><br/> | <span data-ttu-id="0e4ad-217">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e4ad-217">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e4ad-218">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e4ad-218">Minimum supported server</span></span><br/> | <span data-ttu-id="0e4ad-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e4ad-219">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e4ad-220">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e4ad-220">Namespace</span></span><br/>                | <span data-ttu-id="0e4ad-221">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0e4ad-221">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e4ad-222">MOF</span><span class="sxs-lookup"><span data-stu-id="0e4ad-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e4ad-223"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e4ad-223"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e4ad-224">DLL</span><span class="sxs-lookup"><span data-stu-id="0e4ad-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e4ad-225"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e4ad-225"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e4ad-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e4ad-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e4ad-227">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="0e4ad-227">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

