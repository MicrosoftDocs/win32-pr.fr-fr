---
description: Représente un événement déclenché chaque fois que la propriété OperationalStatus de la classe MSVM \_ ResourcePool ou MSVM \_ LogicalDisk change.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Classe Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034800"
---
# <a name="msvm_storagealert-class"></a><span data-ttu-id="83c71-103">MSVM \_ StorageAlert, classe</span><span class="sxs-lookup"><span data-stu-id="83c71-103">Msvm\_StorageAlert class</span></span>

<span data-ttu-id="83c71-104">Représente un événement déclenché chaque fois que la propriété **OperationalStatus** de la classe [**MSVM \_ ResourcePool**](msvm-resourcepool.md) ou [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) change.</span><span class="sxs-lookup"><span data-stu-id="83c71-104">Represents an event that is raised each time the **OperationalStatus** property of the [**Msvm\_ResourcePool**](msvm-resourcepool.md) or [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) class changes.</span></span>

<span data-ttu-id="83c71-105">La syntaxe suivante est simplifiée à partir du code MOF et comprend ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="83c71-105">The following syntax is simplified from MOF code and includes these properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c71-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83c71-106">Syntax</span></span>

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a><span data-ttu-id="83c71-107">Membres</span><span class="sxs-lookup"><span data-stu-id="83c71-107">Members</span></span>

<span data-ttu-id="83c71-108">La classe **MSVM \_ StorageAlert** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="83c71-108">The **Msvm\_StorageAlert** class has these types of members:</span></span>

