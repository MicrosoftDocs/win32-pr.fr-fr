---
description: La \_ classe CIM JobDestination représente l’emplacement où un travail est soumis pour traitement.
ms.assetid: ad2a037d-a5d3-4422-972d-8ef10699bb60
ms.tgt_platform: multiple
title: Classe CIM_JobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestination
- CIM_JobDestination.Caption
- CIM_JobDestination.Description
- CIM_JobDestination.InstallDate
- CIM_JobDestination.Name
- CIM_JobDestination.Status
- CIM_JobDestination.CreationClassName
- CIM_JobDestination.SystemCreationClassName
- CIM_JobDestination.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d01fbe3b6025795084bf0af4cca3d644fd3cf4a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861241"
---
# <a name="cim_jobdestination-class"></a><span data-ttu-id="e9750-103">\_Classe CIM JobDestination</span><span class="sxs-lookup"><span data-stu-id="e9750-103">CIM\_JobDestination class</span></span>

<span data-ttu-id="e9750-104">La classe **CIM \_ JobDestination** représente l’emplacement où un travail est soumis pour traitement.</span><span class="sxs-lookup"><span data-stu-id="e9750-104">The **CIM\_JobDestination** class represents where a job is submitted for processing.</span></span> <span data-ttu-id="e9750-105">Il peut faire référence à une file d’attente qui contient zéro travail ou plus, tel qu’une file d’attente à l’impression contenant des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="e9750-105">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="e9750-106">Les destinations des travaux sont hébergées sur des systèmes, de la même façon que les services sont hébergés sur les systèmes.</span><span class="sxs-lookup"><span data-stu-id="e9750-106">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9750-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e9750-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e9750-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e9750-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e9750-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e9750-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e9750-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e9750-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9750-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9750-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{673E0A2C-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestination : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="e9750-112">Membres</span><span class="sxs-lookup"><span data-stu-id="e9750-112">Members</span></span>

<span data-ttu-id="e9750-113">La classe **CIM \_ JobDestination** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e9750-113">The **CIM\_JobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="e9750-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9750-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9750-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9750-115">Properties</span></span>

<span data-ttu-id="e9750-116">La classe **CIM \_ JobDestination** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e9750-116">The **CIM\_JobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9750-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e9750-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9750-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="e9750-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e9750-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9750-121">A short textual description of the object.</span></span>

<span data-ttu-id="e9750-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9750-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9750-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e9750-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9750-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-126">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e9750-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e9750-127">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="e9750-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e9750-128">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="e9750-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="e9750-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="e9750-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9750-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-132">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e9750-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e9750-133">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9750-133">A textual description of the object.</span></span>

<span data-ttu-id="e9750-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9750-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9750-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e9750-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-136">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9750-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="e9750-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e9750-139">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="e9750-139">Indicates when the object was installed.</span></span> <span data-ttu-id="e9750-140">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="e9750-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e9750-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9750-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9750-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e9750-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9750-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-145">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e9750-145">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e9750-146">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="e9750-146">Label by which the object is known.</span></span> <span data-ttu-id="e9750-147">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="e9750-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e9750-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9750-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9750-149">**État**</span><span class="sxs-lookup"><span data-stu-id="e9750-149">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9750-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-152">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e9750-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e9750-153">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9750-153">String that indicates the current status of the object.</span></span> <span data-ttu-id="e9750-154">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="e9750-154">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e9750-155">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="e9750-155">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e9750-156">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="e9750-156">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e9750-157">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e9750-157">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e9750-158">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e9750-158">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e9750-159">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e9750-159">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e9750-160">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9750-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e9750-161">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9750-161">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e9750-162">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="e9750-162">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e9750-163">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="e9750-163">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e9750-164">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e9750-164">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9750-165">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e9750-165">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e9750-166">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e9750-166">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e9750-167">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e9750-167">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e9750-168">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e9750-168">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e9750-169">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="e9750-169">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e9750-170">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="e9750-170">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e9750-171">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="e9750-171">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e9750-172">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="e9750-172">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e9750-173">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="e9750-173">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9750-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e9750-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9750-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-177">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="e9750-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="e9750-178">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e9750-178">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="e9750-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e9750-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9750-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e9750-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9750-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e9750-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9750-182">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="e9750-182">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="e9750-183">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e9750-183">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9750-184">Notes</span><span class="sxs-lookup"><span data-stu-id="e9750-184">Remarks</span></span>

<span data-ttu-id="e9750-185">La classe **CIM \_ JobDestination** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e9750-185">The **CIM\_JobDestination** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="e9750-186">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e9750-186">WMI does not implement this class.</span></span>

<span data-ttu-id="e9750-187">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e9750-187">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e9750-188">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e9750-188">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9750-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9750-189">Requirements</span></span>



| <span data-ttu-id="e9750-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9750-190">Requirement</span></span> | <span data-ttu-id="e9750-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9750-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9750-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9750-192">Minimum supported client</span></span><br/> | <span data-ttu-id="e9750-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9750-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9750-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9750-194">Minimum supported server</span></span><br/> | <span data-ttu-id="e9750-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9750-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9750-196">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e9750-196">Namespace</span></span><br/>                | <span data-ttu-id="e9750-197">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e9750-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9750-198">MOF</span><span class="sxs-lookup"><span data-stu-id="e9750-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9750-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9750-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9750-200">DLL</span><span class="sxs-lookup"><span data-stu-id="e9750-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9750-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9750-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9750-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9750-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9750-203">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e9750-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

