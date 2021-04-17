---
description: La \_ classe CIM ServiceAccessPoint représente la possibilité d’utiliser ou d’appeler un service. Les points d’accès représentent les services qui peuvent être utilisés par d’autres entités.
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: CIM_ServiceAccessPoint, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 681e5e11de525e535f7965b72adb8ac0e316f7aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523484"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="6195c-104">CIM_ServiceAccessPoint, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6195c-104">CIM_ServiceAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6195c-105">La classe **CIM \_ ServiceAccessPoint** représente la possibilité d’utiliser ou d’appeler un service.</span><span class="sxs-lookup"><span data-stu-id="6195c-105">The **CIM\_ServiceAccessPoint** class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="6195c-106">Les points d’accès représentent les services qui peuvent être utilisés par d’autres entités.</span><span class="sxs-lookup"><span data-stu-id="6195c-106">Access points represent services that are available for use by other entities.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6195c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6195c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6195c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6195c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6195c-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6195c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6195c-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6195c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6195c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6195c-111">Syntax</span></span>

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="6195c-112">Membres</span><span class="sxs-lookup"><span data-stu-id="6195c-112">Members</span></span>

<span data-ttu-id="6195c-113">La classe **CIM \_ ServiceAccessPoint** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6195c-113">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="6195c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6195c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6195c-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6195c-115">Properties</span></span>

<span data-ttu-id="6195c-116">La classe **CIM \_ ServiceAccessPoint** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6195c-116">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6195c-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6195c-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6195c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="6195c-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6195c-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6195c-121">A short textual description of the object.</span></span>

<span data-ttu-id="6195c-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6195c-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6195c-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6195c-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6195c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-126">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6195c-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6195c-127">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6195c-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6195c-128">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="6195c-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="6195c-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="6195c-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6195c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-132">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6195c-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6195c-133">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6195c-133">A textual description of the object.</span></span>

<span data-ttu-id="6195c-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6195c-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6195c-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6195c-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-136">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6195c-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-138">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="6195c-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6195c-139">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="6195c-139">Indicates when the object was installed.</span></span> <span data-ttu-id="6195c-140">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="6195c-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6195c-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6195c-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6195c-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6195c-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6195c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-145">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6195c-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6195c-146">Identifie de façon unique le point d’accès au service et fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="6195c-146">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="6195c-147">Cette fonctionnalité est décrite plus en détail dans la propriété Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6195c-147">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="6195c-148">**État**</span><span class="sxs-lookup"><span data-stu-id="6195c-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6195c-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6195c-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6195c-152">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6195c-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="6195c-153">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="6195c-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6195c-154">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="6195c-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6195c-155">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="6195c-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6195c-156">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="6195c-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6195c-157">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="6195c-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6195c-158">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="6195c-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6195c-159">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6195c-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6195c-160">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6195c-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6195c-161">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="6195c-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6195c-162">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="6195c-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6195c-163">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6195c-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6195c-164">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="6195c-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6195c-165">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6195c-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6195c-166">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6195c-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6195c-167">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6195c-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6195c-168">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="6195c-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6195c-169">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="6195c-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6195c-170">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="6195c-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6195c-171">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="6195c-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6195c-172">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="6195c-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6195c-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6195c-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6195c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-176">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6195c-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6195c-177">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6195c-177">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="6195c-178">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6195c-178">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6195c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-181">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6195c-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6195c-182">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6195c-182">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="6195c-183">**Type**</span><span class="sxs-lookup"><span data-stu-id="6195c-183">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6195c-184">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6195c-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6195c-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6195c-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6195c-186">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6195c-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6195c-187">Type de SAP, tel que attaché ou redirigé.</span><span class="sxs-lookup"><span data-stu-id="6195c-187">Type of SAP, such as attached or redirected.</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="6195c-188">**Écriture** (1)</span><span class="sxs-lookup"><span data-stu-id="6195c-188">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="6195c-189">**Lecture** (2)</span><span class="sxs-lookup"><span data-stu-id="6195c-189">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="6195c-190">**Redirigé** (4)</span><span class="sxs-lookup"><span data-stu-id="6195c-190">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="6195c-191">**Réseau \_ Attaché** (8)</span><span class="sxs-lookup"><span data-stu-id="6195c-191">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6195c-192">**inconnu** (16)</span><span class="sxs-lookup"><span data-stu-id="6195c-192">**unknown** (16)</span></span>


<span data-ttu-id="6195c-193"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6195c-193"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6195c-194">Notes</span><span class="sxs-lookup"><span data-stu-id="6195c-194">Remarks</span></span>

<span data-ttu-id="6195c-195">La classe **CIM \_ ServiceAccessPoint** est dérivée de la [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6195c-195">The **CIM\_ServiceAccessPoint** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="6195c-196">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6195c-196">WMI does not implement this class.</span></span> <span data-ttu-id="6195c-197">Pour les classes WMI dérivées de **CIM \_ ServiceAccessPoint**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6195c-197">For WMI classes derived from **CIM\_ServiceAccessPoint**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6195c-198">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6195c-198">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6195c-199">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6195c-199">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6195c-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6195c-200">Requirements</span></span>



| <span data-ttu-id="6195c-201">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6195c-201">Requirement</span></span> | <span data-ttu-id="6195c-202">Valeur</span><span class="sxs-lookup"><span data-stu-id="6195c-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6195c-203">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6195c-203">Minimum supported client</span></span><br/> | <span data-ttu-id="6195c-204">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6195c-204">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6195c-205">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6195c-205">Minimum supported server</span></span><br/> | <span data-ttu-id="6195c-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6195c-206">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6195c-207">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6195c-207">Namespace</span></span><br/>                | <span data-ttu-id="6195c-208">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6195c-208">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6195c-209">MOF</span><span class="sxs-lookup"><span data-stu-id="6195c-209">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6195c-210"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6195c-210"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6195c-211">DLL</span><span class="sxs-lookup"><span data-stu-id="6195c-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6195c-212"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6195c-212"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6195c-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6195c-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6195c-214">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6195c-214">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

