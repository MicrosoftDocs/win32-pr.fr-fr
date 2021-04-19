---
description: La \_ classe CIM ClusteringService représente la fonctionnalité fournie par un cluster. Par exemple, la fonctionnalité de basculement peut être modélisée en tant que service d’un cluster de basculement.
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: Classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 40dc0ebd8daebb79c323d54591fc16126e0ef97a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544585"
---
# <a name="cim_clusteringservice-class"></a><span data-ttu-id="19b96-104">\_Classe CIM ClusteringService</span><span class="sxs-lookup"><span data-stu-id="19b96-104">CIM\_ClusteringService class</span></span>

<span data-ttu-id="19b96-105">La classe **CIM \_ ClusteringService** représente la fonctionnalité fournie par un cluster.</span><span class="sxs-lookup"><span data-stu-id="19b96-105">The **CIM\_ClusteringService** class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="19b96-106">Par exemple, la fonctionnalité de basculement peut être modélisée en tant que service d’un cluster de basculement.</span><span class="sxs-lookup"><span data-stu-id="19b96-106">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19b96-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="19b96-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="19b96-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="19b96-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="19b96-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="19b96-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="19b96-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="19b96-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b96-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19b96-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="19b96-112">Membres</span><span class="sxs-lookup"><span data-stu-id="19b96-112">Members</span></span>

<span data-ttu-id="19b96-113">La classe **CIM \_ ClusteringService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="19b96-113">The **CIM\_ClusteringService** class has these types of members:</span></span>

-   [<span data-ttu-id="19b96-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19b96-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="19b96-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19b96-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="19b96-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="19b96-116">Methods</span></span>

<span data-ttu-id="19b96-117">La classe **CIM \_ ClusteringService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="19b96-117">The **CIM\_ClusteringService** class has these methods.</span></span>



| <span data-ttu-id="19b96-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="19b96-118">Method</span></span>                                                                     | <span data-ttu-id="19b96-119">Description</span><span class="sxs-lookup"><span data-stu-id="19b96-119">Description</span></span>                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19b96-120">**AddNode**</span><span class="sxs-lookup"><span data-stu-id="19b96-120">**AddNode**</span></span>](addnode-method-in-class-cim-clusteringservice.md)           | <span data-ttu-id="19b96-121">Méthode de classe qui introduit un nouveau système informatique dans un cluster.</span><span class="sxs-lookup"><span data-stu-id="19b96-121">Class method that brings a new computer system into a cluster.</span></span> <span data-ttu-id="19b96-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="19b96-122">Not implemented by WMI.</span></span><br/>          |
| [<span data-ttu-id="19b96-123">**EvictNode**</span><span class="sxs-lookup"><span data-stu-id="19b96-123">**EvictNode**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)       | <span data-ttu-id="19b96-124">Méthode de la classe qui supprime un système informatique d’un cluster.</span><span class="sxs-lookup"><span data-stu-id="19b96-124">Class method that removes a computer system from a cluster.</span></span> <span data-ttu-id="19b96-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="19b96-125">Not implemented by WMI.</span></span><br/>             |
| [<span data-ttu-id="19b96-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="19b96-126">**StartService**</span></span>](startservice-method-in-class-cim-clusteringservice.md) | <span data-ttu-id="19b96-127">Méthode de classe qui tente de placer le service dans son état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="19b96-127">Class method that attempts to place the service into its startup state.</span></span> <span data-ttu-id="19b96-128">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="19b96-128">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="19b96-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="19b96-129">**StopService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)   | <span data-ttu-id="19b96-130">Méthode de classe qui place le service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="19b96-130">Class method that places the service in the stopped state.</span></span> <span data-ttu-id="19b96-131">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="19b96-131">Not implemented by WMI.</span></span><br/>              |



 

### <a name="properties"></a><span data-ttu-id="19b96-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19b96-132">Properties</span></span>

<span data-ttu-id="19b96-133">La classe **CIM \_ ClusteringService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="19b96-133">The **CIM\_ClusteringService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19b96-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="19b96-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-137">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="19b96-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-138">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="19b96-138">A short textual description of the object.</span></span>

