---
description: Représente un nœud NUMA (non-Uniform Memory Access) d’un système virtuel.
ms.assetid: a2e9aa74-15e5-4a78-b7f8-ffe2883a31d0
title: Classe Msvm_NumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NumaNode
- Msvm_NumaNode.RequestStateChange
- Msvm_NumaNode.InstanceID
- Msvm_NumaNode.Caption
- Msvm_NumaNode.Description
- Msvm_NumaNode.ElementName
- Msvm_NumaNode.InstallDate
- Msvm_NumaNode.Name
- Msvm_NumaNode.OperationalStatus
- Msvm_NumaNode.StatusDescriptions
- Msvm_NumaNode.Status
- Msvm_NumaNode.HealthState
- Msvm_NumaNode.CommunicationStatus
- Msvm_NumaNode.DetailedStatus
- Msvm_NumaNode.OperatingStatus
- Msvm_NumaNode.PrimaryStatus
- Msvm_NumaNode.EnabledState
- Msvm_NumaNode.OtherEnabledState
- Msvm_NumaNode.RequestedState
- Msvm_NumaNode.EnabledDefault
- Msvm_NumaNode.TimeOfLastStateChange
- Msvm_NumaNode.AvailableRequestedStates
- Msvm_NumaNode.TransitioningToState
- Msvm_NumaNode.SystemCreationClassName
- Msvm_NumaNode.SystemName
- Msvm_NumaNode.CreationClassName
- Msvm_NumaNode.NodeID
- Msvm_NumaNode.NumberOfProcessorCores
- Msvm_NumaNode.NumberOfLogicalProcessors
- Msvm_NumaNode.CurrentlyConsumableMemoryBlocks
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4bdbd600cd4a78f66376f21ee264b2dfe9854147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526940"
---
# <a name="msvm_numanode-class"></a><span data-ttu-id="f1039-103">MSVM \_ NumaNode, classe</span><span class="sxs-lookup"><span data-stu-id="f1039-103">Msvm\_NumaNode class</span></span>

<span data-ttu-id="f1039-104">Représente un nœud NUMA (non-Uniform Memory Access) d’un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="f1039-104">Represents a Non-Uniform Memory Access (NUMA) node of a virtual system.</span></span>

