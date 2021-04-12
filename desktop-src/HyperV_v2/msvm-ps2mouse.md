---
description: Représente un périphérique de souris PS2.
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d25d168b85a79c5212afc719ce6ec83ca9780395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319286"
---
# <a name="msvm_ps2mouse-class"></a><span data-ttu-id="2d0e0-103">MSVM \_ Ps2Mouse, classe</span><span class="sxs-lookup"><span data-stu-id="2d0e0-103">Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="2d0e0-104">Représente un périphérique de souris PS2.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-104">Represents a PS2 mouse device.</span></span> <span data-ttu-id="2d0e0-105">Les instances de cette classe sont des périphériques logiques qui sont toujours présents dans un ordinateur virtuel, et ne sont donc pas alloués par le biais d’un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-105">Instances of this class are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="2d0e0-106">Une instance est toujours présente dans une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-106">One instance is always present in a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="2d0e0-107">Cette classe n’est pas disponible pour les ordinateurs virtuels de génération 2.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="2d0e0-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0e0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d0e0-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_PS2Mouse";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a><span data-ttu-id="2d0e0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2d0e0-110">Members</span></span>

<span data-ttu-id="2d0e0-111">La classe **MSVM \_ Ps2Mouse** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2d0e0-111">The **Msvm\_Ps2Mouse** class has these types of members:</span></span>

