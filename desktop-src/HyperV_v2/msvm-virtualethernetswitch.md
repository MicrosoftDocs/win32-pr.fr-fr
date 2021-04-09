---
description: Représente un commutateur Ethernet virtuel. Chaque commutateur possède de nombreux ports différents auxquels les cartes réseau peuvent être attachées. Le commutateur lui-même n’est pas hautement configurable et agit principalement comme un espace réservé.
ms.assetid: 9415477a-9423-40fa-a887-3a93da1374af
title: Classe Msvm_VirtualEthernetSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitch
- Msvm_VirtualEthernetSwitch.SetPowerState
- Msvm_VirtualEthernetSwitch.InstanceID
- Msvm_VirtualEthernetSwitch.Caption
- Msvm_VirtualEthernetSwitch.Description
- Msvm_VirtualEthernetSwitch.ElementName
- Msvm_VirtualEthernetSwitch.InstallDate
- Msvm_VirtualEthernetSwitch.OperationalStatus
- Msvm_VirtualEthernetSwitch.StatusDescriptions
- Msvm_VirtualEthernetSwitch.Status
- Msvm_VirtualEthernetSwitch.HealthState
- Msvm_VirtualEthernetSwitch.CommunicationStatus
- Msvm_VirtualEthernetSwitch.DetailedStatus
- Msvm_VirtualEthernetSwitch.OperatingStatus
- Msvm_VirtualEthernetSwitch.PrimaryStatus
- Msvm_VirtualEthernetSwitch.EnabledState
- Msvm_VirtualEthernetSwitch.OtherEnabledState
- Msvm_VirtualEthernetSwitch.RequestedState
- Msvm_VirtualEthernetSwitch.EnabledDefault
- Msvm_VirtualEthernetSwitch.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitch.AvailableRequestedStates
- Msvm_VirtualEthernetSwitch.TransitioningToState
- Msvm_VirtualEthernetSwitch.CreationClassName
- Msvm_VirtualEthernetSwitch.Name
- Msvm_VirtualEthernetSwitch.PrimaryOwnerName
- Msvm_VirtualEthernetSwitch.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitch.Roles
- Msvm_VirtualEthernetSwitch.NameFormat
- Msvm_VirtualEthernetSwitch.OtherIdentifyingInfo
- Msvm_VirtualEthernetSwitch.IdentifyingDescriptions
- Msvm_VirtualEthernetSwitch.Dedicated
- Msvm_VirtualEthernetSwitch.OtherDedicatedDescriptions
- Msvm_VirtualEthernetSwitch.ResetCapability
- Msvm_VirtualEthernetSwitch.PowerManagementCapabilities
- Msvm_VirtualEthernetSwitch.MaxVMQOffloads
- Msvm_VirtualEthernetSwitch.MaxIOVOffloads
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cd916e24a6e34ed6a70002c4988f55810050c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866393"
---
# <a name="msvm_virtualethernetswitch-class"></a><span data-ttu-id="76a3f-105">MSVM \_ VirtualEthernetSwitch, classe</span><span class="sxs-lookup"><span data-stu-id="76a3f-105">Msvm\_VirtualEthernetSwitch class</span></span>

