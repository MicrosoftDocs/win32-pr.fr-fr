---
description: Représente un contrôleur IDE.
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Classe Msvm_IDEController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25da1bddfa029ca5a6892006283e322d91a328a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514859"
---
# <a name="msvm_idecontroller-class"></a><span data-ttu-id="73260-103">MSVM \_ IDEController, classe</span><span class="sxs-lookup"><span data-stu-id="73260-103">Msvm\_IDEController class</span></span>

<span data-ttu-id="73260-104">Représente un contrôleur IDE.</span><span class="sxs-lookup"><span data-stu-id="73260-104">Represents an IDE controller.</span></span> <span data-ttu-id="73260-105">Cette classe peut prendre en charge jusqu’à quatre lecteurs attachés au contrôleur.</span><span class="sxs-lookup"><span data-stu-id="73260-105">This class can support up to four drives attached to the controller.</span></span> <span data-ttu-id="73260-106">Le contrôleur IDE est fixe dans l’ordinateur virtuel et n’est donc pas associé à un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="73260-106">The IDE controller is fixed in the virtual machine and therefore does not have a resource pool associated with it.</span></span>

> [!Note]  
> <span data-ttu-id="73260-107">Cette classe n’est pas disponible pour les ordinateurs virtuels de génération 2.</span><span class="sxs-lookup"><span data-stu-id="73260-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="73260-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="73260-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="73260-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73260-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_IDEController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a><span data-ttu-id="73260-110">Membres</span><span class="sxs-lookup"><span data-stu-id="73260-110">Members</span></span>

<span data-ttu-id="73260-111">La classe **MSVM \_ IDEController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="73260-111">The **Msvm\_IDEController** class has these types of members:</span></span>

-   [<span data-ttu-id="73260-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="73260-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="73260-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73260-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73260-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="73260-114">Methods</span></span>

<span data-ttu-id="73260-115">La classe **MSVM \_ IDEController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="73260-115">The **Msvm\_IDEController** class has these methods.</span></span>



| <span data-ttu-id="73260-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="73260-116">Method</span></span>                                                              | <span data-ttu-id="73260-117">Description</span><span class="sxs-lookup"><span data-stu-id="73260-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="73260-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="73260-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="73260-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73260-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73260-120">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="73260-120">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="73260-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73260-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73260-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="73260-122">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="73260-123">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73260-123">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="73260-124">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="73260-124">**RequestStateChange**</span></span>](msvm-idecontroller-requeststatechange.md) | <span data-ttu-id="73260-125">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="73260-125">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="73260-126">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="73260-126">**Reset**</span></span>](msvm-idecontroller-reset.md)                           | <span data-ttu-id="73260-127">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="73260-127">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="73260-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="73260-128">**RestoreProperties**</span></span>                                               | <span data-ttu-id="73260-129">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73260-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73260-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="73260-130">**SaveProperties**</span></span>                                                  | <span data-ttu-id="73260-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73260-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="73260-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="73260-132">**SetPowerState**</span></span>                                                   | <span data-ttu-id="73260-133">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73260-133">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="73260-134">Propriétés</span><span class="sxs-lookup"><span data-stu-id="73260-134">Properties</span></span>

