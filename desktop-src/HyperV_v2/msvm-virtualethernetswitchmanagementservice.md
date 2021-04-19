---
description: Représente le service de virtualisation présent sur un système hôte unique. MSVM \_ VirtualEthernetSwitchManagementService est utilisé pour contrôler la définition, la modification et la suppression de commutateurs Ethernet virtuels.
ms.assetid: d29935d3-3a88-4186-97e9-b27c0c0d07d0
title: Classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService
- Msvm_VirtualEthernetSwitchManagementService.InstanceID
- Msvm_VirtualEthernetSwitchManagementService.Caption
- Msvm_VirtualEthernetSwitchManagementService.Description
- Msvm_VirtualEthernetSwitchManagementService.ElementName
- Msvm_VirtualEthernetSwitchManagementService.InstallDate
- Msvm_VirtualEthernetSwitchManagementService.Name
- Msvm_VirtualEthernetSwitchManagementService.OperationalStatus
- Msvm_VirtualEthernetSwitchManagementService.StatusDescriptions
- Msvm_VirtualEthernetSwitchManagementService.Status
- Msvm_VirtualEthernetSwitchManagementService.HealthState
- Msvm_VirtualEthernetSwitchManagementService.CommunicationStatus
- Msvm_VirtualEthernetSwitchManagementService.DetailedStatus
- Msvm_VirtualEthernetSwitchManagementService.OperatingStatus
- Msvm_VirtualEthernetSwitchManagementService.PrimaryStatus
- Msvm_VirtualEthernetSwitchManagementService.EnabledState
- Msvm_VirtualEthernetSwitchManagementService.OtherEnabledState
- Msvm_VirtualEthernetSwitchManagementService.RequestedState
- Msvm_VirtualEthernetSwitchManagementService.EnabledDefault
- Msvm_VirtualEthernetSwitchManagementService.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitchManagementService.AvailableRequestedStates
- Msvm_VirtualEthernetSwitchManagementService.TransitioningToState
- Msvm_VirtualEthernetSwitchManagementService.SystemCreationClassName
- Msvm_VirtualEthernetSwitchManagementService.SystemName
- Msvm_VirtualEthernetSwitchManagementService.CreationClassName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitchManagementService.StartMode
- Msvm_VirtualEthernetSwitchManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e6c1d4dee775dc6fabbb5fb3c96c987d1f6bda5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538228"
---
# <a name="msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="043aa-104">MSVM \_ VirtualEthernetSwitchManagementService, classe</span><span class="sxs-lookup"><span data-stu-id="043aa-104">Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="043aa-105">Représente le service de virtualisation présent sur un système hôte unique.</span><span class="sxs-lookup"><span data-stu-id="043aa-105">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="043aa-106">MSVM \_ VirtualEthernetSwitchManagementService est utilisé pour contrôler la définition, la modification et la suppression de commutateurs Ethernet virtuels.</span><span class="sxs-lookup"><span data-stu-id="043aa-106">Msvm\_VirtualEthernetSwitchManagementService is used to control the definition, modification, and deletion of virtual Ethernet switches.</span></span>

<span data-ttu-id="043aa-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="043aa-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="043aa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="043aa-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual Networking Management Service";
  string   Description = "Provides Hyper-V Networking WMI management";
  string   ElementName = "Hyper-V Networking Management Service";
  datetime InstallDate;
  string   Name = "nvspwmi";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status = { "OK" };
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitchManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="043aa-109">Membres</span><span class="sxs-lookup"><span data-stu-id="043aa-109">Members</span></span>

<span data-ttu-id="043aa-110">La classe **MSVM \_ VirtualEthernetSwitchManagementService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="043aa-110">The **Msvm\_VirtualEthernetSwitchManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="043aa-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="043aa-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="043aa-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="043aa-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="043aa-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="043aa-113">Methods</span></span>

<span data-ttu-id="043aa-114">La classe **MSVM \_ VirtualEthernetSwitchManagementService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="043aa-114">The **Msvm\_VirtualEthernetSwitchManagementService** class has these methods.</span></span>