-   [<span data-ttu-id="2d0e0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d0e0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d0e0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d0e0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d0e0-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d0e0-114">Methods</span></span>

<span data-ttu-id="2d0e0-115">La classe **MSVM \_ Ps2Mouse** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-115">The **Msvm\_Ps2Mouse** class has these methods.</span></span>



| <span data-ttu-id="2d0e0-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="2d0e0-116">Method</span></span>                                                           | <span data-ttu-id="2d0e0-117">Description</span><span class="sxs-lookup"><span data-stu-id="2d0e0-117">Description</span></span>                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d0e0-118">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-118">**ClickButton**</span></span>](clickbutton-msvm-ps2mouse.md)                 | <span data-ttu-id="2d0e0-119">Simule un clic sur un bouton, une séquence de rebours, sur le bouton du périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-119">Simulates a button click, a down-up sequence, on the specified device button.</span></span><br/>              |
| <span data-ttu-id="2d0e0-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-120">**EnableDevice**</span></span>                                                 | <span data-ttu-id="2d0e0-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-121">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="2d0e0-122">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-122">**GetButtonState**</span></span>](getbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="2d0e0-123">Récupère l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-123">Retrieves the current state of the specified device button.</span></span><br/>                                |
| <span data-ttu-id="2d0e0-124">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-124">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="2d0e0-125">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-125">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="2d0e0-126">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-126">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="2d0e0-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-127">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="2d0e0-128">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-128">**RequestStateChange**</span></span>](msvm-ps2mouse-requeststatechange.md)   | <span data-ttu-id="2d0e0-129">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-129">Requests a state change.</span></span><br/>                                                                   |
| [<span data-ttu-id="2d0e0-130">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-130">**Reset**</span></span>](msvm-ps2mouse-reset.md)                             | <span data-ttu-id="2d0e0-131">Réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-131">Resets the device.</span></span><br/>                                                                         |
| <span data-ttu-id="2d0e0-132">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-132">**RestoreProperties**</span></span>                                            | <span data-ttu-id="2d0e0-133">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-133">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="2d0e0-134">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-134">**SaveProperties**</span></span>                                               | <span data-ttu-id="2d0e0-135">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-135">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="2d0e0-136">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-136">**SetButtonState**</span></span>](setbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="2d0e0-137">Définit l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-137">Sets the current state of the specified device button.</span></span><br/>                                     |
| <span data-ttu-id="2d0e0-138">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-138">**SetPowerState**</span></span>                                                | <span data-ttu-id="2d0e0-139">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-139">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="2d0e0-140">**SetRelativePosition**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-140">**SetRelativePosition**</span></span>](setrelativeposition-msvm-ps2mouse.md) | <span data-ttu-id="2d0e0-141">Décale la position du pointeur de la souris selon les deltas horizontaux et verticaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-141">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span><br/> |
| [<span data-ttu-id="2d0e0-142">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-142">**SetScrollPosition**</span></span>](setscrollposition-msvm-ps2mouse.md)     | <span data-ttu-id="2d0e0-143">Ajuste la coordonnée z du contrôle de roulette du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-143">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="2d0e0-144">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d0e0-144">Properties</span></span>

<span data-ttu-id="2d0e0-145">La classe **MSVM \_ Ps2Mouse** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-145">The **Msvm\_Ps2Mouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d0e0-146">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-146">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-147">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-149">Indique si l’appareil fonctionne sur des coordonnées absolues.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-149">Indicates whether the device operates on absolute coordinates.</span></span> <span data-ttu-id="2d0e0-150">Si la valeur n’est pas définie, les coordonnées de l’appareil sont relatives.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-150">If not set, the device's coordinates are relative.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-152">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-154">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="2d0e0-154">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="2d0e0-155">La propriété de **disponibilité** indique l’état principal et la disponibilité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-155">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="2d0e0-156">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-156">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="2d0e0-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d0e0-157">Value</span></span>                                                                        | <span data-ttu-id="2d0e0-158">Signification</span><span class="sxs-lookup"><span data-stu-id="2d0e0-158">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2d0e0-159"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-159"><dt>6</dt></span></span> </dl> | <span data-ttu-id="2d0e0-160">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2d0e0-160">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2d0e0-161">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-161">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-162">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-164">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-164">The primary availability and status of the device.</span></span> <span data-ttu-id="2d0e0-165">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-165">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="2d0e0-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d0e0-166">Value</span></span>                                                                        | <span data-ttu-id="2d0e0-167">Signification</span><span class="sxs-lookup"><span data-stu-id="2d0e0-167">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2d0e0-168"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-168"><dt>6</dt></span></span> </dl> | <span data-ttu-id="2d0e0-169">Non applicable</span><span class="sxs-lookup"><span data-stu-id="2d0e0-169">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2d0e0-170">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-170">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-171">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-171">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-173">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2d0e0-173">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="2d0e0-174">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-174">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-178">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-178">A short description of the object.</span></span> <span data-ttu-id="2d0e0-179">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-179">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-180">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-180">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-181">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-183">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-183">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2d0e0-184">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-184">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2d0e0-185">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2d0e0-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2d0e0-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2d0e0-193">)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-193">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d0e0-194">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-194">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-197">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-197">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-198">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-198">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2d0e0-199">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-199">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="2d0e0-200">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-201">**Description**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-204">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="2d0e0-204">A description of the object.</span></span> <span data-ttu-id="2d0e0-205">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-207">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-209">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-209">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2d0e0-210">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2d0e0-211">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2d0e0-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2d0e0-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2d0e0-220">)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-220">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d0e0-221">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-221">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-224">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-224">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-225">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-225">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="2d0e0-226">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID*».</span><span class="sxs-lookup"><span data-stu-id="2d0e0-226">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-227">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-227">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-230">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-230">A display name for the object.</span></span> <span data-ttu-id="2d0e0-231">Cette propriété permet à chaque instance de définir un nom complet en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-231">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="2d0e0-232">La propriété [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la **classe \_ ManagedSystemElement CIM** est également définie en tant que nom complet.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-232">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="2d0e0-233">Toutefois, il est souvent sous-classé comme une clé.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-233">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="2d0e0-234">Il n’est pas raisonnable que la même propriété puisse transmettre à la fois l’identité et un nom d’affichage, sans incohérence.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-234">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="2d0e0-235">Où le [**nom**](msvm-keyboard.md) existe et n’est pas une clé (par exemple, pour les instances de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), les mêmes informations peuvent être présentes dans les propriétés **Name** et **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="2d0e0-235">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="2d0e0-236">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Mouse ».</span><span class="sxs-lookup"><span data-stu-id="2d0e0-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Mouse".</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-238">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-240">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-240">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="2d0e0-241">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-243">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-245">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2d0e0-246">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-246">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-247">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-247">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-248">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-250">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-250">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="2d0e0-251">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-252">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-252">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-255">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-255">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="2d0e0-256">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-257">**Ergonomie**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-257">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-258">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-260">Configuration du dispositif de pointage pour l’opération de droite ou de gauche.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-260">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="2d0e0-261">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-261">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="2d0e0-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d0e0-262">Value</span></span>                                                                        | <span data-ttu-id="2d0e0-263">Signification</span><span class="sxs-lookup"><span data-stu-id="2d0e0-263">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="2d0e0-264"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-264"><dt>0</dt></span></span> </dl> | <span data-ttu-id="2d0e0-265">Unknown</span><span class="sxs-lookup"><span data-stu-id="2d0e0-265">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="2d0e0-266"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-266"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2d0e0-267">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-267">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="2d0e0-268"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-268"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2d0e0-269">Bon fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-269">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="2d0e0-270"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-270"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2d0e0-271">Opération gauche de la main.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-271">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="2d0e0-272">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-272">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-273">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-275">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-275">The current health of the element.</span></span> <span data-ttu-id="2d0e0-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK)</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-277">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-277">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-278">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-278">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-280">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0e0-280">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="2d0e0-281">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-283">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-285">Date et heure de création de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-285">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="2d0e0-286">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-287">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-287">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-290">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-290">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-291">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-291">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2d0e0-292">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-292">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-293">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-293">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-294">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-296">Indique si l’appareil est verrouillé, empêchant l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-296">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="2d0e0-297">Cette propriété est héritée de la [**\_ UserDevice CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-297">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-298">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-298">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-299">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-301">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-301">The last error code reported by the logical device.</span></span> <span data-ttu-id="2d0e0-302">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-303">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-303">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-304">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-306">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-306">This property has been deprecated.</span></span> <span data-ttu-id="2d0e0-307">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-308">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-311">Qualificateurs : **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-311">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-312">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-312">The label by which the object is known.</span></span> <span data-ttu-id="2d0e0-313">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-313">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="2d0e0-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-315">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-315">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-316">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-316">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-318">Nombre de boutons sur le dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-318">The number of buttons on the pointing device.</span></span> <span data-ttu-id="2d0e0-319">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-319">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-321">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-323">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2d0e0-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2d0e0-324">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2d0e0-325">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2d0e0-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2d0e0-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2d0e0-345">)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-345">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d0e0-346">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-346">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-347">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-349">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-349">The current status of the element.</span></span> <span data-ttu-id="2d0e0-350">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-350">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-351">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-351">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-354">État activé ou désactivé de l’élément lorsque la propriété [**EnabledState**](msvm-keyboard.md) a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-354">The enabled or disabled state of the element when the [**EnabledState**](msvm-keyboard.md) property is set to 1 (Other).</span></span> <span data-ttu-id="2d0e0-355">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-355">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2d0e0-356">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-356">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-357">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-357">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-358">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-360">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-360">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2d0e0-361">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-362">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-362">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-363">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-363">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-365">Type du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-365">The type of the pointing device.</span></span> <span data-ttu-id="2d0e0-366">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-366">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="2d0e0-367">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d0e0-367">Value</span></span>                                                                        | <span data-ttu-id="2d0e0-368">Signification</span><span class="sxs-lookup"><span data-stu-id="2d0e0-368">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="2d0e0-369"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-369"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2d0e0-370">Souris</span><span class="sxs-lookup"><span data-stu-id="2d0e0-370">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2d0e0-371">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-371">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-372">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-372">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-374">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-374">The power management capabilities of the device.</span></span> <span data-ttu-id="2d0e0-375">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-376">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-376">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-377">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-379">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-379">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2d0e0-380">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-381">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-381">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-382">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-384">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-384">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2d0e0-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-386">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-386">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-387">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-389">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-389">Provides high level status information.</span></span> <span data-ttu-id="2d0e0-390">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-390">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2d0e0-391">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2d0e0-392">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2d0e0-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2d0e0-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2d0e0-399">)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-399">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d0e0-400">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-400">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-401">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-403">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-403">The last requested or desired state for the element.</span></span> <span data-ttu-id="2d0e0-404">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2d0e0-405">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d0e0-405">Value</span></span>                                                                         | <span data-ttu-id="2d0e0-406">Signification</span><span class="sxs-lookup"><span data-stu-id="2d0e0-406">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2d0e0-407"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-407"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2d0e0-408">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-408">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2d0e0-409">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-409">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-410">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-412">Résolution de suivi du dispositif de pointage, en nombre par pouce.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-412">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="2d0e0-413">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-413">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-414">**État**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-414">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-417">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-417">The current status of the object.</span></span> <span data-ttu-id="2d0e0-418">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-420">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-422">Chaînes qui décrivent les différentes valeurs de tableau [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0e0-422">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="2d0e0-423">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="2d0e0-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-424">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-424">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-425">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-425">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-427">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-427">The current state of the logical device.</span></span> <span data-ttu-id="2d0e0-428">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-429">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-429">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-432">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-432">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-433">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-433">The scoping system's creation class name.</span></span> <span data-ttu-id="2d0e0-434">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-435">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-435">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-438">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="2d0e0-438">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-439">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-439">The scoping system's name.</span></span> <span data-ttu-id="2d0e0-440">Cette valeur correspond à la valeur de la propriété [**Name**](msvm-computersystem.md) de la classe **MSVM \_ ComputerSystem** pour l’ordinateur virtuel d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-440">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="2d0e0-441">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-442">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-442">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-443">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-445">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-445">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2d0e0-446">Si l’état de l’élément n’a pas été modifié et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-446">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="2d0e0-447">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-447">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="2d0e0-448">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-448">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-449">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-449">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-450">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-452">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-452">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2d0e0-453">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d0e0-454">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-454">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d0e0-455">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d0e0-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d0e0-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d0e0-457">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-457">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2d0e0-458">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d0e0-459">Notes</span><span class="sxs-lookup"><span data-stu-id="2d0e0-459">Remarks</span></span>

<span data-ttu-id="2d0e0-460">L’accès à la classe **MSVM \_ Ps2Mouse** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="2d0e0-460">Access to the **Msvm\_Ps2Mouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2d0e0-461">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2d0e0-461">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d0e0-462">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d0e0-462">Requirements</span></span>



| <span data-ttu-id="2d0e0-463">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d0e0-463">Requirement</span></span> | <span data-ttu-id="2d0e0-464">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d0e0-464">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d0e0-465">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d0e0-465">Minimum supported client</span></span><br/> | <span data-ttu-id="2d0e0-466">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d0e0-466">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2d0e0-467">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d0e0-467">Minimum supported server</span></span><br/> | <span data-ttu-id="2d0e0-468">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d0e0-468">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d0e0-469">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d0e0-469">Namespace</span></span><br/>                | <span data-ttu-id="2d0e0-470">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d0e0-470">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2d0e0-471">MOF</span><span class="sxs-lookup"><span data-stu-id="2d0e0-471">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d0e0-472"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-472"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d0e0-473">DLL</span><span class="sxs-lookup"><span data-stu-id="2d0e0-473">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d0e0-474"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d0e0-474"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d0e0-475">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d0e0-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d0e0-476">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-476">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="2d0e0-477">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2d0e0-477">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="2d0e0-478">Classes d’entrée</span><span class="sxs-lookup"><span data-stu-id="2d0e0-478">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