<span data-ttu-id="f1039-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f1039-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1039-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1039-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_NumaNode : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NodeID;
  uint32   NumberOfProcessorCores;
  uint32   NumberOfLogicalProcessors;
  uint64   CurrentlyConsumableMemoryBlocks;
};
```

## <a name="members"></a><span data-ttu-id="f1039-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f1039-107">Members</span></span>

<span data-ttu-id="f1039-108">La classe **MSVM \_ NumaNode** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1039-108">The **Msvm\_NumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="f1039-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f1039-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1039-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1039-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1039-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f1039-111">Methods</span></span>

<span data-ttu-id="f1039-112">La classe **MSVM \_ NumaNode** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f1039-112">The **Msvm\_NumaNode** class has these methods.</span></span>



| <span data-ttu-id="f1039-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="f1039-113">Method</span></span>                 | <span data-ttu-id="f1039-114">Description</span><span class="sxs-lookup"><span data-stu-id="f1039-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="f1039-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f1039-115">**RequestStateChange**</span></span> | <span data-ttu-id="f1039-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f1039-116">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1039-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f1039-117">Properties</span></span>

<span data-ttu-id="f1039-118">La classe **MSVM \_ NumaNode** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1039-118">The **Msvm\_NumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1039-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f1039-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-120">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1039-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-122">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f1039-122">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f1039-123">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1039-123">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f1039-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-127">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1039-127">A short description of the object.</span></span> <span data-ttu-id="f1039-128">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f1039-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-132">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="f1039-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f1039-133">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f1039-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1039-134">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1039-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f1039-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="f1039-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="f1039-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="f1039-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="f1039-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f1039-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f1039-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1039-142">)</span><span class="sxs-lookup"><span data-stu-id="f1039-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1039-143">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1039-143">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1039-146">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f1039-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f1039-147">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f1039-147">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-148">**CurrentlyConsumableMemoryBlocks**</span><span class="sxs-lookup"><span data-stu-id="f1039-148">**CurrentlyConsumableMemoryBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-149">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1039-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-151">Nombre de blocs de mémoire actuellement disponibles pour la consommation par les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="f1039-151">The number of memory blocks currently available for consumption by virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-152">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1039-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-155">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="f1039-155">A description of the object.</span></span> <span data-ttu-id="f1039-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f1039-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-158">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-160">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f1039-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f1039-161">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f1039-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1039-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1039-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="f1039-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="f1039-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="f1039-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="f1039-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="f1039-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="f1039-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f1039-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f1039-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1039-171">)</span><span class="sxs-lookup"><span data-stu-id="f1039-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1039-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f1039-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-175">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1039-175">A display name for the object.</span></span> <span data-ttu-id="f1039-176">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-177">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f1039-177">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-178">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-180">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="f1039-180">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="f1039-181">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1039-181">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-182">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f1039-182">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-183">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-185">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="f1039-185">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f1039-186">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="f1039-186">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="f1039-187">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1039-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f1039-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1039-188">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="f1039-189">Signification</span><span class="sxs-lookup"><span data-stu-id="f1039-189">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="f1039-190"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-190"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="f1039-191">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f1039-191">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="f1039-192"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-192"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="f1039-193"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-193"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="f1039-194">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f1039-194">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="f1039-195"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-195"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="f1039-196">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f1039-196">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="f1039-197"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-197"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="f1039-198">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="f1039-198">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="f1039-199"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="f1039-200">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="f1039-200">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="f1039-201"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="f1039-202">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="f1039-202">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="f1039-203"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-203"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="f1039-204">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="f1039-204">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="f1039-205"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-205"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="f1039-206">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="f1039-206">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="f1039-207"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-207"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="f1039-208">L’élément est activé, mais il est en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="f1039-208">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="f1039-209">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="f1039-209">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="f1039-210">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f1039-210">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="f1039-211">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-211"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="f1039-212">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="f1039-212">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="f1039-213">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f1039-213">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="f1039-214">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f1039-214">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-215">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-217">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f1039-217">The current health of the element.</span></span> <span data-ttu-id="f1039-218">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="f1039-218">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f1039-219">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="f1039-219">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f1039-220">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="f1039-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-221">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1039-221">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-222">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1039-222">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-224">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f1039-224">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f1039-225">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-226">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1039-226">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1039-229">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f1039-229">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f1039-230">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="f1039-230">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f1039-231">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-232">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f1039-232">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-235">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="f1039-235">The label by which the object is known.</span></span> <span data-ttu-id="f1039-236">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-237">**ID**</span><span class="sxs-lookup"><span data-stu-id="f1039-237">**NodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-238">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1039-240">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1039-240">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1039-241">Identificateur du nœud NUMA.</span><span class="sxs-lookup"><span data-stu-id="f1039-241">The NUMA node identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-242">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="f1039-242">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-243">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1039-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-245">Nombre total de cœurs de processeurs logiques dans ce nœud.</span><span class="sxs-lookup"><span data-stu-id="f1039-245">The total number of logical processor cores in this node.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-246">**NumberOfProcessorCores**</span><span class="sxs-lookup"><span data-stu-id="f1039-246">**NumberOfProcessorCores**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-247">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1039-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-249">Nombre total de cœurs de processeur dans ce nœud NUMA.</span><span class="sxs-lookup"><span data-stu-id="f1039-249">The total number of processor cores in this NUMA node.</span></span> <span data-ttu-id="f1039-250">Cela peut être différent du nombre d' [**objets \_ processeur MSVM**](msvm-processor.md) associés à ce nœud si chaque cœur de processeur prend en charge plusieurs threads de calcul.</span><span class="sxs-lookup"><span data-stu-id="f1039-250">This may differ from the number of [**Msvm\_Processor**](msvm-processor.md) objects associated to this node if each processor core supports multiple compute threads.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-251">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f1039-251">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-252">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-254">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f1039-254">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f1039-255">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f1039-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1039-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1039-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f1039-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="f1039-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="f1039-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="f1039-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="f1039-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="f1039-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="f1039-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="f1039-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="f1039-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="f1039-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="f1039-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="f1039-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="f1039-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="f1039-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="f1039-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="f1039-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="f1039-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f1039-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f1039-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1039-276">)</span><span class="sxs-lookup"><span data-stu-id="f1039-276">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1039-277">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f1039-277">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-278">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-278">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1039-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-280">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1039-280">The current statuses of the object.</span></span> <span data-ttu-id="f1039-281">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-282">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f1039-282">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-283">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-285">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="f1039-285">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f1039-286">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="f1039-286">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="f1039-287">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="f1039-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-288">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f1039-288">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-289">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-291">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="f1039-291">Provides high level status information.</span></span> <span data-ttu-id="f1039-292">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="f1039-292">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f1039-293">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="f1039-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1039-294">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1039-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="f1039-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="f1039-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="f1039-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="f1039-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f1039-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1039-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="f1039-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1039-301">)</span><span class="sxs-lookup"><span data-stu-id="f1039-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1039-302">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f1039-302">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-303">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-305">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="f1039-305">The last requested or desired state for the element.</span></span> <span data-ttu-id="f1039-306">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="f1039-306">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="f1039-307">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="f1039-307">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="f1039-308">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f1039-308">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="f1039-309">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f1039-309">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="f1039-310">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="f1039-310">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-311">**État**</span><span class="sxs-lookup"><span data-stu-id="f1039-311">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f1039-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-315">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f1039-315">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-316">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="f1039-316">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1039-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-318">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f1039-318">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f1039-319">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f1039-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1039-320">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1039-320">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1039-323">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="f1039-323">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="f1039-324">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f1039-324">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-325">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f1039-325">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1039-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1039-328">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="f1039-328">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="f1039-329">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="f1039-329">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="f1039-330">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f1039-330">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-331">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1039-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-333">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f1039-333">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f1039-334">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur « null ».</span><span class="sxs-lookup"><span data-stu-id="f1039-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="f1039-335">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f1039-335">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1039-336">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1039-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1039-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f1039-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1039-338">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="f1039-338">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f1039-339">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1039-339">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1039-340">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1039-340">Requirements</span></span>



| <span data-ttu-id="f1039-341">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1039-341">Requirement</span></span> | <span data-ttu-id="f1039-342">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1039-342">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1039-343">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1039-343">Minimum supported client</span></span><br/> | <span data-ttu-id="f1039-344">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1039-344">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1039-345">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1039-345">Minimum supported server</span></span><br/> | <span data-ttu-id="f1039-346">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1039-346">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1039-347">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1039-347">Namespace</span></span><br/>                | <span data-ttu-id="f1039-348">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1039-348">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1039-349">MOF</span><span class="sxs-lookup"><span data-stu-id="f1039-349">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1039-350"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-350"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1039-351">DLL</span><span class="sxs-lookup"><span data-stu-id="f1039-351">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1039-352"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1039-352"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