<span data-ttu-id="73260-135">La classe **MSVM \_ IDEController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="73260-135">The **Msvm\_IDEController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73260-136">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="73260-136">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-137">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-137">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73260-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-139">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="73260-139">Any additional availability and status of the device.</span></span> <span data-ttu-id="73260-140">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73260-140">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73260-141">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="73260-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-142">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-144">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="73260-144">The primary availability and status of the device.</span></span> <span data-ttu-id="73260-145">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73260-145">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73260-146">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="73260-146">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-147">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-147">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73260-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-149">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="73260-149">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="73260-150">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="73260-150">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="73260-151">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="73260-151">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="73260-152">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="73260-152">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="73260-153">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73260-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73260-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="73260-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-157">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="73260-157">A short description of the object.</span></span> <span data-ttu-id="73260-158">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73260-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="73260-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="73260-159">Value</span></span>                                                                                         | <span data-ttu-id="73260-160">Signification</span><span class="sxs-lookup"><span data-stu-id="73260-160">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="73260-161"><dt>« Contrôleur IDE 0 »</dt></span><span class="sxs-lookup"><span data-stu-id="73260-161"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="73260-162">L’instance représente le contrôleur principal.</span><span class="sxs-lookup"><span data-stu-id="73260-162">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="73260-163"><dt>« Contrôleur IDE 1 »</dt></span><span class="sxs-lookup"><span data-stu-id="73260-163"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="73260-164">L’instance représente le contrôleur secondaire.</span><span class="sxs-lookup"><span data-stu-id="73260-164">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73260-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="73260-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-166">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-168">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="73260-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="73260-169">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="73260-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73260-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73260-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-174">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="73260-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="73260-175">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73260-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73260-176">**Description**</span><span class="sxs-lookup"><span data-stu-id="73260-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-179">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="73260-179">A description of the object.</span></span> <span data-ttu-id="73260-180">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73260-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="73260-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-184">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="73260-184">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="73260-185">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="73260-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73260-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-187">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="73260-187">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-190">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific-Data*».</span><span class="sxs-lookup"><span data-stu-id="73260-190">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="73260-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="73260-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-194">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="73260-194">A display name for the object.</span></span> <span data-ttu-id="73260-195">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73260-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="73260-196">Valeur</span><span class="sxs-lookup"><span data-stu-id="73260-196">Value</span></span>                                                                                         | <span data-ttu-id="73260-197">Signification</span><span class="sxs-lookup"><span data-stu-id="73260-197">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="73260-198"><dt>« Contrôleur IDE 0 »</dt></span><span class="sxs-lookup"><span data-stu-id="73260-198"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="73260-199">L’instance représente le contrôleur principal.</span><span class="sxs-lookup"><span data-stu-id="73260-199">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="73260-200"><dt>« Contrôleur IDE 1 »</dt></span><span class="sxs-lookup"><span data-stu-id="73260-200"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="73260-201">L’instance représente le contrôleur secondaire.</span><span class="sxs-lookup"><span data-stu-id="73260-201">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73260-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="73260-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-203">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-205">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="73260-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="73260-206">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73260-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73260-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="73260-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-210">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="73260-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="73260-211">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="73260-211">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="73260-212">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73260-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73260-213">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="73260-213">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-214">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="73260-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73260-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-216">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="73260-216">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="73260-217">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-218">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="73260-218">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-221">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="73260-221">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="73260-222">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-222">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-223">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="73260-223">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-224">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-226">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="73260-226">The current health of the element.</span></span> <span data-ttu-id="73260-227">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="73260-227">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="73260-228">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="73260-228">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="73260-229">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-230">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="73260-230">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-231">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="73260-231">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73260-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-233">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="73260-233">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="73260-234">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-235">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="73260-235">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-236">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73260-236">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73260-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-238">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="73260-238">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="73260-239">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-240">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="73260-240">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73260-243">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="73260-243">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="73260-244">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="73260-244">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="73260-245">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="73260-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-246">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="73260-246">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-247">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73260-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73260-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-249">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="73260-249">The last error code reported by the logical device.</span></span> <span data-ttu-id="73260-250">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-251">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="73260-251">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-252">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73260-252">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73260-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-254">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="73260-254">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="73260-255">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="73260-255">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="73260-256">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="73260-256">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="73260-257">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="73260-257">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="73260-258">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="73260-258">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-259">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73260-259">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73260-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-261">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="73260-261">This property has been deprecated.</span></span> <span data-ttu-id="73260-262">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-262">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-263">**Nom**</span><span class="sxs-lookup"><span data-stu-id="73260-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-266">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="73260-266">The label by which the object is known.</span></span> <span data-ttu-id="73260-267">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="73260-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="73260-268">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="73260-268">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-269">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-271">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="73260-271">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="73260-272">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="73260-272">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73260-273">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-274">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="73260-274">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-275">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-275">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73260-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-277">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="73260-277">The current statuses of the object.</span></span> <span data-ttu-id="73260-278">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-278">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-279">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="73260-279">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-282">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="73260-282">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="73260-283">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="73260-283">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="73260-284">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73260-284">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73260-285">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="73260-285">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-286">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="73260-286">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73260-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-288">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="73260-288">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="73260-289">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="73260-289">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73260-290">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="73260-290">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-291">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-291">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73260-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-293">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="73260-293">The power management capabilities of the device.</span></span> <span data-ttu-id="73260-294">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-294">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-295">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="73260-295">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-296">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="73260-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73260-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-298">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="73260-298">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="73260-299">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-299">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-300">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="73260-300">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-301">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73260-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73260-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-303">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="73260-303">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="73260-304">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-305">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="73260-305">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-306">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-308">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="73260-308">Provides high level status information.</span></span> <span data-ttu-id="73260-309">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="73260-309">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="73260-310">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="73260-310">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="73260-311">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-312">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="73260-312">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-315">Chaîne qui fournit des informations supplémentaires relatives au protocole pris en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="73260-315">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="73260-316">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="73260-316">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="73260-317">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="73260-317">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-318">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-318">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-320">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="73260-320">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="73260-321">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="73260-321">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="73260-322">Valeur</span><span class="sxs-lookup"><span data-stu-id="73260-322">Value</span></span>                                                                         | <span data-ttu-id="73260-323">Signification</span><span class="sxs-lookup"><span data-stu-id="73260-323">Meaning</span></span>        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <span data-ttu-id="73260-324"><dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="73260-324"><dt>37</dt></span></span> </dl> | <span data-ttu-id="73260-325">IDE</span><span class="sxs-lookup"><span data-stu-id="73260-325">IDE</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73260-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="73260-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-327">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-329">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="73260-329">The last requested or desired state for the element.</span></span> <span data-ttu-id="73260-330">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="73260-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="73260-331">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="73260-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="73260-332">Une instance particulière d’un élément logique activé ne prend peut-être pas en charge **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="73260-332">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="73260-333">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-333">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="73260-334">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73260-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73260-335">**État**</span><span class="sxs-lookup"><span data-stu-id="73260-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-338">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="73260-338">The current status of the object.</span></span> <span data-ttu-id="73260-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-340">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="73260-340">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-341">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="73260-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="73260-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-343">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="73260-343">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="73260-344">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="73260-344">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="73260-345">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="73260-345">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-346">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-348">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="73260-348">The current state of the logical device.</span></span> <span data-ttu-id="73260-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-350">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73260-350">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-351">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-353">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="73260-353">The scoping system's creation class name.</span></span> <span data-ttu-id="73260-354">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73260-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73260-355">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="73260-355">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-356">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="73260-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73260-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-358">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="73260-358">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="73260-359">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="73260-359">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="73260-360">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="73260-360">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-361">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73260-361">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73260-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-363">La dernière fois que la machine virtuelle a été mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="73260-363">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="73260-364">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="73260-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="73260-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="73260-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-366">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73260-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73260-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-368">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="73260-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="73260-369">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73260-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="73260-370">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="73260-370">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-371">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73260-371">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73260-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-373">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="73260-373">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="73260-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-374">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="73260-375">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="73260-375">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73260-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73260-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73260-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="73260-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73260-378">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="73260-378">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="73260-379">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="73260-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73260-380">Notes</span><span class="sxs-lookup"><span data-stu-id="73260-380">Remarks</span></span>