| <span data-ttu-id="043aa-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="043aa-115">Method</span></span>                                                                                               | <span data-ttu-id="043aa-116">Description</span><span class="sxs-lookup"><span data-stu-id="043aa-116">Description</span></span>                                                                       |
|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="043aa-117">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="043aa-117">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)         | <span data-ttu-id="043aa-118">Ajoute des paramètres de fonctionnalité à la configuration d’un port commuté Ethernet.</span><span class="sxs-lookup"><span data-stu-id="043aa-118">Adds feature settings to the configuration of an Ethernet switch port.</span></span><br/> |
| [<span data-ttu-id="043aa-119">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="043aa-119">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)       | <span data-ttu-id="043aa-120">Ajoute des ressources à une configuration de commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="043aa-120">Adds resources to a virtual switch configuration.</span></span><br/>                      |
| [<span data-ttu-id="043aa-121">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="043aa-121">**DefineSystem**</span></span>](definesystem-msvm-virtualethernetswitchmanagementservice.md)                     | <span data-ttu-id="043aa-122">Crée un commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="043aa-122">Creates a new virtual switch.</span></span><br/>                                          |
| [<span data-ttu-id="043aa-123">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="043aa-123">**DestroySystem**</span></span>](destroysystem-msvm-virtualethernetswitchmanagementservice.md)                   | <span data-ttu-id="043aa-124">Détruit un commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="043aa-124">Destroys a virtual switch.</span></span><br/>                                             |
| [<span data-ttu-id="043aa-125">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="043aa-125">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="043aa-126">Modifie les paramètres de fonctionnalité d’un port commuté Ethernet.</span><span class="sxs-lookup"><span data-stu-id="043aa-126">Modifies the feature settings of an Ethernet switch port.</span></span><br/>              |
| [<span data-ttu-id="043aa-127">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="043aa-127">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="043aa-128">Modifie les paramètres de ressource pour un commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="043aa-128">Modifies resource settings for a virtual switch.</span></span><br/>                       |
| [<span data-ttu-id="043aa-129">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="043aa-129">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualethernetswitchmanagementservice.md)     | <span data-ttu-id="043aa-130">Modifie les paramètres du commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="043aa-130">Modifies virtual switch settings.</span></span><br/>                                      |
| [<span data-ttu-id="043aa-131">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="043aa-131">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="043aa-132">Supprime les paramètres de fonctionnalités d’un port commuté Ethernet.</span><span class="sxs-lookup"><span data-stu-id="043aa-132">Removes feature settings from an Ethernet switch port.</span></span><br/>                 |
| [<span data-ttu-id="043aa-133">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="043aa-133">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="043aa-134">Supprime les paramètres de ressources virtuelles d’une configuration de commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="043aa-134">Removes virtual resource settings from a virtual switch configuration.</span></span><br/> |
| [<span data-ttu-id="043aa-135">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="043aa-135">**RequestStateChange**</span></span>](msvm-virtualethernetswitchmanagementservice-requeststatechange.md)         | <span data-ttu-id="043aa-136">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="043aa-136">Requests a state change.</span></span><br/>                                               |
| [<span data-ttu-id="043aa-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="043aa-137">**StartService**</span></span>](msvm-virtualethernetswitchmanagementservice-startservice.md)                     | <span data-ttu-id="043aa-138">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="043aa-138">Starts the service.</span></span><br/>                                                    |
| [<span data-ttu-id="043aa-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="043aa-139">**StopService**</span></span>](msvm-virtualethernetswitchmanagementservice-stopservice.md)                       | <span data-ttu-id="043aa-140">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="043aa-140">Stops the service.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="043aa-141">Propriétés</span><span class="sxs-lookup"><span data-stu-id="043aa-141">Properties</span></span>

<span data-ttu-id="043aa-142">La classe **MSVM \_ VirtualEthernetSwitchManagementService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="043aa-142">The **Msvm\_VirtualEthernetSwitchManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="043aa-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="043aa-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-144">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="043aa-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-146">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="043aa-146">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="043aa-147">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="043aa-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043aa-148">**Caption**</span><span class="sxs-lookup"><span data-stu-id="043aa-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-151">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="043aa-151">A short description of the object.</span></span> <span data-ttu-id="043aa-152">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur le « service de gestion de réseau virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="043aa-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-153">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="043aa-153">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-156">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="043aa-156">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="043aa-157">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="043aa-157">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043aa-158">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043aa-158">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="043aa-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="043aa-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="043aa-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="043aa-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="043aa-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="043aa-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="043aa-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="043aa-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="043aa-166">)</span><span class="sxs-lookup"><span data-stu-id="043aa-166">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="043aa-167">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="043aa-167">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-170">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="043aa-170">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="043aa-171">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="043aa-171">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="043aa-172">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ VirtualEthernetSwitchManagementService ».</span><span class="sxs-lookup"><span data-stu-id="043aa-172">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualEthernetSwitchManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-173">**Description**</span><span class="sxs-lookup"><span data-stu-id="043aa-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-176">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="043aa-176">A description of the object.</span></span> <span data-ttu-id="043aa-177">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fournit la gestion WMI de mise en réseau Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="043aa-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Networking WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="043aa-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-181">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="043aa-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="043aa-182">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="043aa-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043aa-183">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043aa-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="043aa-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="043aa-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="043aa-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="043aa-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="043aa-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="043aa-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="043aa-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="043aa-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="043aa-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="043aa-192">)</span><span class="sxs-lookup"><span data-stu-id="043aa-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="043aa-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="043aa-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-196">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="043aa-196">A display name for the object.</span></span> <span data-ttu-id="043aa-197">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur le « service de gestion de réseau Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="043aa-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="043aa-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-199">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-201">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="043aa-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="043aa-202">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="043aa-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="043aa-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="043aa-203">Value</span></span>                                                                        | <span data-ttu-id="043aa-204">Signification</span><span class="sxs-lookup"><span data-stu-id="043aa-204">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="043aa-205"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="043aa-205"><dt>2</dt></span></span> </dl> | <span data-ttu-id="043aa-206">activé</span><span class="sxs-lookup"><span data-stu-id="043aa-206">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="043aa-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="043aa-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-210">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="043aa-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="043aa-211">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="043aa-211">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="043aa-212">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 5 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="043aa-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not applicable).</span></span>

</dd> <dt>

<span data-ttu-id="043aa-213">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="043aa-213">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-214">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-216">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="043aa-216">The current health of the element.</span></span> <span data-ttu-id="043aa-217">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="043aa-217">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="043aa-218">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="043aa-218">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="043aa-219">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="043aa-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="043aa-220">Valeur</span><span class="sxs-lookup"><span data-stu-id="043aa-220">Value</span></span>                                                                        | <span data-ttu-id="043aa-221">Signification</span><span class="sxs-lookup"><span data-stu-id="043aa-221">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="043aa-222"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="043aa-222"><dt>5</dt></span></span> </dl> | <span data-ttu-id="043aa-223">L’état d’intégrité est normal.</span><span class="sxs-lookup"><span data-stu-id="043aa-223">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="043aa-224">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="043aa-224">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-225">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="043aa-225">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-227">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="043aa-227">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="043aa-228">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043aa-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="043aa-229">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="043aa-229">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-232">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="043aa-232">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="043aa-233">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="043aa-233">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="043aa-234">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="043aa-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="043aa-235">**Nom**</span><span class="sxs-lookup"><span data-stu-id="043aa-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-238">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="043aa-238">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="043aa-239">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="043aa-239">The label by which the object is known.</span></span> <span data-ttu-id="043aa-240">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « VMMS ».</span><span class="sxs-lookup"><span data-stu-id="043aa-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-241">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="043aa-241">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-242">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-244">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="043aa-244">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="043aa-245">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="043aa-245">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043aa-246">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043aa-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="043aa-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="043aa-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="043aa-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="043aa-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="043aa-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="043aa-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="043aa-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="043aa-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="043aa-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="043aa-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="043aa-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="043aa-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="043aa-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="043aa-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="043aa-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="043aa-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="043aa-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="043aa-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="043aa-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="043aa-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="043aa-266">)</span><span class="sxs-lookup"><span data-stu-id="043aa-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="043aa-267">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="043aa-267">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-268">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-268">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="043aa-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-270">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="043aa-270">The current statuses of the object.</span></span> <span data-ttu-id="043aa-271">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="043aa-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="043aa-272">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="043aa-272">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-275">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="043aa-275">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="043aa-276">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="043aa-276">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="043aa-277">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="043aa-277">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043aa-278">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="043aa-278">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-281">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="043aa-281">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="043aa-282">Toutes les informations relatives à la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="043aa-282">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="043aa-283">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="043aa-283">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043aa-284">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="043aa-284">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-287">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="043aa-287">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="043aa-288">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="043aa-288">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="043aa-289">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="043aa-289">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="043aa-290">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="043aa-290">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043aa-291">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="043aa-291">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-292">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-292">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-294">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="043aa-294">Provides high level status information.</span></span> <span data-ttu-id="043aa-295">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="043aa-295">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="043aa-296">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="043aa-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043aa-297">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043aa-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="043aa-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="043aa-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="043aa-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="043aa-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="043aa-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="043aa-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="043aa-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="043aa-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="043aa-304">)</span><span class="sxs-lookup"><span data-stu-id="043aa-304">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="043aa-305">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="043aa-305">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-306">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-308">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="043aa-308">The last requested or desired state for the element.</span></span> <span data-ttu-id="043aa-309">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="043aa-309">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="043aa-310">Cette propriété est fournie pour comparer les derniers États demandés et actuels d’un élément.</span><span class="sxs-lookup"><span data-stu-id="043aa-310">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="043aa-311">Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la propriété **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="043aa-311">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="043aa-312">Si cela se produit, la valeur 12 (« non applicable ») est utilisée.</span><span class="sxs-lookup"><span data-stu-id="043aa-312">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="043aa-313">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="043aa-313">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="043aa-314">Valeur</span><span class="sxs-lookup"><span data-stu-id="043aa-314">Value</span></span>                                                                         | <span data-ttu-id="043aa-315">Signification</span><span class="sxs-lookup"><span data-stu-id="043aa-315">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="043aa-316"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="043aa-316"><dt>12</dt></span></span> </dl> | <span data-ttu-id="043aa-317">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="043aa-317">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="043aa-318">**Cours**</span><span class="sxs-lookup"><span data-stu-id="043aa-318">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-319">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="043aa-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-321">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="043aa-321">Indicates whether the service is currently running.</span></span> <span data-ttu-id="043aa-322">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="043aa-322">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="043aa-323">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="043aa-323">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-326">Qualificateurs : **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="043aa-326">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="043aa-327">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="043aa-327">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="043aa-328">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="043aa-328">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043aa-329">**État**</span><span class="sxs-lookup"><span data-stu-id="043aa-329">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-332">Décrit l'état actuel du service.</span><span class="sxs-lookup"><span data-stu-id="043aa-332">Describes the current status of the service.</span></span> <span data-ttu-id="043aa-333">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="043aa-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-334">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="043aa-334">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-335">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="043aa-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="043aa-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-337">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="043aa-337">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="043aa-338">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="043aa-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-339">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="043aa-339">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-342">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="043aa-342">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="043aa-343">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="043aa-343">The scoping system's creation class name.</span></span> <span data-ttu-id="043aa-344">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="043aa-344">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="043aa-345">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="043aa-345">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="043aa-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043aa-348">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="043aa-348">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="043aa-349">Nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="043aa-349">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="043aa-350">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="043aa-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="043aa-351">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="043aa-351">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-352">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="043aa-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-354">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="043aa-354">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="043aa-355">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="043aa-355">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="043aa-356">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="043aa-356">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043aa-357">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043aa-357">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043aa-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="043aa-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043aa-359">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="043aa-359">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="043aa-360">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="043aa-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="043aa-361">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="043aa-361">Requirements</span></span>



| <span data-ttu-id="043aa-362">Condition requise</span><span class="sxs-lookup"><span data-stu-id="043aa-362">Requirement</span></span> | <span data-ttu-id="043aa-363">Valeur</span><span class="sxs-lookup"><span data-stu-id="043aa-363">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="043aa-364">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="043aa-364">Minimum supported client</span></span><br/> | <span data-ttu-id="043aa-365">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="043aa-365">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="043aa-366">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="043aa-366">Minimum supported server</span></span><br/> | <span data-ttu-id="043aa-367">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="043aa-367">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="043aa-368">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="043aa-368">Namespace</span></span><br/>                | <span data-ttu-id="043aa-369">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="043aa-369">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="043aa-370">MOF</span><span class="sxs-lookup"><span data-stu-id="043aa-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="043aa-371"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="043aa-371"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="043aa-372">DLL</span><span class="sxs-lookup"><span data-stu-id="043aa-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="043aa-373"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="043aa-373"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

