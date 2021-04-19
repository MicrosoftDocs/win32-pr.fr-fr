---
description: Représente un ordinateur virtuel planifié.
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522209"
---
# <a name="msvm_plannedcomputersystem-class"></a><span data-ttu-id="9798b-103">MSVM \_ PlannedComputerSystem, classe</span><span class="sxs-lookup"><span data-stu-id="9798b-103">Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="9798b-104">Représente un ordinateur virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="9798b-104">Represents a planned virtual machine.</span></span>

<span data-ttu-id="9798b-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9798b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9798b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9798b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a><span data-ttu-id="9798b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9798b-107">Members</span></span>

<span data-ttu-id="9798b-108">La classe **MSVM \_ PlannedComputerSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9798b-108">The **Msvm\_PlannedComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="9798b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9798b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9798b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9798b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9798b-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9798b-111">Methods</span></span>

<span data-ttu-id="9798b-112">La classe **MSVM \_ PlannedComputerSystem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9798b-112">The **Msvm\_PlannedComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="9798b-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="9798b-113">Method</span></span>                                                                      | <span data-ttu-id="9798b-114">Description</span><span class="sxs-lookup"><span data-stu-id="9798b-114">Description</span></span>                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9798b-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9798b-115">**RequestStateChange**</span></span>](requeststatechange-msvm-plannedcomputersystem.md) | <span data-ttu-id="9798b-116">Demande que l’état du système planifié soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9798b-116">Requests that the state of the planned system be changed to the value specified.</span></span><br/> |
| <span data-ttu-id="9798b-117">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9798b-117">**SetPowerState**</span></span>                                                           | <span data-ttu-id="9798b-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9798b-118">This method is not supported.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="9798b-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9798b-119">Properties</span></span>

<span data-ttu-id="9798b-120">La classe **MSVM \_ PlannedComputerSystem** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9798b-120">The **Msvm\_PlannedComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9798b-121">**AssignedNumaNodeList**</span><span class="sxs-lookup"><span data-stu-id="9798b-121">**AssignedNumaNodeList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-122">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9798b-124">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="9798b-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9798b-125">Tableau de nœuds NUMA (non-Uniform Memory Access) actuellement attribués à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9798b-125">An array of nonuniform memory access (NUMA) nodes that are currently assigned to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9798b-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-127">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-129">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="9798b-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="9798b-130">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9798b-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="9798b-131">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="9798b-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="9798b-132">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="9798b-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="9798b-133">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9798b-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9798b-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="9798b-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="9798b-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="9798b-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="9798b-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="9798b-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="9798b-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="9798b-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="9798b-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="9798b-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9798b-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="9798b-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="9798b-144">)</span><span class="sxs-lookup"><span data-stu-id="9798b-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9798b-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9798b-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-148">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9798b-148">A short description of the object.</span></span> <span data-ttu-id="9798b-149">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « ordinateur virtuel planifié ».</span><span class="sxs-lookup"><span data-stu-id="9798b-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="9798b-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9798b-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-153">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9798b-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9798b-154">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9798b-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9798b-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9798b-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9798b-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9798b-159">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9798b-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="9798b-160">Indique le nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="9798b-160">Indicates the name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="9798b-161">Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="9798b-161">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="9798b-162">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-162">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-163">**Dédié**</span><span class="sxs-lookup"><span data-stu-id="9798b-163">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-164">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-166">Tableau de valeurs qui indiquent les rôles qui sont dédiés au système prévu, le cas échéant, et les fonctionnalités fournies.</span><span class="sxs-lookup"><span data-stu-id="9798b-166">An array of values that indicate the purposes to which the planned system is dedicated, if any, and what functionality is provided.</span></span> <span data-ttu-id="9798b-167">Par exemple, il est possible de spécifier que le système est dédié à l’impression (valeur = 11) ou qu’il agit comme un « Hub » (valeur = 8).</span><span class="sxs-lookup"><span data-stu-id="9798b-167">For example, one could specify that the System is dedicated to "Print" (value=11) or acts as a "Hub" (value=8).</span></span> <span data-ttu-id="9798b-168">Vous pouvez également indiquer plusieurs objectifs.</span><span class="sxs-lookup"><span data-stu-id="9798b-168">Multiple purposes can also be indicated.</span></span> <span data-ttu-id="9798b-169">Par exemple, il s’agit d’un système à usage général indiquant « non dédié » (valeur = 0), mais qui héberge également les services « imprimer » (valeur = 11) ou « périphérique utilisateur mobile » (valeur = 17).</span><span class="sxs-lookup"><span data-stu-id="9798b-169">For example, this is a general purpose system indicating "Not Dedicated" (value=0) but that it also hosts "Print" (value=11) or "Mobile User Device" (value=17) services.</span></span>

