---
description: Sert d’espace réservé pour le service à l’intérieur du commutateur qui apprend les adresses MAC et sert de pont entre les \_ classes MSVM VirtualEthernetSwitch et MSVM \_ DynamicForwardingEntry.
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Classe Msvm_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951433"
---
# <a name="msvm_transparentbridgingservice-class"></a><span data-ttu-id="8a70d-103">MSVM \_ TransparentBridgingService, classe</span><span class="sxs-lookup"><span data-stu-id="8a70d-103">Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="8a70d-104">Sert d’espace réservé pour le service à l’intérieur du commutateur qui apprend les adresses MAC et sert de pont entre les classes [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) et [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) .</span><span class="sxs-lookup"><span data-stu-id="8a70d-104">Serves as a placeholder for the service inside the switch that learns MAC addresses and serves as a bridge between the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) and [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) classes.</span></span>

<span data-ttu-id="8a70d-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8a70d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a70d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a70d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a><span data-ttu-id="8a70d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8a70d-107">Members</span></span>

<span data-ttu-id="8a70d-108">La classe **MSVM \_ TransparentBridgingService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8a70d-108">The **Msvm\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="8a70d-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8a70d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="8a70d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8a70d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8a70d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8a70d-111">Methods</span></span>

<span data-ttu-id="8a70d-112">La classe **MSVM \_ TransparentBridgingService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8a70d-112">The **Msvm\_TransparentBridgingService** class has these methods.</span></span>



| <span data-ttu-id="8a70d-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="8a70d-113">Method</span></span>                                                                           | <span data-ttu-id="8a70d-114">Description</span><span class="sxs-lookup"><span data-stu-id="8a70d-114">Description</span></span>                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="8a70d-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8a70d-115">**RequestStateChange**</span></span>](msvm-transparentbridgingservice-requeststatechange.md) | <span data-ttu-id="8a70d-116">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="8a70d-116">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="8a70d-117">**StartService**</span><span class="sxs-lookup"><span data-stu-id="8a70d-117">**StartService**</span></span>](msvm-transparentbridgingservice-startservice.md)             | <span data-ttu-id="8a70d-118">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="8a70d-118">Starts the service.</span></span><br/>      |
| [<span data-ttu-id="8a70d-119">**StopService**</span><span class="sxs-lookup"><span data-stu-id="8a70d-119">**StopService**</span></span>](msvm-transparentbridgingservice-stopservice.md)               | <span data-ttu-id="8a70d-120">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="8a70d-120">Stops the service.</span></span><br/>       |



 

### <a name="properties"></a><span data-ttu-id="8a70d-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8a70d-121">Properties</span></span>

