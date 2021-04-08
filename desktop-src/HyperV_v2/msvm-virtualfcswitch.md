---
description: Représente un commutateur de Fibre Channel virtuel.
ms.assetid: 4300747b-3ffc-4caf-8f0b-76cab6d2294e
title: Classe Msvm_VirtualFcSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitch
- Msvm_VirtualFcSwitch.SetPowerState
- Msvm_VirtualFcSwitch.InstanceID
- Msvm_VirtualFcSwitch.Caption
- Msvm_VirtualFcSwitch.Description
- Msvm_VirtualFcSwitch.ElementName
- Msvm_VirtualFcSwitch.InstallDate
- Msvm_VirtualFcSwitch.OperationalStatus
- Msvm_VirtualFcSwitch.StatusDescriptions
- Msvm_VirtualFcSwitch.Status
- Msvm_VirtualFcSwitch.HealthState
- Msvm_VirtualFcSwitch.CommunicationStatus
- Msvm_VirtualFcSwitch.DetailedStatus
- Msvm_VirtualFcSwitch.OperatingStatus
- Msvm_VirtualFcSwitch.PrimaryStatus
- Msvm_VirtualFcSwitch.EnabledState
- Msvm_VirtualFcSwitch.OtherEnabledState
- Msvm_VirtualFcSwitch.RequestedState
- Msvm_VirtualFcSwitch.EnabledDefault
- Msvm_VirtualFcSwitch.TimeOfLastStateChange
- Msvm_VirtualFcSwitch.AvailableRequestedStates
- Msvm_VirtualFcSwitch.TransitioningToState
- Msvm_VirtualFcSwitch.CreationClassName
- Msvm_VirtualFcSwitch.Name
- Msvm_VirtualFcSwitch.PrimaryOwnerName
- Msvm_VirtualFcSwitch.PrimaryOwnerContact
- Msvm_VirtualFcSwitch.Roles
- Msvm_VirtualFcSwitch.NameFormat
- Msvm_VirtualFcSwitch.OtherIdentifyingInfo
- Msvm_VirtualFcSwitch.IdentifyingDescriptions
- Msvm_VirtualFcSwitch.Dedicated
- Msvm_VirtualFcSwitch.OtherDedicatedDescriptions
- Msvm_VirtualFcSwitch.ResetCapability
- Msvm_VirtualFcSwitch.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66c6b7a284a2751b1c9b664428a9c90db9f468a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112291"
---
# <a name="msvm_virtualfcswitch-class"></a><span data-ttu-id="9475b-103">MSVM \_ VirtualFcSwitch, classe</span><span class="sxs-lookup"><span data-stu-id="9475b-103">Msvm\_VirtualFcSwitch class</span></span>

<span data-ttu-id="9475b-104">Représente un commutateur de Fibre Channel virtuel.</span><span class="sxs-lookup"><span data-stu-id="9475b-104">Represents a virtual Fibre Channel switch.</span></span> <span data-ttu-id="9475b-105">Chaque commutateur est associé à un port de Fibre Channel physique auquel de nombreux ports de Fibre Channel synthétiques peuvent être connectés.</span><span class="sxs-lookup"><span data-stu-id="9475b-105">Each switch is associated with one physical Fibre Channel port to which many synthetic Fibre Channel ports can be connected.</span></span> <span data-ttu-id="9475b-106">Le commutateur lui-même n’est pas hautement configurable et agit principalement comme un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="9475b-106">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="9475b-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9475b-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9475b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9475b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
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
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="9475b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9475b-109">Members</span></span>

<span data-ttu-id="9475b-110">La classe **MSVM \_ VirtualFcSwitch** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9475b-110">The **Msvm\_VirtualFcSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="9475b-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9475b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9475b-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9475b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9475b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9475b-113">Methods</span></span>

<span data-ttu-id="9475b-114">La classe **MSVM \_ VirtualFcSwitch** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9475b-114">The **Msvm\_VirtualFcSwitch** class has these methods.</span></span>



| <span data-ttu-id="9475b-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="9475b-115">Method</span></span>                                                                | <span data-ttu-id="9475b-116">Description</span><span class="sxs-lookup"><span data-stu-id="9475b-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="9475b-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9475b-117">**RequestStateChange**</span></span>](msvm-virtualfcswitch-requeststatechange.md) | <span data-ttu-id="9475b-118">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="9475b-118">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="9475b-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9475b-119">**SetPowerState**</span></span>                                                     | <span data-ttu-id="9475b-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9475b-120">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9475b-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9475b-121">Properties</span></span>