<span data-ttu-id="9798b-170">Cette propriété est héritée de la classe [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="9798b-170">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="9798b-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-171">Value</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="9798b-172">Signification</span><span class="sxs-lookup"><span data-stu-id="9798b-172">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <span data-ttu-id="9798b-173"><dt>**Non dédié**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-173"><dt>**Not Dedicated**</dt> <dt>0</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9798b-174"><dt>**Inconnu**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-174"><dt>**Unknown**</dt> <dt>1</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9798b-175"><dt>**Autre**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-175"><dt>**Other**</dt> <dt>2</dt></span></span> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <span data-ttu-id="9798b-176"><dt>**Stockage**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-176"><dt>**Storage**</dt> <dt>3</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <span data-ttu-id="9798b-177"><dt>**Routeur**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-177"><dt>**Router**</dt> <dt>4</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <span data-ttu-id="9798b-178"><dt>**Commutateur**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-178"><dt>**Switch**</dt> <dt>5</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <span data-ttu-id="9798b-179"><dt>**Commutateur de couche 3**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-179"><dt>**Layer 3 Switch**</dt> <dt>6</dt></span></span> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <span data-ttu-id="9798b-180"><dt>**Commutateur Office central**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-180"><dt>**Central Office Switch**</dt> <dt>7</dt></span></span> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <span data-ttu-id="9798b-181"><dt>**Hub**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-181"><dt>**Hub**</dt> <dt>8</dt></span></span> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <span data-ttu-id="9798b-182"><dt>**Accès au serveur**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-182"><dt>**Access Server**</dt> <dt>9</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <span data-ttu-id="9798b-183"><dt>**Pare-feu**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-183"><dt>**Firewall**</dt> <dt>10</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <span data-ttu-id="9798b-184"><dt>**Imprimer**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-184"><dt>**Print**</dt> <dt>11</dt></span></span> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <span data-ttu-id="9798b-185"><dt>**E/s**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-185"><dt>**I/O**</dt> <dt>12</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <span data-ttu-id="9798b-186"><dt>**Mise en cache Web**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-186"><dt>**Web Caching**</dt> <dt>13</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <span data-ttu-id="9798b-187"><dt>**Gestion**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-187"><dt>**Management**</dt> <dt>14</dt></span></span> </dl>                                                                 | <span data-ttu-id="9798b-188">Indique que cette instance est dédiée à l’hébergement du logiciel de gestion du système.</span><span class="sxs-lookup"><span data-stu-id="9798b-188">Indicates this instance is dedicated to hosting system management software.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <span data-ttu-id="9798b-189"><dt>**Bloquer le serveur**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-189"><dt>**Block Server**</dt> <dt>15</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <span data-ttu-id="9798b-190"><dt>**Serveur de fichiers**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-190"><dt>**File Server**</dt> <dt>16</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <span data-ttu-id="9798b-191"><dt>**Appareil utilisateur mobile**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-191"><dt>**Mobile User Device**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="9798b-192">Par exemple, un appareil utilisateur mobile dédié est un téléphone mobile ou un scanneur de code-barres dans un magasin qui communique à l’aide de la fréquence radio.</span><span class="sxs-lookup"><span data-stu-id="9798b-192">An example of a dedicated mobile user device is a mobile phone or a bar code scanner in a store that communicates through radio frequency.</span></span> <span data-ttu-id="9798b-193">Ces systèmes sont assez limités en matière de fonctionnalité et de programmabilité, et ne sont pas considérés comme des plateformes informatiques à usage général.</span><span class="sxs-lookup"><span data-stu-id="9798b-193">These systems are quite limited in functionality and programmability, and are not considered general purpose computing platforms.</span></span> <span data-ttu-id="9798b-194">Un exemple de système mobile à usage général (autrement dit, qui n’est pas dédié) est un ordinateur autonome.</span><span class="sxs-lookup"><span data-stu-id="9798b-194">Alternately, an example of a mobile system that is general purpose (that is, is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="9798b-195">Bien qu’elles soient limitées dans sa programmation, de nouveaux logiciels peuvent être téléchargés et leurs fonctionnalités développées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9798b-195">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span> <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <span data-ttu-id="9798b-196"><dt>**Répéteur**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-196"><dt>**Repeater**</dt> <dt>18</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <span data-ttu-id="9798b-197"><dt>**Pont/extendeur**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span></span> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <span data-ttu-id="9798b-198"><dt>**Passerelle**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-198"><dt>**Gateway**</dt> <dt>20</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <span data-ttu-id="9798b-199"><dt>**Virtualisation du stockage**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-199"><dt>**Storage Virtualizer**</dt> <dt>21</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <span data-ttu-id="9798b-200"><dt>**Bibliothèque multimédia**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-200"><dt>**Media Library**</dt> <dt>22</dt></span></span> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <span data-ttu-id="9798b-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <span data-ttu-id="9798b-202"><dt>**NAS-tête**</dt> <dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-202"><dt>**NAS Head**</dt> <dt>24</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <span data-ttu-id="9798b-203"><dt>**NAS autonome**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-203"><dt>**Self-contained NAS**</dt> <dt>25</dt></span></span> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <span data-ttu-id="9798b-204"><dt>**UPS**</dt> <dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-204"><dt>**UPS**</dt> <dt>26</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <span data-ttu-id="9798b-205"><dt>**Téléphone IP**</dt> <dt>27</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-205"><dt>**IP Phone**</dt> <dt>27</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <span data-ttu-id="9798b-206"><dt>**Contrôleur de gestion**</dt> <dt>28</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-206"><dt>**Management Controller**</dt> <dt>28</dt></span></span> </dl>                     | <span data-ttu-id="9798b-207">Indique que cette instance représente un matériel spécialisé dédié à la gestion des systèmes (c’est-à-dire un contrôleur de gestion de la carte de configuration (BMC) ou un processeur de service).</span><span class="sxs-lookup"><span data-stu-id="9798b-207">Indicates this instance represents specialized hardware dedicated to systems management (that is, a Baseboard Management Controller (BMC) or service processor).</span></span> <span data-ttu-id="9798b-208">L’étendue de gestion d’un contrôleur de gestion est généralement un système géré unique dans lequel il est contenu.</span><span class="sxs-lookup"><span data-stu-id="9798b-208">The management scope of a Management Controller is typically a single managed system in which it is contained.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <span data-ttu-id="9798b-209"><dt>**Gestionnaire de châssis**</dt> <dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span></span> </dl>                                             | <span data-ttu-id="9798b-210">Indique que cette instance représente un système dédié à la gestion d’un châssis de panneau et de ses appareils contenus.</span><span class="sxs-lookup"><span data-stu-id="9798b-210">Indicates this instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="9798b-211">Cette valeur est utilisée pour représenter un contrôleur de tablette.</span><span class="sxs-lookup"><span data-stu-id="9798b-211">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="9798b-212">Un gestionnaire de châssis est un point d’agrégation pour la gestion et peut reposer sur des contrôleurs de gestion subordonnés pour la gestion des composants constitutifs.</span><span class="sxs-lookup"><span data-stu-id="9798b-212">A Chassis Manager is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span> <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <span data-ttu-id="9798b-213"><dt>**Contrôleur RAID basé sur l’hôte**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-213"><dt>**Host-based RAID controller**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="9798b-214">Indique que cette instance représente un contrôleur de stockage RAID contenu dans un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="9798b-214">Indicates this instance represents a RAID storage controller contained within a host computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <span data-ttu-id="9798b-215"><dt>**Boîtier du dispositif de stockage**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-215"><dt>**Storage Device Enclosure**</dt> <dt>31</dt></span></span> </dl>         | <span data-ttu-id="9798b-216">Indique que cette instance représente un boîtier qui contient des dispositifs de stockage.</span><span class="sxs-lookup"><span data-stu-id="9798b-216">Indicates this instance represents an enclosure that contains storage devices.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <span data-ttu-id="9798b-217"><dt>**Bureau**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-217"><dt>**Desktop**</dt> <dt>32</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <span data-ttu-id="9798b-218"><dt>**Ordinateur portable**</dt> <dt>33</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-218"><dt>**Laptop**</dt> <dt>33</dt></span></span> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <span data-ttu-id="9798b-219"><dt>**Bibliothèque de bandes virtuelle**</dt> <dt>34</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-219"><dt>**Virtual Tape Library**</dt> <dt>34</dt></span></span> </dl>                         | <span data-ttu-id="9798b-220">Émulation d’une bibliothèque de bandes par un système de bibliothèque virtuelle.</span><span class="sxs-lookup"><span data-stu-id="9798b-220">The emulation of a tape library by a Virtual Library System.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <span data-ttu-id="9798b-221"><dt>**Système de bibliothèque virtuelle**</dt> <dt>35</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-221"><dt>**Virtual Library System**</dt> <dt>35</dt></span></span> </dl>                 | <span data-ttu-id="9798b-222">Utilise le stockage sur disque pour émuler les bibliothèques de bandes.</span><span class="sxs-lookup"><span data-stu-id="9798b-222">Uses disk storage to emulate tape libraries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <span data-ttu-id="9798b-223"><dt>**PC réseau/client léger**</dt> <dt>36</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-223"><dt>**Network PC/Thin Client**</dt> <dt>36</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <span data-ttu-id="9798b-224"><dt>**Commutateur FC**</dt> <dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-224"><dt>**FC Switch**</dt> <dt>37</dt></span></span> </dl>                                                                     | <span data-ttu-id="9798b-225">Indique que cette instance est dédiée au basculement des frames de couche 2 Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="9798b-225">Indicates this instance is dedicated to switching layer 2 Fibre Channel frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <span data-ttu-id="9798b-226"><dt>**Commutateur Ethernet**</dt> <dt>38</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-226"><dt>**Ethernet Switch**</dt> <dt>38</dt></span></span> </dl>                                             | <span data-ttu-id="9798b-227">Indique que cette instance est dédiée au basculement des frames Ethernet de couche 2.</span><span class="sxs-lookup"><span data-stu-id="9798b-227">Indicates this instance is dedicated to switching layer 2 Ethernet frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9798b-228"><dt>**DMTF réservé**</dt> <dt>39.. 32567</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-228"><dt>**DMTF Reserved**</dt> <dt>39..32567</dt></span></span> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9798b-229">32568 <dt> **réservé du fournisseur**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-229"><dt>**Vendor Reserved** </dt> <dt>32568..65535</dt></span></span> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="9798b-230">**Description**</span><span class="sxs-lookup"><span data-stu-id="9798b-230">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-233">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="9798b-233">A description of the object.</span></span> <span data-ttu-id="9798b-234">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « machine virtuelle planifiée Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="9798b-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="9798b-235">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9798b-235">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-236">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-238">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9798b-238">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9798b-239">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9798b-239">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9798b-240">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9798b-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-241">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9798b-241">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-244">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9798b-244">A display name for the object.</span></span> <span data-ttu-id="9798b-245">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9798b-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-246">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9798b-246">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-247">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-249">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9798b-249">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9798b-250">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9798b-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and can be one of the following values.</span></span>



| <span data-ttu-id="9798b-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9798b-252">Signification</span><span class="sxs-lookup"><span data-stu-id="9798b-252">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9798b-253"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-253"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9798b-254">Le système est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9798b-254">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="9798b-255"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-255"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="9798b-256">Le système est activé, mais il est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9798b-256">The system is enabled, but offline.</span></span> <span data-ttu-id="9798b-257">Toutes les nouvelles demandes seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="9798b-257">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9798b-258">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9798b-258">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-259">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-261">Spécifie l’état activé du système planifié.</span><span class="sxs-lookup"><span data-stu-id="9798b-261">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="9798b-262">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9798b-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="9798b-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-263">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9798b-264">Signification</span><span class="sxs-lookup"><span data-stu-id="9798b-264">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9798b-265"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-265"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9798b-266">Le système est désactivé.</span><span class="sxs-lookup"><span data-stu-id="9798b-266">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="9798b-267"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-267"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="9798b-268">Le système est activé, mais il est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9798b-268">The system is enabled, but offline.</span></span> <span data-ttu-id="9798b-269">Toutes les nouvelles demandes seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="9798b-269">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9798b-270">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9798b-270">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-271">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-271">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-273">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9798b-273">The current health of the element.</span></span> <span data-ttu-id="9798b-274">Cette propriété exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9798b-274">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9798b-275">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="9798b-275">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9798b-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="9798b-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="9798b-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-277">Value</span></span>                                                                        | <span data-ttu-id="9798b-278">Signification</span><span class="sxs-lookup"><span data-stu-id="9798b-278">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="9798b-279"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-279"><dt>5</dt></span></span> </dl> | <span data-ttu-id="9798b-280">L’état d’intégrité est normal.</span><span class="sxs-lookup"><span data-stu-id="9798b-280">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9798b-281">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9798b-281">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-282">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9798b-282">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-284">Tableau de chaînes fournissant des explications et des détails sur les entrées du tableau **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="9798b-284">An array of strings providing explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="9798b-285">Chaque entrée de ce tableau est liée à l’entrée dans **OtherIdentifyingInfo** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="9798b-285">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="9798b-286">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-286">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-287">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9798b-287">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-288">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9798b-288">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-290">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9798b-290">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9798b-291">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9798b-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-292">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9798b-292">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9798b-295">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="9798b-295">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9798b-296">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="9798b-296">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9798b-297">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9798b-297">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-298">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9798b-298">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9798b-301">Qualificateurs : **clé**, **remplacement**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9798b-301">Qualifiers: **Key**, **Override**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="9798b-302">Le nom hérité sert de clé d’une instance système dans un environnement d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9798b-302">The inherited name serves as the key of a system instance in an enterprise environment.</span></span> <span data-ttu-id="9798b-303">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-303">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-304">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="9798b-304">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9798b-307">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="9798b-307">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="9798b-308">Identifie la manière dont le nom du système a été généré, à l’aide de l’heuristique de la sous-classe.</span><span class="sxs-lookup"><span data-stu-id="9798b-308">Identifies how the system name was generated, using the heuristic of the subclass.</span></span> <span data-ttu-id="9798b-309">L’objet système et ses dérivés sont des objets de niveau supérieur de CIM.</span><span class="sxs-lookup"><span data-stu-id="9798b-309">The system object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="9798b-310">Ils fournissent l’étendue de nombreux composants.</span><span class="sxs-lookup"><span data-stu-id="9798b-310">They provide the scope for numerous components.</span></span> <span data-ttu-id="9798b-311">Une clé système unique est requise.</span><span class="sxs-lookup"><span data-stu-id="9798b-311">Having unique system keys is required.</span></span> <span data-ttu-id="9798b-312">Une heuristique peut être définie dans les sous-classes système individuelles pour tenter de toujours générer la même clé de nom système.</span><span class="sxs-lookup"><span data-stu-id="9798b-312">A heuristic can be defined in individual system subclasses to attempt to always generate the same system name key.</span></span> <span data-ttu-id="9798b-313">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-313">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-314">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="9798b-314">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-315">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9798b-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9798b-317">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)</span><span class="sxs-lookup"><span data-stu-id="9798b-317">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="9798b-318">Durée totale, en millisecondes, depuis l’activation, la réinitialisation ou la restauration de la dernière machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="9798b-318">The total time, in milliseconds, since the virtual machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="9798b-319">Cette fois, vous excluez l’heure à laquelle la machine virtuelle était à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="9798b-319">This time excludes the time the virtual machine was in the paused state.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9798b-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-321">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-323">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9798b-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9798b-324">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9798b-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9798b-325">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9798b-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9798b-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-327">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-329">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9798b-329">The current statuses of the object.</span></span> <span data-ttu-id="9798b-330">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="9798b-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-331">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9798b-331">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-332">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9798b-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-334">Chaîne décrivant la manière ou la raison pour laquelle le système est dédié lorsque le tableau dédié comprend la valeur 2, « other ».</span><span class="sxs-lookup"><span data-stu-id="9798b-334">A string describing how or why the system is dedicated when the Dedicated array includes the value 2, "Other".</span></span> <span data-ttu-id="9798b-335">Cette propriété est héritée de la classe [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="9798b-335">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9798b-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-339">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="9798b-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="9798b-340">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="9798b-340">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9798b-341">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="9798b-341">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9798b-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-343">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9798b-343">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9798b-345">Qualificateurs : **clé**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9798b-345">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="9798b-346">Contient des données supplémentaires, au-delà des informations sur le nom du système, qui peuvent être utilisées pour identifier un ComputerSystem.</span><span class="sxs-lookup"><span data-stu-id="9798b-346">Contains additional data, beyond system name information, that can be used to identify a ComputerSystem.</span></span> <span data-ttu-id="9798b-347">Par exemple, vous pouvez conserver le nom WWN (World-World Name) Fibre Channel d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="9798b-347">One example would be to hold the Fibre Channel World-Wide Name (WWN) of a node.</span></span> <span data-ttu-id="9798b-348">Si seul le nom de Fibre Channel est disponible et qu’il est unique (en mesure d’être utilisé comme clé système), cette propriété est **null** et le nom WWN devient la clé système, ses données placées dans la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="9798b-348">If only the Fibre Channel name is available and is unique (able to be used as the system key), then this property would be **Null** and the WWN would become the system key, its data placed in the **Name** property.</span></span> <span data-ttu-id="9798b-349">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-349">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9798b-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-351">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-353">Cette propriété est héritée de la classe [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , mais elle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9798b-353">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class, but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-354">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="9798b-354">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-356">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9798b-356">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9798b-357">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="9798b-357">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="9798b-358">Chaîne qui fournit des informations sur la façon dont le propriétaire principal du système est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="9798b-358">A string that provides information on how the primary system owner can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="9798b-359">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-359">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-360">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="9798b-360">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-362">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9798b-362">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9798b-363">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="9798b-363">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="9798b-364">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="9798b-364">The name of the primary system owner.</span></span> <span data-ttu-id="9798b-365">Le propriétaire du système est l’utilisateur principal du système.</span><span class="sxs-lookup"><span data-stu-id="9798b-365">The system owner is the primary user of the system.</span></span> <span data-ttu-id="9798b-366">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-366">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-367">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9798b-367">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-368">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-370">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="9798b-370">Provides high level status information.</span></span> <span data-ttu-id="9798b-371">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="9798b-371">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="9798b-372">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="9798b-372">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9798b-373">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9798b-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9798b-374">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="9798b-374">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-375">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9798b-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-377">Identificateur du processus sous lequel cet ordinateur virtuel est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9798b-377">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="9798b-378">Cette valeur peut être utilisée pour identifier de façon unique l’instance de Vmwp.exe sur le système qui exécute l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9798b-378">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-379">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9798b-379">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-380">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-382">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="9798b-382">The last requested or desired state for the element.</span></span> <span data-ttu-id="9798b-383">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="9798b-383">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9798b-384">Cette propriété est fournie pour comparer les derniers États demandés et actuels d’un élément.</span><span class="sxs-lookup"><span data-stu-id="9798b-384">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="9798b-385">Une instance particulière de la [**classe \_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la propriété **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="9798b-385">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="9798b-386">Si cela se produit, la valeur 12 (« non applicable ») est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9798b-386">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="9798b-387">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="9798b-387">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="9798b-388">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-388">Value</span></span>                                                                         | <span data-ttu-id="9798b-389">Signification</span><span class="sxs-lookup"><span data-stu-id="9798b-389">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="9798b-390"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-390"><dt>12</dt></span></span> </dl> | <span data-ttu-id="9798b-391">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="9798b-391">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9798b-392">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="9798b-392">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-393">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-395">Spécifie les fonctionnalités de réinitialisation du système informatique.</span><span class="sxs-lookup"><span data-stu-id="9798b-395">Specifies the reset capabilities of the computer system.</span></span> <span data-ttu-id="9798b-396">Cette propriété est héritée de la classe [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="9798b-396">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="9798b-397">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-397">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="9798b-398">Signification</span><span class="sxs-lookup"><span data-stu-id="9798b-398">Meaning</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9798b-399"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-399"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9798b-400"><dt>**Inconnu**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-400"><dt>**Unknown**</dt> <dt>2</dt></span></span> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9798b-401"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-401"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                  | <span data-ttu-id="9798b-402">La réinitialisation du matériel n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="9798b-402">Hardware reset is not allowed.</span></span> <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="9798b-403"><dt>**Activé**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-403"><dt>**Enabled**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="9798b-404">Le système informatique peut être réinitialisé à l’aide de matériel (par exemple, les boutons d’alimentation et de réinitialisation).</span><span class="sxs-lookup"><span data-stu-id="9798b-404">The computer system can be reset by using hardware (for example, the power and reset buttons).</span></span> <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <span data-ttu-id="9798b-405"><dt> **Non implémenté**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-405"><dt>**Not Implemented** </dt> <dt>5 </dt></span></span> </dl> |                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="9798b-406">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="9798b-406">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-407">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9798b-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-408">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9798b-408">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9798b-409">Tableau de chaînes qui spécifie les rôles définis par l’administrateur que ce système joue dans l’environnement géré.</span><span class="sxs-lookup"><span data-stu-id="9798b-409">An array of strings that specifies the administrator-defined roles this system plays in the managed environment.</span></span> <span data-ttu-id="9798b-410">Il peut s’agir, par exemple, du « bâtiment 8 Print Server » ou des « Boise User Directors ».</span><span class="sxs-lookup"><span data-stu-id="9798b-410">Examples might be "Building 8 print server" or "Boise user directories".</span></span> <span data-ttu-id="9798b-411">Un système unique peut exécuter plusieurs rôles.</span><span class="sxs-lookup"><span data-stu-id="9798b-411">A single system may perform multiple roles.</span></span> <span data-ttu-id="9798b-412">La vue d’instrumentation des rôles d’un système est définie en instanciant une sous-classe spécifique du système, ou des propriétés d’une sous-classe, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="9798b-412">The instrumentation view of the roles of a system is defined by instantiating a specific subclass of system, or by properties in a subclass, or both.</span></span> <span data-ttu-id="9798b-413">Par exemple, l’objectif d’un ComputerSystem est défini à l’aide des propriétés **dédiées** et **OtherDedicatedDescription** .</span><span class="sxs-lookup"><span data-stu-id="9798b-413">For example, the purpose of a ComputerSystem is defined using the **Dedicated** and **OtherDedicatedDescription** properties.</span></span> <span data-ttu-id="9798b-414">Cette propriété est héritée de la classe [**\_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="9798b-414">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-415">**État**</span><span class="sxs-lookup"><span data-stu-id="9798b-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-416">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9798b-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-418">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9798b-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9798b-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-420">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="9798b-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9798b-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-422">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9798b-422">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9798b-423">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur « le service s’exécute normalement ».</span><span class="sxs-lookup"><span data-stu-id="9798b-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="9798b-424">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="9798b-424">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-425">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9798b-425">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-427">Date et heure de la dernière modification du fichier de configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="9798b-427">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="9798b-428">Le fichier de configuration est modifié lors de certaines opérations d’ordinateur virtuel, ainsi que lors de l’ajout, de la modification ou de la suppression de l’un des paramètres de l’ordinateur virtuel ou de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9798b-428">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-429">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9798b-429">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-430">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9798b-430">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-432">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9798b-432">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9798b-433">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9798b-433">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9798b-434">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9798b-434">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9798b-435">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9798b-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9798b-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9798b-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9798b-437">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="9798b-437">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9798b-438">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9798b-438">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9798b-439">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-439">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="9798b-440">Signification</span><span class="sxs-lookup"><span data-stu-id="9798b-440">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9798b-441"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-441"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="9798b-442"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-442"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9798b-443"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-443"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="9798b-444"><dt>**Arrêter**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-444"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="9798b-445"><dt>**Aucune modification**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-445"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="9798b-446">Aucune transition n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="9798b-446">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="9798b-447"><dt>**Hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-447"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="9798b-448"><dt>**Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-448"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="9798b-449"><dt>**Différer**</dt> de <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-449"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="9798b-450"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-450"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="9798b-451"><dt>**Redémarrer**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-451"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="9798b-452"><dt>**Réinitialiser**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-452"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="9798b-453"><dt>**Non applicable**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-453"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="9798b-454">L’implémentation ne prend pas en charge la représentation des transitions en cours.</span><span class="sxs-lookup"><span data-stu-id="9798b-454">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="9798b-455"><dt> **DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-455"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9798b-456">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9798b-456">Requirements</span></span>



| <span data-ttu-id="9798b-457">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9798b-457">Requirement</span></span> | <span data-ttu-id="9798b-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="9798b-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9798b-459">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9798b-459">Minimum supported client</span></span><br/> | <span data-ttu-id="9798b-460">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9798b-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9798b-461">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9798b-461">Minimum supported server</span></span><br/> | <span data-ttu-id="9798b-462">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9798b-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9798b-463">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9798b-463">Namespace</span></span><br/>                | <span data-ttu-id="9798b-464">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9798b-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9798b-465">MOF</span><span class="sxs-lookup"><span data-stu-id="9798b-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9798b-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9798b-467">DLL</span><span class="sxs-lookup"><span data-stu-id="9798b-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9798b-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9798b-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9798b-469">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9798b-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9798b-470">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="9798b-470">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="9798b-471">**MSVM \_ VirtualSystemManagementService. Méthode ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="9798b-471">**Msvm\_VirtualSystemManagementService .ImportSystemDefinition method**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