<span data-ttu-id="76a3f-106">Représente un commutateur Ethernet virtuel.</span><span class="sxs-lookup"><span data-stu-id="76a3f-106">Represents a virtual Ethernet switch.</span></span> <span data-ttu-id="76a3f-107">Chaque commutateur possède de nombreux ports différents auxquels les cartes réseau peuvent être attachées.</span><span class="sxs-lookup"><span data-stu-id="76a3f-107">Each switch has many different ports to which network adapters can be attached.</span></span> <span data-ttu-id="76a3f-108">Le commutateur lui-même n’est pas hautement configurable et agit principalement comme un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="76a3f-108">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="76a3f-109">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="76a3f-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a3f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76a3f-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Virtual Switch";
  string   Description = "Microsoft Virtual Switch";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName = "Msvm_VirtualEthernetSwitch";
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 5;
  uint16   PowerManagementCapabilities[];
  uint32   MaxVMQOffloads;
  uint32   MaxIOVOffloads;
};
```

## <a name="members"></a><span data-ttu-id="76a3f-111">Membres</span><span class="sxs-lookup"><span data-stu-id="76a3f-111">Members</span></span>

<span data-ttu-id="76a3f-112">La classe **MSVM \_ VirtualEthernetSwitch** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="76a3f-112">The **Msvm\_VirtualEthernetSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="76a3f-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="76a3f-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="76a3f-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76a3f-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76a3f-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="76a3f-115">Methods</span></span>

<span data-ttu-id="76a3f-116">La classe **MSVM \_ VirtualEthernetSwitch** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="76a3f-116">The **Msvm\_VirtualEthernetSwitch** class has these methods.</span></span>



| <span data-ttu-id="76a3f-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="76a3f-117">Method</span></span>                                                                      | <span data-ttu-id="76a3f-118">Description</span><span class="sxs-lookup"><span data-stu-id="76a3f-118">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="76a3f-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="76a3f-119">**RequestStateChange**</span></span>](msvm-virtualethernetswitch-requeststatechange.md) | <span data-ttu-id="76a3f-120">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="76a3f-120">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="76a3f-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="76a3f-121">**SetPowerState**</span></span>                                                           | <span data-ttu-id="76a3f-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="76a3f-122">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="76a3f-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="76a3f-123">Properties</span></span>

<span data-ttu-id="76a3f-124">La classe **MSVM \_ VirtualEthernetSwitch** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="76a3f-124">The **Msvm\_VirtualEthernetSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76a3f-125">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="76a3f-125">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-126">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-128">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="76a3f-128">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="76a3f-129">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="76a3f-129">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="76a3f-130">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="76a3f-130">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="76a3f-131">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="76a3f-131">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="76a3f-132">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76a3f-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="76a3f-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="76a3f-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="76a3f-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="76a3f-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="76a3f-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="76a3f-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="76a3f-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="76a3f-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="76a3f-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="76a3f-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="76a3f-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="76a3f-143">)</span><span class="sxs-lookup"><span data-stu-id="76a3f-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76a3f-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="76a3f-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-147">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="76a3f-147">A short description of the object.</span></span> <span data-ttu-id="76a3f-148">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « commutateur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="76a3f-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-149">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="76a3f-149">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-152">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="76a3f-152">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="76a3f-153">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="76a3f-153">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76a3f-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="76a3f-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76a3f-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="76a3f-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="76a3f-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="76a3f-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="76a3f-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76a3f-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="76a3f-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="76a3f-162">)</span><span class="sxs-lookup"><span data-stu-id="76a3f-162">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76a3f-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="76a3f-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-166">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="76a3f-166">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="76a3f-167">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur « MSVM \_ VirtualEthernetSwitch ».</span><span class="sxs-lookup"><span data-stu-id="76a3f-167">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-168">**Dédié**</span><span class="sxs-lookup"><span data-stu-id="76a3f-168">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-169">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-171">Indique si le système informatique est un système à usage spécifique (dédié à une utilisation particulière) et s’il s’agit d’un système à usage général.</span><span class="sxs-lookup"><span data-stu-id="76a3f-171">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="76a3f-172">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur 0 (non dédié).</span><span class="sxs-lookup"><span data-stu-id="76a3f-172">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-173">**Description**</span><span class="sxs-lookup"><span data-stu-id="76a3f-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-176">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="76a3f-176">A description of the object.</span></span> <span data-ttu-id="76a3f-177">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Microsoft Virtual Switch ».</span><span class="sxs-lookup"><span data-stu-id="76a3f-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="76a3f-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-181">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="76a3f-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="76a3f-182">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="76a3f-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76a3f-183">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="76a3f-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="76a3f-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="76a3f-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="76a3f-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="76a3f-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="76a3f-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="76a3f-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76a3f-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="76a3f-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="76a3f-192">)</span><span class="sxs-lookup"><span data-stu-id="76a3f-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76a3f-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="76a3f-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-196">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="76a3f-196">A display name for the object.</span></span> <span data-ttu-id="76a3f-197">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="76a3f-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-199">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-201">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="76a3f-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="76a3f-202">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="76a3f-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="76a3f-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="76a3f-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="76a3f-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="76a3f-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76a3f-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="76a3f-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-207">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-209">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="76a3f-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="76a3f-210">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="76a3f-210">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="76a3f-211">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 5 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="76a3f-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-212">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="76a3f-212">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-213">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-215">Spécifie l’intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="76a3f-215">Specifies the current health of the element.</span></span> <span data-ttu-id="76a3f-216">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="76a3f-216">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="76a3f-217">Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="76a3f-217">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="76a3f-218">La propriété **EnabledState** peut également contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="76a3f-218">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="76a3f-219">Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).</span><span class="sxs-lookup"><span data-stu-id="76a3f-219">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="76a3f-220">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="76a3f-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="76a3f-221">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="76a3f-222">Signification</span><span class="sxs-lookup"><span data-stu-id="76a3f-222">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="76a3f-223"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="76a3f-223"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="76a3f-224">L’élément est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.</span><span class="sxs-lookup"><span data-stu-id="76a3f-224">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="76a3f-225"><dt>**Erreur majeure**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="76a3f-225"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="76a3f-226">L’élément a subi un échec majeur.</span><span class="sxs-lookup"><span data-stu-id="76a3f-226">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="76a3f-227"><dt>**Erreur critique**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="76a3f-227"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="76a3f-228">L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible.</span><span class="sxs-lookup"><span data-stu-id="76a3f-228">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="76a3f-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="76a3f-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-230">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76a3f-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-232">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-232">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-233">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="76a3f-233">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-234">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="76a3f-234">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-236">Date et heure de création de la configuration d’ordinateur virtuel pour un ordinateur virtuel, ou **valeur null**, pour un système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="76a3f-236">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="76a3f-237">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-238">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="76a3f-238">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-239">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-241">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="76a3f-241">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-242">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="76a3f-242">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="76a3f-243">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-243">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-244">**MaxIOVOffloads**</span><span class="sxs-lookup"><span data-stu-id="76a3f-244">**MaxIOVOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-245">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76a3f-245">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-247">Le nombre maximal de déchargements de fonctions virtuelles SR-IOV (root IO Virtualization) unique sur ce commutateur.</span><span class="sxs-lookup"><span data-stu-id="76a3f-247">The maximum number of single root IO virtualization (SR-IOV) virtual function offloads available on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-248">**MaxVMQOffloads**</span><span class="sxs-lookup"><span data-stu-id="76a3f-248">**MaxVMQOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-249">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="76a3f-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="76a3f-250">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-251">Nombre maximal de déchargements de file d’attente d’ordinateurs virtuels autorisés pour un port sur ce commutateur.</span><span class="sxs-lookup"><span data-stu-id="76a3f-251">The maximum number of virtual machine queue (VMQ) offloads allowed for a port on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-252">**Nom**</span><span class="sxs-lookup"><span data-stu-id="76a3f-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-255">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="76a3f-255">The label by which the object is known.</span></span> <span data-ttu-id="76a3f-256">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur «*GUID*».</span><span class="sxs-lookup"><span data-stu-id="76a3f-256">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-257">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="76a3f-257">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-260">Chaîne qui identifie la façon dont le nom système a été généré, à l’aide de la méthode heuristique de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="76a3f-260">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="76a3f-261">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-261">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-262">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="76a3f-262">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-263">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-265">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="76a3f-265">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="76a3f-266">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="76a3f-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76a3f-267">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="76a3f-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76a3f-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="76a3f-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="76a3f-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="76a3f-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="76a3f-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="76a3f-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="76a3f-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="76a3f-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="76a3f-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="76a3f-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="76a3f-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="76a3f-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="76a3f-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="76a3f-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="76a3f-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="76a3f-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="76a3f-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76a3f-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="76a3f-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="76a3f-287">)</span><span class="sxs-lookup"><span data-stu-id="76a3f-287">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76a3f-288">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="76a3f-288">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-289">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-289">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-291">Tableau qui contient les États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="76a3f-291">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="76a3f-292">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-293">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="76a3f-293">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-294">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76a3f-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-296">Chaîne qui décrit comment ou pourquoi le système est dédié lorsque le tableau **dédié** comprend la valeur 2 (autre).</span><span class="sxs-lookup"><span data-stu-id="76a3f-296">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="76a3f-297">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-298">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="76a3f-298">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-301">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="76a3f-301">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="76a3f-302">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="76a3f-302">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="76a3f-303">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-304">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="76a3f-304">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-305">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76a3f-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-307">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-307">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-308">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="76a3f-308">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-309">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-311">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="76a3f-311">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-312">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="76a3f-312">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-315">Chaîne qui indique comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="76a3f-315">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="76a3f-316">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-316">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-317">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="76a3f-317">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-320">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="76a3f-320">The name of the primary system owner.</span></span> <span data-ttu-id="76a3f-321">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-321">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-322">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="76a3f-322">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-323">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-325">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="76a3f-325">Provides high level status information.</span></span> <span data-ttu-id="76a3f-326">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="76a3f-326">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="76a3f-327">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="76a3f-327">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76a3f-328">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="76a3f-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="76a3f-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="76a3f-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="76a3f-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="76a3f-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="76a3f-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="76a3f-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="76a3f-335">)</span><span class="sxs-lookup"><span data-stu-id="76a3f-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76a3f-336">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="76a3f-336">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-337">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-339">Dernier État demandé ou souhaité pour l’élément passé à la méthode **RequestStateChange** , ou 12 (non applicable) si aucun changement d’État n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="76a3f-339">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="76a3f-340">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-340">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="76a3f-341">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="76a3f-341">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="76a3f-342">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76a3f-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-343">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="76a3f-343">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-344">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-346">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur 5 (non implémenté).</span><span class="sxs-lookup"><span data-stu-id="76a3f-346">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 5 (Not implemented).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-347">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="76a3f-347">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-348">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76a3f-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-350">Tableau de chaînes qui décrivent les rôles joués par le système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="76a3f-350">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="76a3f-351">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="76a3f-351">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-352">**État**</span><span class="sxs-lookup"><span data-stu-id="76a3f-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="76a3f-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-355">Chaîne qui spécifie l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="76a3f-355">A string that specifies the status of the element.</span></span> <span data-ttu-id="76a3f-356">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-357">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="76a3f-357">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-358">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="76a3f-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-360">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="76a3f-360">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-361">Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="76a3f-361">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="76a3f-362">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76a3f-362">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-363">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="76a3f-363">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-364">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="76a3f-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-366">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="76a3f-366">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="76a3f-367">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76a3f-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="76a3f-368">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="76a3f-368">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76a3f-369">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76a3f-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76a3f-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="76a3f-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76a3f-371">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="76a3f-371">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="76a3f-372">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76a3f-372">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76a3f-373">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76a3f-373">Requirements</span></span>



| <span data-ttu-id="76a3f-374">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76a3f-374">Requirement</span></span> | <span data-ttu-id="76a3f-375">Valeur</span><span class="sxs-lookup"><span data-stu-id="76a3f-375">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76a3f-376">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a3f-376">Minimum supported client</span></span><br/> | <span data-ttu-id="76a3f-377">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a3f-377">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="76a3f-378">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a3f-378">Minimum supported server</span></span><br/> | <span data-ttu-id="76a3f-379">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a3f-379">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76a3f-380">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76a3f-380">Namespace</span></span><br/>                | <span data-ttu-id="76a3f-381">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="76a3f-381">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="76a3f-382">MOF</span><span class="sxs-lookup"><span data-stu-id="76a3f-382">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76a3f-383"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76a3f-383"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76a3f-384">DLL</span><span class="sxs-lookup"><span data-stu-id="76a3f-384">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76a3f-385"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76a3f-385"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

