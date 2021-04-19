---
description: La \_ classe CIM BootSAP représente les points d’accès d’un service de démarrage.
ms.assetid: eea6d6c5-3930-4e20-b7d3-b6d5722662cd
ms.tgt_platform: multiple
title: Classe CIM_BootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootSAP
- CIM_BootSAP.Caption
- CIM_BootSAP.Description
- CIM_BootSAP.InstallDate
- CIM_BootSAP.Status
- CIM_BootSAP.CreationClassName
- CIM_BootSAP.Name
- CIM_BootSAP.SystemCreationClassName
- CIM_BootSAP.SystemName
- CIM_BootSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4868497c2d604457a45273b1c0cc609ae361ad9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513147"
---
# <a name="cim_bootsap-class"></a><span data-ttu-id="79dff-103">\_Classe CIM BootSAP</span><span class="sxs-lookup"><span data-stu-id="79dff-103">CIM\_BootSAP class</span></span>

<span data-ttu-id="79dff-104">La classe **CIM \_ BootSAP** représente les points d’accès d’un service de démarrage.</span><span class="sxs-lookup"><span data-stu-id="79dff-104">The **CIM\_BootSAP** class represents the access points of a boot service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79dff-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="79dff-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="79dff-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="79dff-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="79dff-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="79dff-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="79dff-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="79dff-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="79dff-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79dff-109">Syntax</span></span>

``` syntax
[UUID("{F6FEF20A-E3D2-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootSAP : CIM_ServiceAccessPoint
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

## <a name="members"></a><span data-ttu-id="79dff-110">Membres</span><span class="sxs-lookup"><span data-stu-id="79dff-110">Members</span></span>

<span data-ttu-id="79dff-111">La classe **CIM \_ BootSAP** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="79dff-111">The **CIM\_BootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="79dff-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79dff-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79dff-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="79dff-113">Properties</span></span>

<span data-ttu-id="79dff-114">La classe **CIM \_ BootSAP** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="79dff-114">The **CIM\_BootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79dff-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="79dff-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79dff-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="79dff-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="79dff-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79dff-119">A short textual description of the object.</span></span>

<span data-ttu-id="79dff-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79dff-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79dff-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79dff-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-124">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="79dff-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="79dff-125">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="79dff-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="79dff-126">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="79dff-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="79dff-127">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="79dff-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="79dff-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79dff-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-131">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="79dff-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="79dff-132">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79dff-132">A textual description of the object.</span></span>

<span data-ttu-id="79dff-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79dff-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="79dff-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-135">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79dff-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-137">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="79dff-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="79dff-138">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="79dff-138">Indicates when the object was installed.</span></span> <span data-ttu-id="79dff-139">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="79dff-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="79dff-140">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79dff-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="79dff-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79dff-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-144">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="79dff-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="79dff-145">Identifie de façon unique le point d’accès au service et fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="79dff-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="79dff-146">Cette fonctionnalité est décrite plus en détail dans la propriété Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79dff-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="79dff-147">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="79dff-148">**État**</span><span class="sxs-lookup"><span data-stu-id="79dff-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79dff-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-151">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="79dff-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="79dff-152">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79dff-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="79dff-153">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="79dff-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="79dff-154">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="79dff-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="79dff-155">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="79dff-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="79dff-156">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="79dff-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="79dff-157">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="79dff-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="79dff-158">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="79dff-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="79dff-159">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="79dff-160">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="79dff-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="79dff-161">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="79dff-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="79dff-162">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="79dff-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="79dff-163">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="79dff-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79dff-164">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="79dff-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="79dff-165">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="79dff-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="79dff-166">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="79dff-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="79dff-167">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="79dff-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="79dff-168">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="79dff-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="79dff-169">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="79dff-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="79dff-170">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="79dff-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="79dff-171">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="79dff-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="79dff-172">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="79dff-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79dff-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79dff-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79dff-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-176">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="79dff-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="79dff-177">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="79dff-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="79dff-178">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="79dff-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="79dff-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="79dff-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-182">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="79dff-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="79dff-183">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="79dff-183">The scoping system's name.</span></span>

<span data-ttu-id="79dff-184">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="79dff-185">**Type**</span><span class="sxs-lookup"><span data-stu-id="79dff-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79dff-186">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79dff-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79dff-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="79dff-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79dff-188">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="79dff-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="79dff-189">Type de SAP, tel que attaché ou redirigé.</span><span class="sxs-lookup"><span data-stu-id="79dff-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="79dff-190">Cette propriété est héritée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="79dff-191">**Écriture** (1)</span><span class="sxs-lookup"><span data-stu-id="79dff-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="79dff-192">**Lecture** (2)</span><span class="sxs-lookup"><span data-stu-id="79dff-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="79dff-193">**Redirigé** (4)</span><span class="sxs-lookup"><span data-stu-id="79dff-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="79dff-194">**Réseau \_ Attaché** (8)</span><span class="sxs-lookup"><span data-stu-id="79dff-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79dff-195">**inconnu** (16)</span><span class="sxs-lookup"><span data-stu-id="79dff-195">**unknown** (16)</span></span>


<span data-ttu-id="79dff-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79dff-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="79dff-197">Notes</span><span class="sxs-lookup"><span data-stu-id="79dff-197">Remarks</span></span>

<span data-ttu-id="79dff-198">La classe **CIM \_ BootSAP** est dérivée de [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="79dff-198">The **CIM\_BootSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="79dff-199">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="79dff-199">WMI does not implement this class.</span></span>

<span data-ttu-id="79dff-200">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="79dff-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="79dff-201">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="79dff-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="79dff-202">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79dff-202">Requirements</span></span>



| <span data-ttu-id="79dff-203">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79dff-203">Requirement</span></span> | <span data-ttu-id="79dff-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="79dff-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79dff-205">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79dff-205">Minimum supported client</span></span><br/> | <span data-ttu-id="79dff-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79dff-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79dff-207">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79dff-207">Minimum supported server</span></span><br/> | <span data-ttu-id="79dff-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79dff-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79dff-209">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="79dff-209">Namespace</span></span><br/>                | <span data-ttu-id="79dff-210">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="79dff-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79dff-211">MOF</span><span class="sxs-lookup"><span data-stu-id="79dff-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79dff-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79dff-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79dff-213">DLL</span><span class="sxs-lookup"><span data-stu-id="79dff-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79dff-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79dff-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79dff-215">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79dff-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79dff-216">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="79dff-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

