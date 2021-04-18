---
description: Gère toutes les connexions de terminal distant à un hôte particulier.
ms.assetid: 7eacb8a6-cb8d-4a2a-951e-f5286cf484e7
title: Classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService
- Msvm_TerminalService.InstanceID
- Msvm_TerminalService.Caption
- Msvm_TerminalService.Description
- Msvm_TerminalService.ElementName
- Msvm_TerminalService.InstallDate
- Msvm_TerminalService.OperationalStatus
- Msvm_TerminalService.StatusDescriptions
- Msvm_TerminalService.Status
- Msvm_TerminalService.HealthState
- Msvm_TerminalService.CommunicationStatus
- Msvm_TerminalService.DetailedStatus
- Msvm_TerminalService.OperatingStatus
- Msvm_TerminalService.PrimaryStatus
- Msvm_TerminalService.EnabledState
- Msvm_TerminalService.OtherEnabledState
- Msvm_TerminalService.RequestedState
- Msvm_TerminalService.EnabledDefault
- Msvm_TerminalService.TimeOfLastStateChange
- Msvm_TerminalService.AvailableRequestedStates
- Msvm_TerminalService.TransitioningToState
- Msvm_TerminalService.SystemCreationClassName
- Msvm_TerminalService.SystemName
- Msvm_TerminalService.Name
- Msvm_TerminalService.CreationClassName
- Msvm_TerminalService.PrimaryOwnerName
- Msvm_TerminalService.PrimaryOwnerContact
- Msvm_TerminalService.StartMode
- Msvm_TerminalService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76b12bb49391909638d20df817a3693938c3222c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533775"
---
# <a name="msvm_terminalservice-class"></a><span data-ttu-id="cd861-103">MSVM \_ TerminalService, classe</span><span class="sxs-lookup"><span data-stu-id="cd861-103">Msvm\_TerminalService class</span></span>

<span data-ttu-id="cd861-104">Gère toutes les connexions de terminal distant à un hôte particulier.</span><span class="sxs-lookup"><span data-stu-id="cd861-104">Manages all remote terminal connections to a particular host.</span></span> <span data-ttu-id="cd861-105">Le service utilise un port configurable pour initier toutes les connexions Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="cd861-105">The service uses a configurable port to initiate all terminal connections.</span></span>

<span data-ttu-id="cd861-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cd861-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd861-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd861-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Terminal Service";
  string   Description = "Microsoft Virtual Terminal Service";
  string   ElementName = "Hyper-V Terminal Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The virtual terminal connection management service is fully operational" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "termsvc";
  string   CreationClassName = "Msvm_TerminalService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="cd861-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cd861-108">Members</span></span>

<span data-ttu-id="cd861-109">La classe **MSVM \_ TerminalService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cd861-109">The **Msvm\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="cd861-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cd861-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd861-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd861-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd861-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cd861-112">Methods</span></span>