-   [<span data-ttu-id="83c71-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83c71-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83c71-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="83c71-110">Properties</span></span>

<span data-ttu-id="83c71-111">La classe **MSVM \_ StorageAlert** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="83c71-111">The **Msvm\_StorageAlert** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83c71-112">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="83c71-112">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83c71-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83c71-115">Qualificateurs : **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")</span><span class="sxs-lookup"><span data-stu-id="83c71-115">Qualifiers: **ModelCorrespondence** ("CIM\_AlertIndication.AlertingManagedElement", "CIM\_AlertIndication.OtherAlertingElementFormat")</span></span>
</dt> </dl>

<span data-ttu-id="83c71-116">Spécifie le format de la propriété **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="83c71-116">Specifies the format of the **AlertingManagedElement** property.</span></span> <span data-ttu-id="83c71-117">Le format est un CIMObjectPath, avec le format *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, qui spécifie une instance dans le schéma CIM.</span><span class="sxs-lookup"><span data-stu-id="83c71-117">The format is a CIMObjectPath, with the format *<NamespacePath>:<ClassName>.<Prop1>=\\"<Value1>\\", "<Prop2>=\\"<Value2>\\"*, which specifies an instance in the CIM Schema.</span></span>

<span data-ttu-id="83c71-118">Cette propriété est héritée de la classe **CIM \_ AlertIndication** .</span><span class="sxs-lookup"><span data-stu-id="83c71-118">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

<span data-ttu-id="83c71-119">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="83c71-119">The possible values are:</span></span>

<dl> <dt>

<span data-ttu-id="83c71-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="83c71-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83c71-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="83c71-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="83c71-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="83c71-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83c71-123">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="83c71-123">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-124">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="83c71-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="83c71-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-126">Chemins d’accès WMI de l’instance pour laquelle l’alerte est générée.</span><span class="sxs-lookup"><span data-stu-id="83c71-126">The WMI paths of the instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="83c71-127">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="83c71-127">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83c71-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-130">Spécifie la classification principale de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="83c71-130">Specifies the primary classification of the alert.</span></span> <span data-ttu-id="83c71-131">Les valeurs possibles pour cette propriété sont :</span><span class="sxs-lookup"><span data-stu-id="83c71-131">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="83c71-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerte de qualité de service** (3)</span><span class="sxs-lookup"><span data-stu-id="83c71-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83c71-133">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="83c71-133">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-134">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83c71-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-136">Date et heure de détection de l’événement sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="83c71-136">The date and time at which the underlying event was detected.</span></span>

</dd> <dt>

<span data-ttu-id="83c71-137">**Message**</span><span class="sxs-lookup"><span data-stu-id="83c71-137">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83c71-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-140">Message mis en forme qui est construit en combinant tout ou partie des éléments dynamiques spécifiés dans la propriété **MessageArguments** avec les éléments statiques identifiés de manière unique par la propriété **MessageID** dans un registre de messages ou un autre catalogue associé à la propriété **OwningEntity** .</span><span class="sxs-lookup"><span data-stu-id="83c71-140">A formatted message that is constructed by combining some or all of the dynamic elements that are specified in the **MessageArguments** property with the static elements uniquely identified by the **MessageID** property in a message registry or other catalog associated with the **OwningEntity** property.</span></span>

</dd> <dt>

<span data-ttu-id="83c71-141">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="83c71-141">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-142">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="83c71-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="83c71-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-144">Tableau qui contient le contenu dynamique du message.</span><span class="sxs-lookup"><span data-stu-id="83c71-144">An array that contains the dynamic content of the message.</span></span> <span data-ttu-id="83c71-145">Si la valeur de **MessageID** est 32930, l’argument situé à la position 0 est le **PoolID** de l’instance [**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md) pour laquelle l’alerte est générée.</span><span class="sxs-lookup"><span data-stu-id="83c71-145">If the value of **MessageID** is 32930, the argument at position 0 is the **PoolID** of the [**Msvm\_ResourcePool**](msvm-resourcepoolcomponent.md) instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="83c71-146">**ID**</span><span class="sxs-lookup"><span data-stu-id="83c71-146">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83c71-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-149">Identifie de façon unique, dans l’étendue de la propriété **OwningEntity** , le format de la propriété de **message** .</span><span class="sxs-lookup"><span data-stu-id="83c71-149">Uniquely identifies, within the scope of the **OwningEntity** property, the format of the **Message** property.</span></span> <span data-ttu-id="83c71-150">Les valeurs possibles pour cette propriété sont :</span><span class="sxs-lookup"><span data-stu-id="83c71-150">The possible values for this property are:</span></span>

<span data-ttu-id="83c71-151">32930 (message « volume de débit (QoS) du pool de stockage insuffisant »)</span><span class="sxs-lookup"><span data-stu-id="83c71-151">32930 ("Storage Pool QoS Insufficient Throughput Message")</span></span>

</dd> <dt>

<span data-ttu-id="83c71-152">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="83c71-152">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83c71-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-155">Chaîne qui définit les valeurs « Other » pour **AlertingManagedElement**.</span><span class="sxs-lookup"><span data-stu-id="83c71-155">A string that defines "Other" values for **AlertingManagedElement**.</span></span> <span data-ttu-id="83c71-156">Cette valeur doit être définie sur une valeur non NULL lorsque **AlertingManagedElement** est défini sur une valeur de 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="83c71-156">This value MUST be set to a non NULL value when **AlertingManagedElement** is set to a value of 1 ("Other").</span></span> <span data-ttu-id="83c71-157">Pour toutes les autres valeurs de **AlertingManagedElement**, la valeur de cette chaîne doit être définie sur null.</span><span class="sxs-lookup"><span data-stu-id="83c71-157">For all other values of **AlertingManagedElement**, the value of this string must be set to NULL.</span></span>

<span data-ttu-id="83c71-158">Cette propriété est héritée de la classe **CIM \_ AlertIndication** .</span><span class="sxs-lookup"><span data-stu-id="83c71-158">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

</dd> <dt>

<span data-ttu-id="83c71-159">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="83c71-159">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83c71-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-162">Identifie de façon unique l’entité qui possède la définition du format du **message** décrit dans cette instance.</span><span class="sxs-lookup"><span data-stu-id="83c71-162">Uniquely identifies the entity that owns the definition of the format of the **Message** described in this instance.</span></span> <span data-ttu-id="83c71-163">La valeur de cette propriété est toujours « Microsoft-Windows-Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="83c71-163">The value of this property is always "Microsoft-Windows- Hyper-V."</span></span>

<span data-ttu-id="83c71-164">« Microsoft-Windows-Hyper-V »</span><span class="sxs-lookup"><span data-stu-id="83c71-164">"Microsoft-Windows- Hyper-V"</span></span>

</dd> <dt>

<span data-ttu-id="83c71-165">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="83c71-165">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-166">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83c71-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-168">Décrit la gravité de l’indication d’alerte.</span><span class="sxs-lookup"><span data-stu-id="83c71-168">Describes the severity of the alert indication.</span></span> <span data-ttu-id="83c71-169">Les valeurs possibles pour cette propriété sont :</span><span class="sxs-lookup"><span data-stu-id="83c71-169">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="83c71-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informations** (2)</span><span class="sxs-lookup"><span data-stu-id="83c71-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83c71-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Détérioré/AVERTISSEMENT** (3)</span><span class="sxs-lookup"><span data-stu-id="83c71-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83c71-172">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="83c71-172">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-173">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83c71-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-175">Décrit la cause probable de la situation qui a entraîné l’indication de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="83c71-175">Describes the probable cause of the situation that resulted in the alert indication.</span></span>

<dl> <dt>

<span data-ttu-id="83c71-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problème de capacité de stockage** (50)</span><span class="sxs-lookup"><span data-stu-id="83c71-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="83c71-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerte précédente effacée** (59)</span><span class="sxs-lookup"><span data-stu-id="83c71-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="83c71-178">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="83c71-178">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83c71-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="83c71-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83c71-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="83c71-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83c71-181">Description textuelle qui correspond à la valeur de la propriété **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="83c71-181">A textual description that corresponds to the value of the **ProbableCause** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83c71-182">Notes</span><span class="sxs-lookup"><span data-stu-id="83c71-182">Remarks</span></span>

<span data-ttu-id="83c71-183">Le fournisseur WMI Hyper-V ne déclenche pas d’événements pour des disques virtuels individuels afin d’éviter d’inonder les clients avec des événements en cas de dysfonctionnements à grande échelle des systèmes de stockage sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="83c71-183">The Hyper-V WMI provider won't raise events for individual virtual disks to avoid flooding clients with events in case of large scale malfunctions of the underlying storage systems.</span></span>

<span data-ttu-id="83c71-184">Lorsqu’un client reçoit un événement **MSVM \_ StorageAlert** , si la valeur de la propriété **ProbableCause** est 50 (problème de capacité de stockage), le client peut détecter les disques virtuels qui fonctionnent en dehors de leur stratégie de QoS à l’aide de l’une des procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="83c71-184">When a client receives an **Msvm\_StorageAlert** event, if the value of the **ProbableCause** property is 50 ( Storage Capacity Problem ), the client can discover which virtual disks are operating outside their QoS policy by using one of these procedures:</span></span>

-   <span data-ttu-id="83c71-185">Interrogez toutes les instances de [**\_ disque logique MSVM**](msvm-logicaldisk.md) allouées à partir du pool de ressources pour lequel l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="83c71-185">Query all the [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) instances that were allocated from the resource pool for which the event was generated.</span></span> <span data-ttu-id="83c71-186">Ces instances de **\_ disque logique MSVM** sont associées au pool de ressources via l’Association [**MSVM \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) .</span><span class="sxs-lookup"><span data-stu-id="83c71-186">These **Msvm\_LogicalDisk** instances are associated to the resource pool via the [**Msvm\_ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) association.</span></span>
-   <span data-ttu-id="83c71-187">Filtrez la liste des résultats en sélectionnant les instances dont OperationalStatus contient un débit insuffisant.</span><span class="sxs-lookup"><span data-stu-id="83c71-187">Filter the result list by selecting instances whose OperationalStatus contains  Insufficient Throughput .</span></span>

## <a name="requirements"></a><span data-ttu-id="83c71-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83c71-188">Requirements</span></span>



| <span data-ttu-id="83c71-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83c71-189">Requirement</span></span> | <span data-ttu-id="83c71-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c71-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c71-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c71-191">Minimum supported client</span></span><br/> | <span data-ttu-id="83c71-192">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83c71-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="83c71-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c71-193">Minimum supported server</span></span><br/> | <span data-ttu-id="83c71-194">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83c71-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="83c71-195">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83c71-195">Namespace</span></span><br/>                | <span data-ttu-id="83c71-196">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="83c71-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="83c71-197">MOF</span><span class="sxs-lookup"><span data-stu-id="83c71-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83c71-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83c71-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83c71-199">DLL</span><span class="sxs-lookup"><span data-stu-id="83c71-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83c71-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83c71-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="83c71-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83c71-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83c71-202">**\_ALERTINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="83c71-202">**CIM\_AlertIndication**</span></span>](cim-alertindication.md)
</dt> <dt>

[<span data-ttu-id="83c71-203">**\_Disque logique MSVM**</span><span class="sxs-lookup"><span data-stu-id="83c71-203">**Msvm\_LogicalDisk**</span></span>](msvm-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="83c71-204">**MSVM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="83c71-204">**Msvm\_ResourcePool**</span></span>](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




