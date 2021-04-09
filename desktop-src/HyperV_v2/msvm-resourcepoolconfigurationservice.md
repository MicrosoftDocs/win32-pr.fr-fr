---
description: Fournit la gestion active des pools de ressources.
ms.assetid: 34ee3189-cb89-4d36-b12f-333449103968
title: Classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService
- Msvm_ResourcePoolConfigurationService.RequestStateChange
- Msvm_ResourcePoolConfigurationService.StartService
- Msvm_ResourcePoolConfigurationService.StopService
- Msvm_ResourcePoolConfigurationService.InstanceID
- Msvm_ResourcePoolConfigurationService.Caption
- Msvm_ResourcePoolConfigurationService.Description
- Msvm_ResourcePoolConfigurationService.ElementName
- Msvm_ResourcePoolConfigurationService.InstallDate
- Msvm_ResourcePoolConfigurationService.Name
- Msvm_ResourcePoolConfigurationService.OperationalStatus
- Msvm_ResourcePoolConfigurationService.StatusDescriptions
- Msvm_ResourcePoolConfigurationService.Status
- Msvm_ResourcePoolConfigurationService.HealthState
- Msvm_ResourcePoolConfigurationService.CommunicationStatus
- Msvm_ResourcePoolConfigurationService.DetailedStatus
- Msvm_ResourcePoolConfigurationService.OperatingStatus
- Msvm_ResourcePoolConfigurationService.PrimaryStatus
- Msvm_ResourcePoolConfigurationService.EnabledState
- Msvm_ResourcePoolConfigurationService.OtherEnabledState
- Msvm_ResourcePoolConfigurationService.RequestedState
- Msvm_ResourcePoolConfigurationService.EnabledDefault
- Msvm_ResourcePoolConfigurationService.TimeOfLastStateChange
- Msvm_ResourcePoolConfigurationService.AvailableRequestedStates
- Msvm_ResourcePoolConfigurationService.TransitioningToState
- Msvm_ResourcePoolConfigurationService.SystemCreationClassName
- Msvm_ResourcePoolConfigurationService.SystemName
- Msvm_ResourcePoolConfigurationService.CreationClassName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerContact
- Msvm_ResourcePoolConfigurationService.StartMode
- Msvm_ResourcePoolConfigurationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3160e8ac9ba011db70a5d7118e4d1f72733ff23f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868490"
---
# <a name="msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="06a23-103">MSVM \_ ResourcePoolConfigurationService, classe</span><span class="sxs-lookup"><span data-stu-id="06a23-103">Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="06a23-104">Fournit la gestion active des pools de ressources.</span><span class="sxs-lookup"><span data-stu-id="06a23-104">Provides for active management of resource pools.</span></span>

<span data-ttu-id="06a23-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="06a23-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a23-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06a23-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationService : CIM_Service
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
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="06a23-107">Membres</span><span class="sxs-lookup"><span data-stu-id="06a23-107">Members</span></span>

<span data-ttu-id="06a23-108">La classe **MSVM \_ ResourcePoolConfigurationService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="06a23-108">The **Msvm\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="06a23-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="06a23-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="06a23-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06a23-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06a23-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="06a23-111">Methods</span></span>