<span data-ttu-id="19b96-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b96-140">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="19b96-140">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-143">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="19b96-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-144">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="19b96-144">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="19b96-145">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="19b96-145">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="19b96-146">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-146">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b96-147">**Description**</span><span class="sxs-lookup"><span data-stu-id="19b96-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-150">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="19b96-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-151">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="19b96-151">A textual description of the object.</span></span>

<span data-ttu-id="19b96-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b96-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="19b96-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-154">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="19b96-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-156">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="19b96-156">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-157">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="19b96-157">Indicates when the object was installed.</span></span> <span data-ttu-id="19b96-158">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="19b96-158">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="19b96-159">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b96-160">**Nom**</span><span class="sxs-lookup"><span data-stu-id="19b96-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-163">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19b96-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19b96-164">La propriété Name identifie de façon unique le service et fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="19b96-164">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="19b96-165">Cette fonctionnalité est décrite plus en détail dans la propriété Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="19b96-165">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="19b96-166">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-166">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b96-167">**Cours**</span><span class="sxs-lookup"><span data-stu-id="19b96-167">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-168">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="19b96-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-170">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="19b96-170">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-171">Si la **valeur est true**, le service a démarré.</span><span class="sxs-lookup"><span data-stu-id="19b96-171">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="19b96-172">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-172">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b96-173">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="19b96-173">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-176">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« mode de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="19b96-176">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-177">Indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="19b96-177">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="19b96-178">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-178">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="19b96-179">**Automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="19b96-179">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="19b96-180">**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="19b96-180">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19b96-181">**État**</span><span class="sxs-lookup"><span data-stu-id="19b96-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-184">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="19b96-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-185">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="19b96-185">String that indicates the current status of the object.</span></span> <span data-ttu-id="19b96-186">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="19b96-186">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="19b96-187">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="19b96-187">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="19b96-188">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="19b96-188">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="19b96-189">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="19b96-189">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="19b96-190">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="19b96-190">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="19b96-191">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="19b96-191">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="19b96-192">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="19b96-193">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="19b96-193">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="19b96-194">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="19b96-194">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="19b96-195">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="19b96-195">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="19b96-196">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="19b96-196">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="19b96-197">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="19b96-197">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="19b96-198">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="19b96-198">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="19b96-199">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="19b96-199">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="19b96-200">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="19b96-200">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="19b96-201">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="19b96-201">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="19b96-202">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="19b96-202">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="19b96-203">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="19b96-203">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="19b96-204">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="19b96-204">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="19b96-205">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="19b96-205">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="19b96-206">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="19b96-206">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-209">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="19b96-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-210">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="19b96-210">Scoping system's creation class name.</span></span>

<span data-ttu-id="19b96-211">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-211">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b96-212">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="19b96-212">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19b96-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="19b96-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19b96-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19b96-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19b96-215">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="19b96-215">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="19b96-216">Nom du système qui héberge le service.</span><span class="sxs-lookup"><span data-stu-id="19b96-216">Name of the system that hosts the service.</span></span>

<span data-ttu-id="19b96-217">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-217">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19b96-218">Notes</span><span class="sxs-lookup"><span data-stu-id="19b96-218">Remarks</span></span>

<span data-ttu-id="19b96-219">La classe **CIM \_ ClusteringService** est dérivée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="19b96-219">The **CIM\_ClusteringService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="19b96-220">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="19b96-220">WMI does not implement this class.</span></span>

<span data-ttu-id="19b96-221">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="19b96-221">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="19b96-222">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="19b96-222">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="19b96-223">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19b96-223">Requirements</span></span>



| <span data-ttu-id="19b96-224">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19b96-224">Requirement</span></span> | <span data-ttu-id="19b96-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="19b96-225">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19b96-226">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19b96-226">Minimum supported client</span></span><br/> | <span data-ttu-id="19b96-227">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19b96-227">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19b96-228">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19b96-228">Minimum supported server</span></span><br/> | <span data-ttu-id="19b96-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19b96-229">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19b96-230">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="19b96-230">Namespace</span></span><br/>                | <span data-ttu-id="19b96-231">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="19b96-231">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19b96-232">MOF</span><span class="sxs-lookup"><span data-stu-id="19b96-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19b96-233"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19b96-233"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19b96-234">DLL</span><span class="sxs-lookup"><span data-stu-id="19b96-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b96-235"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b96-235"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19b96-236">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19b96-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b96-237">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="19b96-237">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

