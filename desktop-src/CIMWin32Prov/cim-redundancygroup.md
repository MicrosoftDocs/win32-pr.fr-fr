---
description: La \_ classe REDUNDANCYGROUP CIM représente une collection d’éléments système gérés, qui indique que les composants agrégés, ensemble, fournissent une redondance.
ms.assetid: b47899cc-eafc-431f-96d4-edb01bf4bcd1
ms.tgt_platform: multiple
title: Classe CIM_RedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyGroup
- CIM_RedundancyGroup.Caption
- CIM_RedundancyGroup.Description
- CIM_RedundancyGroup.InstallDate
- CIM_RedundancyGroup.Name
- CIM_RedundancyGroup.Status
- CIM_RedundancyGroup.CreationClassName
- CIM_RedundancyGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1394e052b4741dee5b2646c903d83477bfa1ccf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860645"
---
# <a name="cim_redundancygroup-class"></a><span data-ttu-id="b4a9b-103">\_Classe REDUNDANCYGROUP CIM</span><span class="sxs-lookup"><span data-stu-id="b4a9b-103">CIM\_RedundancyGroup class</span></span>

<span data-ttu-id="b4a9b-104">La **classe \_ RedundancyGroup CIM** représente une collection d’éléments système gérés, qui indique que les composants agrégés, ensemble, fournissent une redondance.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-104">The **CIM\_RedundancyGroup** class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="b4a9b-105">Tous les éléments agrégés dans un groupe de redondance doivent être des instanciations de la même classe d’objets.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4a9b-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b4a9b-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b4a9b-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b4a9b-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a9b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4a9b-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C3A040A-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyGroup : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="b4a9b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b4a9b-111">Members</span></span>

<span data-ttu-id="b4a9b-112">La **classe \_ RedundancyGroup CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b4a9b-112">The **CIM\_RedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="b4a9b-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4a9b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4a9b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4a9b-114">Properties</span></span>

<span data-ttu-id="b4a9b-115">La **classe \_ RedundancyGroup CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-115">The **CIM\_RedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4a9b-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a9b-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4a9b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-119">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b4a9b-120">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-120">A short textual description of the object.</span></span>

<span data-ttu-id="b4a9b-121">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4a9b-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a9b-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4a9b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-125">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4a9b-126">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b4a9b-127">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="b4a9b-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a9b-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4a9b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-131">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b4a9b-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b4a9b-132">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-132">A textual description of the object.</span></span>

<span data-ttu-id="b4a9b-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4a9b-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a9b-135">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4a9b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-137">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="b4a9b-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b4a9b-138">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-138">Indicates when the object was installed.</span></span> <span data-ttu-id="b4a9b-139">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b4a9b-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4a9b-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a9b-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4a9b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-144">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b4a9b-144">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b4a9b-145">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-145">Label by which the object is known.</span></span> <span data-ttu-id="b4a9b-146">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-146">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b4a9b-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b4a9b-148">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-148">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a9b-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4a9b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4a9b-151">Informations sur l’état du groupe de redondance.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-151">Information about the state of the redundancy group.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4a9b-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b4a9b-153">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-153">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b4a9b-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b4a9b-155">Autre.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-155">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="b4a9b-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Entièrement redondant** (2)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b4a9b-157">Toute la redondance configurée est disponible.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-157">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="b4a9b-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redondance dégradée** (3)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b4a9b-159">Une quantité réduite de redondance est disponible en raison de défaillances.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-159">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="b4a9b-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redondance perdue** (4)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b4a9b-161">La redondance n’est pas disponible en raison d’un nombre suffisant d’échecs.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-161">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="b4a9b-162">L’échec suivant entraîne une défaillance globale.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-162">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b4a9b-163">**État**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4a9b-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4a9b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4a9b-166">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b4a9b-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b4a9b-167">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-167">String that indicates the current status of the object.</span></span> <span data-ttu-id="b4a9b-168">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-168">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b4a9b-169">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="b4a9b-169">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b4a9b-170">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-170">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b4a9b-171">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="b4a9b-171">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b4a9b-172">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-172">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b4a9b-173">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-173">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b4a9b-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b4a9b-175">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4a9b-175">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b4a9b-176">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-176">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b4a9b-177">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-177">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b4a9b-178">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-178">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b4a9b-179">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="b4a9b-179">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b4a9b-180">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-180">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b4a9b-181">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-181">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b4a9b-182">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-182">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b4a9b-183">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-183">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b4a9b-184">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-184">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b4a9b-185">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-185">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b4a9b-186">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-186">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b4a9b-187">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="b4a9b-187">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b4a9b-188"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b4a9b-188"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b4a9b-189">Notes</span><span class="sxs-lookup"><span data-stu-id="b4a9b-189">Remarks</span></span>

<span data-ttu-id="b4a9b-190">La **classe \_ RedundancyGroup CIM** est dérivée de la [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b4a9b-190">The **CIM\_RedundancyGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="b4a9b-191">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-191">WMI does not implement this class.</span></span>

<span data-ttu-id="b4a9b-192">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b4a9b-193">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b4a9b-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a9b-194">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4a9b-194">Requirements</span></span>



| <span data-ttu-id="b4a9b-195">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4a9b-195">Requirement</span></span> | <span data-ttu-id="b4a9b-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4a9b-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a9b-197">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4a9b-197">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a9b-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4a9b-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4a9b-199">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4a9b-199">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a9b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4a9b-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4a9b-201">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b4a9b-201">Namespace</span></span><br/>                | <span data-ttu-id="b4a9b-202">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b4a9b-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4a9b-203">MOF</span><span class="sxs-lookup"><span data-stu-id="b4a9b-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4a9b-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4a9b-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4a9b-205">DLL</span><span class="sxs-lookup"><span data-stu-id="b4a9b-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4a9b-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4a9b-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a9b-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4a9b-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a9b-208">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b4a9b-208">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