<span data-ttu-id="cd861-113">La classe **MSVM \_ TerminalService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cd861-113">The **Msvm\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="cd861-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="cd861-114">Method</span></span>                                                                                        | <span data-ttu-id="cd861-115">Description</span><span class="sxs-lookup"><span data-stu-id="cd861-115">Description</span></span>                                                                                                      |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd861-116">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="cd861-116">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)             | <span data-ttu-id="cd861-117">Récupère la liste DACL actuelle qui contrôle l’accès à la session interactive d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="cd861-117">Retrieves the current DACL that controls access to the interactive session of a virtual machine.</span></span><br/>      |
| [<span data-ttu-id="cd861-118">**GrantInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="cd861-118">**GrantInteractiveSessionAccess**</span></span>](grantinteractivesessionaccess-msvm-terminalservice.md)   | <span data-ttu-id="cd861-119">Octroie l’accès à la session interactive de l’ordinateur virtuel à la liste de confiance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cd861-119">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span><br/>    |
| [<span data-ttu-id="cd861-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="cd861-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-terminalservice.md)                   | <span data-ttu-id="cd861-121">Modifie les données de paramètre pour le service.</span><span class="sxs-lookup"><span data-stu-id="cd861-121">Modifies the setting data for the service.</span></span><br/>                                                            |
| [<span data-ttu-id="cd861-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="cd861-122">**RequestStateChange**</span></span>](msvm-terminalservice-requeststatechange.md)                         | <span data-ttu-id="cd861-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="cd861-123">Requests a state change.</span></span><br/>                                                                              |
| [<span data-ttu-id="cd861-124">**RevokeInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="cd861-124">**RevokeInteractiveSessionAccess**</span></span>](revokeinteractivesessionaccess-msvm-terminalservice.md) | <span data-ttu-id="cd861-125">Révoque l’accès à la session interactive de l’ordinateur virtuel à partir de la liste de confiance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cd861-125">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span><br/> |
| [<span data-ttu-id="cd861-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="cd861-126">**StartService**</span></span>](msvm-terminalservice-startservice.md)                                     | <span data-ttu-id="cd861-127">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="cd861-127">Starts the service.</span></span><br/>                                                                                   |
| [<span data-ttu-id="cd861-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="cd861-128">**StopService**</span></span>](msvm-terminalservice-stopservice.md)                                       | <span data-ttu-id="cd861-129">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="cd861-129">Stops the service.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="cd861-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd861-130">Properties</span></span>

<span data-ttu-id="cd861-131">La classe **MSVM \_ TerminalService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cd861-131">The **Msvm\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd861-132">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="cd861-132">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-133">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-133">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd861-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-135">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="cd861-135">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="cd861-136">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd861-136">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-137">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cd861-137">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-140">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cd861-140">A short description of the object.</span></span> <span data-ttu-id="cd861-141">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-142">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="cd861-142">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-145">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="cd861-145">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="cd861-146">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="cd861-146">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd861-147">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd861-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="cd861-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="cd861-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="cd861-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="cd861-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="cd861-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="cd861-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd861-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd861-155">)</span><span class="sxs-lookup"><span data-stu-id="cd861-155">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd861-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd861-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-159">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="cd861-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cd861-160">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-161">**Description**</span><span class="sxs-lookup"><span data-stu-id="cd861-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-164">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="cd861-164">A description of the object.</span></span> <span data-ttu-id="cd861-165">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="cd861-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-169">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cd861-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="cd861-170">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="cd861-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd861-171">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd861-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="cd861-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="cd861-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="cd861-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="cd861-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="cd861-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="cd861-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="cd861-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd861-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd861-180">)</span><span class="sxs-lookup"><span data-stu-id="cd861-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd861-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd861-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-184">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cd861-184">A display name for the object.</span></span> <span data-ttu-id="cd861-185">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="cd861-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-189">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="cd861-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="cd861-190">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd861-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-191">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="cd861-191">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-194">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="cd861-194">The enabled and disabled states of an element.</span></span> <span data-ttu-id="cd861-195">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="cd861-195">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="cd861-196">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd861-196">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-197">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="cd861-197">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-200">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="cd861-200">The current health of the element.</span></span> <span data-ttu-id="cd861-201">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="cd861-201">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="cd861-202">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="cd861-202">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="cd861-203">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd861-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-205">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd861-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-207">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="cd861-207">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="cd861-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-209">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd861-209">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd861-212">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="cd861-212">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cd861-213">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="cd861-213">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cd861-214">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="cd861-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd861-215">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cd861-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-218">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="cd861-218">The label by which the object is known.</span></span> <span data-ttu-id="cd861-219">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-219">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-220">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="cd861-220">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-221">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-223">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="cd861-223">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="cd861-224">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="cd861-224">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd861-225">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd861-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="cd861-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="cd861-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="cd861-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="cd861-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="cd861-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="cd861-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="cd861-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="cd861-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="cd861-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="cd861-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="cd861-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="cd861-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="cd861-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="cd861-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="cd861-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="cd861-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="cd861-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="cd861-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd861-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd861-245">)</span><span class="sxs-lookup"><span data-stu-id="cd861-245">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd861-246">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="cd861-246">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-247">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd861-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-249">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cd861-249">The current statuses of the object.</span></span> <span data-ttu-id="cd861-250">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-250">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-251">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="cd861-251">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-254">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="cd861-254">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="cd861-255">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="cd861-255">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="cd861-256">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd861-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-257">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="cd861-257">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-260">Valeur qui fournit des informations sur la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="cd861-260">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="cd861-261">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-261">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-262">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="cd861-262">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-265">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="cd861-265">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="cd861-266">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="cd861-266">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="cd861-267">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-267">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-268">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="cd861-268">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-269">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-271">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="cd861-271">Provides high level status information.</span></span> <span data-ttu-id="cd861-272">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="cd861-272">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="cd861-273">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="cd861-273">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd861-274">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-274">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd861-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="cd861-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="cd861-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="cd861-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="cd861-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="cd861-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd861-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd861-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd861-281">)</span><span class="sxs-lookup"><span data-stu-id="cd861-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd861-282">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="cd861-282">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-285">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="cd861-285">The last requested or desired state for the element.</span></span> <span data-ttu-id="cd861-286">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="cd861-286">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="cd861-287">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="cd861-287">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="cd861-288">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="cd861-288">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="cd861-289">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd861-289">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="cd861-290">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="cd861-290">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="cd861-291">**Cours**</span><span class="sxs-lookup"><span data-stu-id="cd861-291">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-292">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="cd861-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-294">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cd861-294">Indicates whether the service is currently running.</span></span> <span data-ttu-id="cd861-295">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-295">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-296">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="cd861-296">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-299">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="cd861-299">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="cd861-300">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-301">**État**</span><span class="sxs-lookup"><span data-stu-id="cd861-301">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-304">État de l’élément.</span><span class="sxs-lookup"><span data-stu-id="cd861-304">The status of the element.</span></span> <span data-ttu-id="cd861-305">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-306">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cd861-306">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-307">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="cd861-307">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd861-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-309">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="cd861-309">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="cd861-310">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd861-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-311">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd861-311">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-314">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="cd861-314">The scoping system's creation class name.</span></span> <span data-ttu-id="cd861-315">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-316">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cd861-316">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cd861-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-319">Nom du système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="cd861-319">The name of the hosting computer system.</span></span> <span data-ttu-id="cd861-320">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="cd861-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-321">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="cd861-321">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-322">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd861-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-324">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="cd861-324">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="cd861-325">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd861-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd861-326">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="cd861-326">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd861-327">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd861-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd861-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd861-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd861-329">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="cd861-329">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="cd861-330">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd861-330">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd861-331">Notes</span><span class="sxs-lookup"><span data-stu-id="cd861-331">Remarks</span></span>

<span data-ttu-id="cd861-332">L’accès à la classe **MSVM \_ TerminalService** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="cd861-332">Access to the **Msvm\_TerminalService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cd861-333">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cd861-333">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd861-334">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd861-334">Requirements</span></span>



| <span data-ttu-id="cd861-335">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd861-335">Requirement</span></span> | <span data-ttu-id="cd861-336">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd861-336">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd861-337">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd861-337">Minimum supported client</span></span><br/> | <span data-ttu-id="cd861-338">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd861-338">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd861-339">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd861-339">Minimum supported server</span></span><br/> | <span data-ttu-id="cd861-340">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd861-340">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd861-341">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cd861-341">Namespace</span></span><br/>                | <span data-ttu-id="cd861-342">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd861-342">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd861-343">MOF</span><span class="sxs-lookup"><span data-stu-id="cd861-343">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd861-344"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd861-344"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd861-345">DLL</span><span class="sxs-lookup"><span data-stu-id="cd861-345">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd861-346"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd861-346"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd861-347">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd861-347">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd861-348">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="cd861-348">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