<span data-ttu-id="06a23-112">La classe **MSVM \_ ResourcePoolConfigurationService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="06a23-112">The **Msvm\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="06a23-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="06a23-113">Method</span></span>                                                                                   | <span data-ttu-id="06a23-114">Description</span><span class="sxs-lookup"><span data-stu-id="06a23-114">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06a23-115">**CreatePool**</span><span class="sxs-lookup"><span data-stu-id="06a23-115">**CreatePool**</span></span>](createpool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="06a23-116">Crée un pool de ressources enfant.</span><span class="sxs-lookup"><span data-stu-id="06a23-116">Creates a child resource pool.</span></span><br/>                                                    |
| [<span data-ttu-id="06a23-117">**DeletePool**</span><span class="sxs-lookup"><span data-stu-id="06a23-117">**DeletePool**</span></span>](deletepool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="06a23-118">Supprime un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="06a23-118">Deletes a resource pool.</span></span><br/>                                                          |
| [<span data-ttu-id="06a23-119">**ModifyPoolResources**</span><span class="sxs-lookup"><span data-stu-id="06a23-119">**ModifyPoolResources**</span></span>](modifypoolresources-msvm-resourcepoolconfigurationservice.md) | <span data-ttu-id="06a23-120">Modifie les paramètres de ressource du pool parent pour les ressources affectées à un pool enfant.</span><span class="sxs-lookup"><span data-stu-id="06a23-120">Changes the parent pool resource settings for resources assigned to a child pool.</span></span><br/> |
| [<span data-ttu-id="06a23-121">**ModifyPoolSettings**</span><span class="sxs-lookup"><span data-stu-id="06a23-121">**ModifyPoolSettings**</span></span>](modifypoolsettings-msvm-resourcepoolconfigurationservice.md)   | <span data-ttu-id="06a23-122">Modifie les paramètres d’un pool enfant qui ne sont pas liés à l’allocation.</span><span class="sxs-lookup"><span data-stu-id="06a23-122">Changes the settings of a child pool that are not allocation related.</span></span><br/>             |
| <span data-ttu-id="06a23-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="06a23-123">**RequestStateChange**</span></span>                                                                   | <span data-ttu-id="06a23-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="06a23-124">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="06a23-125">**StartService**</span><span class="sxs-lookup"><span data-stu-id="06a23-125">**StartService**</span></span>                                                                         | <span data-ttu-id="06a23-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="06a23-126">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="06a23-127">**StopService**</span><span class="sxs-lookup"><span data-stu-id="06a23-127">**StopService**</span></span>                                                                          | <span data-ttu-id="06a23-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="06a23-128">This method is not supported.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="06a23-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="06a23-129">Properties</span></span>

<span data-ttu-id="06a23-130">La classe **MSVM \_ ResourcePoolConfigurationService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="06a23-130">The **Msvm\_ResourcePoolConfigurationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06a23-131">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="06a23-131">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-132">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06a23-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-134">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="06a23-134">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="06a23-135">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="06a23-135">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06a23-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="06a23-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-139">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="06a23-139">A short description of the object.</span></span> <span data-ttu-id="06a23-140">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-141">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="06a23-141">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-144">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="06a23-144">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="06a23-145">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="06a23-145">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06a23-146">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-146">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06a23-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="06a23-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="06a23-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="06a23-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="06a23-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="06a23-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="06a23-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="06a23-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06a23-154">)</span><span class="sxs-lookup"><span data-stu-id="06a23-154">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06a23-155">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06a23-155">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-158">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="06a23-158">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="06a23-159">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="06a23-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="06a23-160">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="06a23-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-161">**Description**</span><span class="sxs-lookup"><span data-stu-id="06a23-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-164">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="06a23-164">A description of the object.</span></span> <span data-ttu-id="06a23-165">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="06a23-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-169">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="06a23-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="06a23-170">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="06a23-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06a23-171">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06a23-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="06a23-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="06a23-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="06a23-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="06a23-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="06a23-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="06a23-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="06a23-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="06a23-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06a23-180">)</span><span class="sxs-lookup"><span data-stu-id="06a23-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06a23-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="06a23-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-184">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="06a23-184">A display name for the object.</span></span> <span data-ttu-id="06a23-185">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="06a23-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-189">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="06a23-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="06a23-190">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="06a23-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="06a23-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a23-191">Value</span></span>                                                                        | <span data-ttu-id="06a23-192">Signification</span><span class="sxs-lookup"><span data-stu-id="06a23-192">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="06a23-193"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="06a23-193"><dt>2</dt></span></span> </dl> | <span data-ttu-id="06a23-194">activé</span><span class="sxs-lookup"><span data-stu-id="06a23-194">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06a23-195">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="06a23-195">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-198">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="06a23-198">The enabled and disabled states of an element.</span></span> <span data-ttu-id="06a23-199">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="06a23-199">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="06a23-200">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="06a23-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="06a23-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a23-201">Value</span></span>                                                                        | <span data-ttu-id="06a23-202">Signification</span><span class="sxs-lookup"><span data-stu-id="06a23-202">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="06a23-203"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="06a23-203"><dt>2</dt></span></span> </dl> | <span data-ttu-id="06a23-204">activé</span><span class="sxs-lookup"><span data-stu-id="06a23-204">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06a23-205">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="06a23-205">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-206">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-208">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="06a23-208">The current health of the element.</span></span> <span data-ttu-id="06a23-209">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="06a23-209">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="06a23-210">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="06a23-210">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="06a23-211">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06a23-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-213">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06a23-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-215">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="06a23-215">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="06a23-216">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-217">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="06a23-217">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-220">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="06a23-220">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="06a23-221">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="06a23-221">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="06a23-222">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-223">**Nom**</span><span class="sxs-lookup"><span data-stu-id="06a23-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-226">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="06a23-226">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="06a23-227">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="06a23-227">The label by which the object is known.</span></span> <span data-ttu-id="06a23-228">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="06a23-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-230">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-232">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="06a23-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="06a23-233">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="06a23-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06a23-234">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06a23-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="06a23-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="06a23-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="06a23-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="06a23-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="06a23-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="06a23-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="06a23-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="06a23-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="06a23-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="06a23-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="06a23-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="06a23-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="06a23-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="06a23-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="06a23-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="06a23-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="06a23-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="06a23-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="06a23-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06a23-254">)</span><span class="sxs-lookup"><span data-stu-id="06a23-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06a23-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="06a23-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-256">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06a23-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-258">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="06a23-258">The current statuses of the object.</span></span> <span data-ttu-id="06a23-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="06a23-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-263">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="06a23-263">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="06a23-264">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="06a23-264">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="06a23-265">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="06a23-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06a23-266">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="06a23-266">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-269">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="06a23-269">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="06a23-270">Toutes les informations relatives à la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="06a23-270">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="06a23-271">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="06a23-271">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06a23-272">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="06a23-272">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-275">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="06a23-275">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="06a23-276">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="06a23-276">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="06a23-277">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="06a23-277">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="06a23-278">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="06a23-278">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06a23-279">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="06a23-279">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-280">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-282">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="06a23-282">Provides high level status information.</span></span> <span data-ttu-id="06a23-283">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="06a23-283">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="06a23-284">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="06a23-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06a23-285">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06a23-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="06a23-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="06a23-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="06a23-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="06a23-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="06a23-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06a23-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="06a23-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06a23-292">)</span><span class="sxs-lookup"><span data-stu-id="06a23-292">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06a23-293">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="06a23-293">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-294">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-296">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="06a23-296">The last requested or desired state for the element.</span></span> <span data-ttu-id="06a23-297">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="06a23-297">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="06a23-298">Cette propriété est fournie pour comparer les derniers États demandés et actuels d’un élément.</span><span class="sxs-lookup"><span data-stu-id="06a23-298">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="06a23-299">Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la propriété **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="06a23-299">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="06a23-300">Si cela se produit, la valeur 12 (« non applicable ») est utilisée.</span><span class="sxs-lookup"><span data-stu-id="06a23-300">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="06a23-301">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="06a23-301">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="06a23-302">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a23-302">Value</span></span>                                                                         | <span data-ttu-id="06a23-303">Signification</span><span class="sxs-lookup"><span data-stu-id="06a23-303">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="06a23-304"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="06a23-304"><dt>12</dt></span></span> </dl> | <span data-ttu-id="06a23-305">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="06a23-305">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06a23-306">**Cours**</span><span class="sxs-lookup"><span data-stu-id="06a23-306">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-307">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="06a23-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-309">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="06a23-309">Indicates whether the service is currently running.</span></span> <span data-ttu-id="06a23-310">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="06a23-310">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-311">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="06a23-311">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-314">Qualificateurs : **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="06a23-314">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="06a23-315">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="06a23-315">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="06a23-316">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="06a23-316">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06a23-317">**État**</span><span class="sxs-lookup"><span data-stu-id="06a23-317">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-320">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="06a23-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06a23-321">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06a23-321">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-322">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="06a23-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06a23-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-324">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="06a23-324">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="06a23-325">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="06a23-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-326">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06a23-326">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-327">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-329">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="06a23-329">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="06a23-330">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="06a23-330">The scoping system's creation class name.</span></span> <span data-ttu-id="06a23-331">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="06a23-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-332">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="06a23-332">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="06a23-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06a23-335">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="06a23-335">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="06a23-336">Nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="06a23-336">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="06a23-337">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="06a23-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-338">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="06a23-338">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-339">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="06a23-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-341">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="06a23-341">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="06a23-342">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06a23-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06a23-343">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="06a23-343">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a23-344">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06a23-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06a23-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="06a23-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a23-346">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="06a23-346">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="06a23-347">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="06a23-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06a23-348">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06a23-348">Requirements</span></span>



| <span data-ttu-id="06a23-349">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06a23-349">Requirement</span></span> | <span data-ttu-id="06a23-350">Valeur</span><span class="sxs-lookup"><span data-stu-id="06a23-350">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a23-351">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06a23-351">Minimum supported client</span></span><br/> | <span data-ttu-id="06a23-352">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06a23-352">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="06a23-353">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06a23-353">Minimum supported server</span></span><br/> | <span data-ttu-id="06a23-354">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06a23-354">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="06a23-355">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="06a23-355">Namespace</span></span><br/>                | <span data-ttu-id="06a23-356">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="06a23-356">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06a23-357">MOF</span><span class="sxs-lookup"><span data-stu-id="06a23-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06a23-358"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06a23-358"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06a23-359">DLL</span><span class="sxs-lookup"><span data-stu-id="06a23-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06a23-360"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06a23-360"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