<span data-ttu-id="9475b-122">La classe **MSVM \_ VirtualFcSwitch** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9475b-122">The **Msvm\_VirtualFcSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9475b-123">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9475b-123">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-124">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-126">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="9475b-126">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="9475b-127">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9475b-127">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="9475b-128">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="9475b-128">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="9475b-129">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="9475b-129">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="9475b-130">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9475b-130">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9475b-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="9475b-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="9475b-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="9475b-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="9475b-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="9475b-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="9475b-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="9475b-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="9475b-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="9475b-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="9475b-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="9475b-141">)</span><span class="sxs-lookup"><span data-stu-id="9475b-141">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9475b-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9475b-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-145">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9475b-145">A short description of the object.</span></span> <span data-ttu-id="9475b-146">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9475b-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-148">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-150">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9475b-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9475b-151">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9475b-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9475b-152">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9475b-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9475b-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9475b-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="9475b-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="9475b-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="9475b-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9475b-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9475b-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9475b-160">)</span><span class="sxs-lookup"><span data-stu-id="9475b-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9475b-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9475b-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-164">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9475b-164">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="9475b-165">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="9475b-165">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-166">**Dédié**</span><span class="sxs-lookup"><span data-stu-id="9475b-166">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-167">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-169">Indique si le système informatique est un système à usage spécifique (dédié à une utilisation particulière) et s’il s’agit d’un système à usage général.</span><span class="sxs-lookup"><span data-stu-id="9475b-169">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="9475b-170">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur 0 (non dédié).</span><span class="sxs-lookup"><span data-stu-id="9475b-170">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-171">**Description**</span><span class="sxs-lookup"><span data-stu-id="9475b-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-174">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="9475b-174">A description of the object.</span></span> <span data-ttu-id="9475b-175">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9475b-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-177">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-179">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9475b-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9475b-180">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9475b-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9475b-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9475b-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="9475b-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="9475b-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="9475b-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="9475b-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="9475b-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="9475b-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9475b-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9475b-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9475b-190">)</span><span class="sxs-lookup"><span data-stu-id="9475b-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9475b-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9475b-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-194">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9475b-194">A display name for the object.</span></span> <span data-ttu-id="9475b-195">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-196">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9475b-196">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-197">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-199">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9475b-199">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9475b-200">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9475b-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9475b-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="9475b-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="9475b-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="9475b-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9475b-204">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9475b-204">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-205">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-207">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9475b-207">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9475b-208">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="9475b-208">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9475b-209">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 5 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="9475b-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-210">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9475b-210">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-213">Spécifie l’intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9475b-213">Specifies the current health of the element.</span></span> <span data-ttu-id="9475b-214">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9475b-214">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="9475b-215">Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9475b-215">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="9475b-216">La propriété **EnabledState** peut également contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9475b-216">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="9475b-217">Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).</span><span class="sxs-lookup"><span data-stu-id="9475b-217">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="9475b-218">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="9475b-219">Valeur</span><span class="sxs-lookup"><span data-stu-id="9475b-219">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="9475b-220">Signification</span><span class="sxs-lookup"><span data-stu-id="9475b-220">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="9475b-221"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9475b-221"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="9475b-222">L’élément est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.</span><span class="sxs-lookup"><span data-stu-id="9475b-222">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="9475b-223"><dt>**Erreur majeure**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="9475b-223"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="9475b-224">L’élément a subi un échec majeur.</span><span class="sxs-lookup"><span data-stu-id="9475b-224">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="9475b-225"><dt>**Erreur critique**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="9475b-225"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="9475b-226">L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible.</span><span class="sxs-lookup"><span data-stu-id="9475b-226">The element is nonfunctional and recovery might not be possible.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="9475b-227">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9475b-227">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-228">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9475b-228">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-230">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-230">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9475b-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-232">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9475b-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-234">Date et heure de création de la configuration d’ordinateur virtuel pour un ordinateur virtuel, ou **valeur null**, pour un système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="9475b-234">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="9475b-235">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-236">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9475b-236">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9475b-239">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="9475b-239">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9475b-240">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9475b-240">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9475b-241">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-241">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-242">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9475b-242">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-245">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="9475b-245">The label by which the object is known.</span></span> <span data-ttu-id="9475b-246">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="9475b-246">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-247">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="9475b-247">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-250">Chaîne qui identifie la façon dont le nom système a été généré, à l’aide de la méthode heuristique de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="9475b-250">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="9475b-251">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-251">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-252">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9475b-252">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-253">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-255">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9475b-255">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9475b-256">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9475b-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9475b-257">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9475b-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9475b-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9475b-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="9475b-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="9475b-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="9475b-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="9475b-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="9475b-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="9475b-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="9475b-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="9475b-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="9475b-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="9475b-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="9475b-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="9475b-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="9475b-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="9475b-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="9475b-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9475b-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9475b-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9475b-277">)</span><span class="sxs-lookup"><span data-stu-id="9475b-277">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9475b-278">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9475b-278">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-279">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-281">Tableau qui contient les États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9475b-281">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="9475b-282">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-283">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9475b-283">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-284">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9475b-284">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-286">Chaîne qui décrit comment ou pourquoi le système est dédié lorsque le tableau **dédié** comprend la valeur 2 (autre).</span><span class="sxs-lookup"><span data-stu-id="9475b-286">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="9475b-287">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-287">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-288">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9475b-288">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-291">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="9475b-291">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9475b-292">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="9475b-292">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9475b-293">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-293">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-294">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9475b-294">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-295">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9475b-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-297">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-298">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9475b-298">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-299">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-299">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-301">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9475b-301">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-302">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="9475b-302">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-305">Chaîne qui indique comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="9475b-305">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="9475b-306">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-306">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-307">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="9475b-307">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-310">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="9475b-310">The name of the primary system owner.</span></span> <span data-ttu-id="9475b-311">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-311">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-312">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9475b-312">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-313">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-315">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="9475b-315">Provides high level status information.</span></span> <span data-ttu-id="9475b-316">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9475b-316">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9475b-317">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9475b-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9475b-318">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9475b-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="9475b-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="9475b-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="9475b-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="9475b-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9475b-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9475b-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="9475b-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9475b-325">)</span><span class="sxs-lookup"><span data-stu-id="9475b-325">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9475b-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9475b-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-327">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-329">Dernier État demandé ou souhaité pour l’élément passé à la méthode **RequestStateChange** , ou 12 (non applicable) si aucun changement d’État n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="9475b-329">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="9475b-330">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="9475b-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9475b-331">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="9475b-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9475b-332">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9475b-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-333">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="9475b-333">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-334">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-336">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span><span class="sxs-lookup"><span data-stu-id="9475b-336">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-337">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="9475b-337">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-338">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9475b-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-340">Tableau de chaînes qui décrivent les rôles joués par le système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="9475b-340">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="9475b-341">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9475b-341">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9475b-342">**État**</span><span class="sxs-lookup"><span data-stu-id="9475b-342">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9475b-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-345">Chaîne qui spécifie l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9475b-345">A string that specifies the status of the element.</span></span> <span data-ttu-id="9475b-346">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-346">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-347">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9475b-347">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-348">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9475b-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9475b-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9475b-350">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="9475b-350">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9475b-351">Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="9475b-351">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="9475b-352">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9475b-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-353">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9475b-353">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-354">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9475b-354">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-356">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9475b-356">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9475b-357">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9475b-357">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9475b-358">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9475b-358">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9475b-359">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9475b-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9475b-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9475b-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9475b-361">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="9475b-361">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9475b-362">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9475b-362">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9475b-363">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9475b-363">Requirements</span></span>



| <span data-ttu-id="9475b-364">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9475b-364">Requirement</span></span> | <span data-ttu-id="9475b-365">Valeur</span><span class="sxs-lookup"><span data-stu-id="9475b-365">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9475b-366">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9475b-366">Minimum supported client</span></span><br/> | <span data-ttu-id="9475b-367">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9475b-367">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9475b-368">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9475b-368">Minimum supported server</span></span><br/> | <span data-ttu-id="9475b-369">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9475b-369">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9475b-370">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9475b-370">Namespace</span></span><br/>                | <span data-ttu-id="9475b-371">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9475b-371">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9475b-372">MOF</span><span class="sxs-lookup"><span data-stu-id="9475b-372">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9475b-373"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9475b-373"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9475b-374">DLL</span><span class="sxs-lookup"><span data-stu-id="9475b-374">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9475b-375"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9475b-375"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