<span data-ttu-id="73260-381">L’accès à la classe **MSVM \_ IDEController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="73260-381">Access to the **Msvm\_IDEController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="73260-382">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="73260-382">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="73260-383">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73260-383">Requirements</span></span>



| <span data-ttu-id="73260-384">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73260-384">Requirement</span></span> | <span data-ttu-id="73260-385">Valeur</span><span class="sxs-lookup"><span data-stu-id="73260-385">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73260-386">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73260-386">Minimum supported client</span></span><br/> | <span data-ttu-id="73260-387">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73260-387">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="73260-388">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73260-388">Minimum supported server</span></span><br/> | <span data-ttu-id="73260-389">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73260-389">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73260-390">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="73260-390">Namespace</span></span><br/>                | <span data-ttu-id="73260-391">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="73260-391">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="73260-392">MOF</span><span class="sxs-lookup"><span data-stu-id="73260-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73260-393"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73260-393"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73260-394">DLL</span><span class="sxs-lookup"><span data-stu-id="73260-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73260-395"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73260-395"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="73260-396">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73260-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73260-397">**\_IDECONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="73260-397">**CIM\_IDEController**</span></span>](cim-idecontroller.md)
</dt> <dt>

<span data-ttu-id="73260-398">[**\_IDECONTROLLER CIM**](/previous-versions//cc136863(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73260-398">[**CIM\_IDEController**](/previous-versions//cc136863(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="73260-399">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="73260-399">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