<span data-ttu-id="8a70d-122">La classe **MSVM \_ TransparentBridgingService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a70d-122">The **Msvm\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a70d-123">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="8a70d-123">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a70d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-126">Délai d’attente, en secondes, pour le vieillissement des adresses MAC apprises de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="8a70d-126">The time-out period, in seconds, for aging out dynamically learned MAC addresses.</span></span> <span data-ttu-id="8a70d-127">Cette propriété est héritée de la [**\_ TransparentBridgingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="8a70d-127">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-128">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8a70d-128">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-129">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-131">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8a70d-131">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8a70d-132">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8a70d-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-136">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8a70d-136">A short description of the object.</span></span> <span data-ttu-id="8a70d-137">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours « service de pontage transparent du commutateur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="8a70d-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always "Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-138">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8a70d-138">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-141">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="8a70d-141">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8a70d-142">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-142">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a70d-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-143">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8a70d-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8a70d-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8a70d-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="8a70d-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="8a70d-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="8a70d-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8a70d-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8a70d-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8a70d-151">)</span><span class="sxs-lookup"><span data-stu-id="8a70d-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a70d-152">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a70d-152">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-155">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8a70d-155">A short description of the object.</span></span> <span data-ttu-id="8a70d-156">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-156">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a70d-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-160">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="8a70d-160">A description of the object.</span></span> <span data-ttu-id="8a70d-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de pontage transparent du commutateur virtuel Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="8a70d-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-162">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8a70d-162">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-165">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8a70d-165">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8a70d-166">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a70d-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8a70d-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="8a70d-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="8a70d-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="8a70d-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="8a70d-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="8a70d-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="8a70d-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8a70d-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8a70d-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8a70d-176">)</span><span class="sxs-lookup"><span data-stu-id="8a70d-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a70d-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8a70d-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-180">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8a70d-180">A display name for the object.</span></span> <span data-ttu-id="8a70d-181">Cette propriété permet à chaque instance de définir un nom complet en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="8a70d-181">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="8a70d-182">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-183">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8a70d-183">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-184">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-186">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8a70d-186">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="8a70d-187">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-188">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8a70d-188">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-189">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-191">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8a70d-191">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8a70d-192">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-193">**IDENTIFICATEUR manquant**</span><span class="sxs-lookup"><span data-stu-id="8a70d-193">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-194">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a70d-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-196">Identificateur de la base de données de filtrage utilisé par les commutateurs qui prennent en charge le VLAN et qui ont plusieurs bases de données de filtrage.</span><span class="sxs-lookup"><span data-stu-id="8a70d-196">The filtering database identifier used by switches that support VLAN and that have more than one filtering database.</span></span> <span data-ttu-id="8a70d-197">Cette propriété est héritée de la [**\_ TransparentBridgingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="8a70d-197">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8a70d-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-199">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-201">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8a70d-201">The current health of the element.</span></span> <span data-ttu-id="8a70d-202">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="8a70d-202">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8a70d-203">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8a70d-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-205">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8a70d-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-207">Spécifie l’heure à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="8a70d-207">Specifies the time when the object was installed.</span></span> <span data-ttu-id="8a70d-208">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="8a70d-208">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="8a70d-209">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8a70d-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-213">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="8a70d-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-214">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="8a70d-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8a70d-215">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-216">**Mots clés**</span><span class="sxs-lookup"><span data-stu-id="8a70d-216">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-217">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8a70d-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-219">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="8a70d-219">Do not use.</span></span> <span data-ttu-id="8a70d-220">Tableau de chaînes de forme libre qui contiennent des mots descriptifs et des expressions qui peuvent être utilisés dans les requêtes.</span><span class="sxs-lookup"><span data-stu-id="8a70d-220">A free-form array of strings that provide descriptive words and phrases that can be used in queries.</span></span> <span data-ttu-id="8a70d-221">Cette propriété n’est pas implémentée, car elle n’est pas standardisée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-221">This property is not implemented because it is not standardized.</span></span> <span data-ttu-id="8a70d-222">Si cette propriété était une construction de requête nécessaire, elle est requise plus haut dans la hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="8a70d-222">If this property were a necessary query construct, then it would be required higher in the inheritance hierarchy.</span></span> <span data-ttu-id="8a70d-223">Cette propriété est héritée de [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-223">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-224">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8a70d-224">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-227">Nom qui identifie de façon unique le service et fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-227">A name that uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="8a70d-228">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-228">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8a70d-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-230">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-232">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8a70d-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8a70d-233">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a70d-234">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8a70d-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8a70d-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8a70d-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="8a70d-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="8a70d-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="8a70d-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="8a70d-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="8a70d-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="8a70d-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="8a70d-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="8a70d-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="8a70d-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="8a70d-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="8a70d-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="8a70d-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="8a70d-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="8a70d-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="8a70d-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8a70d-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8a70d-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8a70d-254">)</span><span class="sxs-lookup"><span data-stu-id="8a70d-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a70d-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8a70d-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-256">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-258">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8a70d-258">The current status of the element.</span></span> <span data-ttu-id="8a70d-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8a70d-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-263">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="8a70d-263">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8a70d-264">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-264">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-265">**OtherProtocolType**</span><span class="sxs-lookup"><span data-stu-id="8a70d-265">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-266">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-268">Type de protocole qui est transféré lorsque la valeur de **ProtocolType** est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="8a70d-268">The type of protocol that is being forwarded when the value of **ProtocolType** is 1 (Other).</span></span> <span data-ttu-id="8a70d-269">Cette propriété est héritée de la [**\_ ForwardingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="8a70d-269">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-270">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="8a70d-270">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-273">Chaîne qui fournit des informations sur la façon dont le propriétaire principal du service peut être atteint.</span><span class="sxs-lookup"><span data-stu-id="8a70d-273">A string that provides information about how the primary owner of the Service can be reached.</span></span> <span data-ttu-id="8a70d-274">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-274">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-275">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="8a70d-275">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-278">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="8a70d-278">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="8a70d-279">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-280">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8a70d-280">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-281">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-283">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="8a70d-283">Provides high level status information.</span></span> <span data-ttu-id="8a70d-284">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="8a70d-284">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8a70d-285">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8a70d-286">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8a70d-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8a70d-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="8a70d-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="8a70d-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="8a70d-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8a70d-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8a70d-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8a70d-293">)</span><span class="sxs-lookup"><span data-stu-id="8a70d-293">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a70d-294">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="8a70d-294">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-295">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-295">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-297">Type de protocole transféré.</span><span class="sxs-lookup"><span data-stu-id="8a70d-297">The type of protocol that is being forwarded.</span></span> <span data-ttu-id="8a70d-298">Cette propriété est héritée de la [**\_ ForwardingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="8a70d-298">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-299">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8a70d-299">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-300">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-302">Dernier État demandé ou souhaité pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="8a70d-302">The last requested or desired state for the management service.</span></span> <span data-ttu-id="8a70d-303">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-304">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="8a70d-304">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-307">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="8a70d-307">Do not use.</span></span> <span data-ttu-id="8a70d-308">URL qui fournit le protocole, l’emplacement réseau et d’autres informations spécifiques au service requises pour accéder au service.</span><span class="sxs-lookup"><span data-stu-id="8a70d-308">A URL that provides the protocol, network location, and other service-specific information required to access the service.</span></span> <span data-ttu-id="8a70d-309">Utilisez plutôt la classe **ServiceAccessURI** , qui positionne correctement la sémantique de l’accès au service et clarifie le format des informations.</span><span class="sxs-lookup"><span data-stu-id="8a70d-309">Instead, use the **ServiceAccessURI** class, which correctly positions the semantics of the service access, and clarifies the format of the information.</span></span> <span data-ttu-id="8a70d-310">Cette propriété est héritée de [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-310">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-311">**Cours**</span><span class="sxs-lookup"><span data-stu-id="8a70d-311">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-312">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8a70d-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-314">Indique si le service a été démarré (**true**) ou arrêté (**false**).</span><span class="sxs-lookup"><span data-stu-id="8a70d-314">Indicates whether the service has been started (**True**), or stopped (**False**).</span></span> <span data-ttu-id="8a70d-315">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-316">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="8a70d-316">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-319">Indique si le service est démarré automatiquement par un système, un système d’exploitation, etc. ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="8a70d-319">Indicates whether the service is automatically started by a system, an operating system, and so on, or is started only upon request.</span></span> <span data-ttu-id="8a70d-320">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-321">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="8a70d-321">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-322">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8a70d-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-324">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="8a70d-324">Do not use.</span></span> <span data-ttu-id="8a70d-325">Tableau de chaînes de forme libre qui spécifient les conditions préalables spécifiques qui doivent être remplies pour que ce service démarre correctement.</span><span class="sxs-lookup"><span data-stu-id="8a70d-325">A free-form array of strings that specify any specific preconditions that must be met for this service to start correctly.</span></span> <span data-ttu-id="8a70d-326">Cette propriété n’est pas utile, car elle n’est pas standardisée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-326">This property is not useful because it is not standardized.</span></span> <span data-ttu-id="8a70d-327">Si cette propriété était une construction nécessaire, elle est requise plus haut dans la hiérarchie d’héritage (on service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-327">If this property were a necessary construct, then it would be required higher in the inheritance hierarchy (on Service).</span></span> <span data-ttu-id="8a70d-328">Cette propriété est héritée de [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-328">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-329">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="8a70d-329">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-330">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8a70d-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-332">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="8a70d-332">Do not use.</span></span> <span data-ttu-id="8a70d-333">Tableau de chaînes de forme libre qui spécifient tous les paramètres spécifiques qui doivent être fournis à la méthode **StartService** pour que ce service démarre correctement.</span><span class="sxs-lookup"><span data-stu-id="8a70d-333">A free-form array of strings that specify any specific parameters that must be supplied to the **StartService** method for this service to start correctly.</span></span> <span data-ttu-id="8a70d-334">Si cette méthode a été affinée, ses paramètres transmettent plus officiellement ces informations.</span><span class="sxs-lookup"><span data-stu-id="8a70d-334">If this method were refined, then its parameters would more formally convey this information.</span></span> <span data-ttu-id="8a70d-335">Cette propriété est héritée de [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-335">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-336">**État**</span><span class="sxs-lookup"><span data-stu-id="8a70d-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-339">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8a70d-339">The current status of the object.</span></span> <span data-ttu-id="8a70d-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8a70d-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-342">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8a70d-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-344">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8a70d-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8a70d-345">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8a70d-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a70d-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-349">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8a70d-349">The creation class name of the scoping system.</span></span> <span data-ttu-id="8a70d-350">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8a70d-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8a70d-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-354">Nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="8a70d-354">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="8a70d-355">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="8a70d-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8a70d-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-357">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8a70d-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-359">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8a70d-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8a70d-360">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8a70d-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8a70d-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8a70d-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a70d-362">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8a70d-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a70d-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8a70d-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a70d-364">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="8a70d-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8a70d-365">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a70d-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a70d-366">Notes</span><span class="sxs-lookup"><span data-stu-id="8a70d-366">Remarks</span></span>

<span data-ttu-id="8a70d-367">L’accès à la classe **MSVM \_ TransparentBridgingService** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="8a70d-367">Access to the **Msvm\_TransparentBridgingService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8a70d-368">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8a70d-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a70d-369">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a70d-369">Requirements</span></span>



| <span data-ttu-id="8a70d-370">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a70d-370">Requirement</span></span> | <span data-ttu-id="8a70d-371">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a70d-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a70d-372">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a70d-372">Minimum supported client</span></span><br/> | <span data-ttu-id="8a70d-373">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a70d-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a70d-374">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a70d-374">Minimum supported server</span></span><br/> | <span data-ttu-id="8a70d-375">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a70d-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a70d-376">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8a70d-376">Namespace</span></span><br/>                | <span data-ttu-id="8a70d-377">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a70d-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a70d-378">MOF</span><span class="sxs-lookup"><span data-stu-id="8a70d-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a70d-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a70d-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a70d-380">DLL</span><span class="sxs-lookup"><span data-stu-id="8a70d-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a70d-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a70d-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a70d-382">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a70d-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a70d-383">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8a70d-383">**CIM\_TransparentBridgingService**</span></span>](cim-transparentbridgingservice.md)
</dt> <dt>

[<span data-ttu-id="8a70d-384">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8a70d-384">**CIM\_TransparentBridgingService**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

