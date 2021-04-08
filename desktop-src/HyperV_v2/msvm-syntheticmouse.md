---
description: Représente un périphérique de souris synthétique.
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c5be44637c91ebd57867c5062eba6f9e57ee543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750196"
---
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="8462c-103">MSVM \_ SyntheticMouse, classe</span><span class="sxs-lookup"><span data-stu-id="8462c-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="8462c-104">Représente un périphérique de souris synthétique.</span><span class="sxs-lookup"><span data-stu-id="8462c-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="8462c-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8462c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8462c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8462c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
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
  string   CreationClassName = "Msvm_SyntheticMouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a><span data-ttu-id="8462c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8462c-107">Members</span></span>

<span data-ttu-id="8462c-108">La classe **MSVM \_ SyntheticMouse** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8462c-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="8462c-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8462c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="8462c-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8462c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8462c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8462c-111">Methods</span></span>

<span data-ttu-id="8462c-112">La classe **MSVM \_ SyntheticMouse** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8462c-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="8462c-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="8462c-113">Method</span></span>                                                                 | <span data-ttu-id="8462c-114">Description</span><span class="sxs-lookup"><span data-stu-id="8462c-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="8462c-115">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="8462c-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="8462c-116">Simule un clic sur le bouton du périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="8462c-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="8462c-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="8462c-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="8462c-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8462c-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="8462c-119">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="8462c-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="8462c-120">Récupère l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="8462c-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="8462c-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="8462c-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="8462c-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8462c-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="8462c-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="8462c-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="8462c-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8462c-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="8462c-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8462c-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="8462c-126">Demande un changement d’État</span><span class="sxs-lookup"><span data-stu-id="8462c-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="8462c-127">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="8462c-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="8462c-128">Réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8462c-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="8462c-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="8462c-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="8462c-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8462c-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="8462c-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="8462c-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="8462c-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8462c-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="8462c-133">**SetAbsolutePosition**</span><span class="sxs-lookup"><span data-stu-id="8462c-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="8462c-134">Définit la position horizontale et verticale du curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="8462c-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="8462c-135">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="8462c-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="8462c-136">Définit l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="8462c-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="8462c-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8462c-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="8462c-138">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8462c-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="8462c-139">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="8462c-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="8462c-140">Définit la coordonnée z du contrôle de roulette du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="8462c-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8462c-141">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8462c-141">Properties</span></span>

<span data-ttu-id="8462c-142">La classe **MSVM \_ SyntheticMouse** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8462c-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8462c-143">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="8462c-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-144">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8462c-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-146">Indique si l’appareil fonctionne sur des coordonnées absolues ou relatives.</span><span class="sxs-lookup"><span data-stu-id="8462c-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="8462c-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-147">Value</span></span>                                                                                | <span data-ttu-id="8462c-148">Signification</span><span class="sxs-lookup"><span data-stu-id="8462c-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="8462c-149"><dt>**Vrai**</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="8462c-150">Les coordonnées de l’appareil sont absolues.</span><span class="sxs-lookup"><span data-stu-id="8462c-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="8462c-151"><dt>**Faux**</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="8462c-152">Les coordonnées de l’appareil sont relatives.</span><span class="sxs-lookup"><span data-stu-id="8462c-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8462c-153">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="8462c-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-154">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8462c-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-156">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="8462c-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="8462c-157">La propriété de **disponibilité** indique l’état principal et la disponibilité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8462c-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="8462c-158">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="8462c-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-159">Value</span></span>                                                                          | <span data-ttu-id="8462c-160">Signification</span><span class="sxs-lookup"><span data-stu-id="8462c-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="8462c-161">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8462c-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8462c-162">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="8462c-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-165">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8462c-165">The primary availability and status of the device.</span></span> <span data-ttu-id="8462c-166">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="8462c-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-167">Value</span></span>                                                                        | <span data-ttu-id="8462c-168">Signification</span><span class="sxs-lookup"><span data-stu-id="8462c-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8462c-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="8462c-170">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8462c-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8462c-171">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8462c-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-172">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8462c-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-174">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8462c-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8462c-175">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="8462c-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8462c-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-179">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8462c-179">A short description of the object.</span></span> <span data-ttu-id="8462c-180">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-181">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8462c-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-184">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="8462c-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8462c-185">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8462c-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8462c-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8462c-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8462c-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8462c-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="8462c-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="8462c-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="8462c-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8462c-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8462c-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8462c-194">)</span><span class="sxs-lookup"><span data-stu-id="8462c-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8462c-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8462c-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8462c-198">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8462c-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8462c-199">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="8462c-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8462c-200">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="8462c-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="8462c-201">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-202">**Description**</span><span class="sxs-lookup"><span data-stu-id="8462c-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-205">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="8462c-205">A description of the object.</span></span> <span data-ttu-id="8462c-206">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8462c-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-210">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8462c-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8462c-211">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8462c-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8462c-212">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8462c-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="8462c-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="8462c-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="8462c-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="8462c-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="8462c-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="8462c-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8462c-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8462c-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8462c-221">)</span><span class="sxs-lookup"><span data-stu-id="8462c-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8462c-222">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8462c-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8462c-225">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="8462c-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8462c-226">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8462c-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="8462c-227">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID*».</span><span class="sxs-lookup"><span data-stu-id="8462c-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="8462c-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8462c-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-231">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8462c-231">A display name for the object.</span></span> <span data-ttu-id="8462c-232">Cette propriété permet à chaque instance de définir un nom complet en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="8462c-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="8462c-233">La propriété [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la **classe \_ ManagedSystemElement CIM** est également définie en tant que nom complet.</span><span class="sxs-lookup"><span data-stu-id="8462c-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="8462c-234">Toutefois, il est souvent sous-classé comme une clé.</span><span class="sxs-lookup"><span data-stu-id="8462c-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="8462c-235">Il n’est pas raisonnable que la même propriété puisse transmettre à la fois l’identité et un nom d’affichage, sans incohérence.</span><span class="sxs-lookup"><span data-stu-id="8462c-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="8462c-236">Où le [**nom**](msvm-keyboard.md) existe et n’est pas une clé (par exemple, pour les instances de LogicalDevice), les mêmes informations peuvent être présentes dans les propriétés **Name** et **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="8462c-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="8462c-237">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8462c-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-239">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-241">Configuration par défaut ou de démarrage d’un administrateur pour **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8462c-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="8462c-242">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8462c-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8462c-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-244">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-246">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8462c-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8462c-247">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8462c-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8462c-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="8462c-249">Signification</span><span class="sxs-lookup"><span data-stu-id="8462c-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="8462c-250"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="8462c-251">La machine virtuelle invitée prend en charge une souris synthétique.</span><span class="sxs-lookup"><span data-stu-id="8462c-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="8462c-252"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="8462c-253">L’ordinateur virtuel invité ne prend pas en charge de souris synthétique.</span><span class="sxs-lookup"><span data-stu-id="8462c-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8462c-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8462c-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-255">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8462c-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-257">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="8462c-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="8462c-258">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8462c-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-262">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="8462c-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="8462c-263">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-264">**Ergonomie**</span><span class="sxs-lookup"><span data-stu-id="8462c-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-265">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-267">Configuration du dispositif de pointage pour l’opération de droite ou de gauche.</span><span class="sxs-lookup"><span data-stu-id="8462c-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="8462c-268">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="8462c-269">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-269">Value</span></span>                                                                        | <span data-ttu-id="8462c-270">Signification</span><span class="sxs-lookup"><span data-stu-id="8462c-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="8462c-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="8462c-272">Unknown</span><span class="sxs-lookup"><span data-stu-id="8462c-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="8462c-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="8462c-274">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="8462c-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="8462c-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="8462c-276">Bon fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="8462c-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="8462c-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8462c-278">Opération gauche de la main.</span><span class="sxs-lookup"><span data-stu-id="8462c-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="8462c-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8462c-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-280">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-282">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8462c-282">The current health of the element.</span></span> <span data-ttu-id="8462c-283">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-284">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="8462c-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-285">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8462c-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-287">Coordonnée x absolue du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="8462c-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8462c-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-289">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8462c-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8462c-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-291">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="8462c-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="8462c-292">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8462c-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-294">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8462c-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-296">Date et heure de création de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8462c-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="8462c-297">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8462c-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8462c-301">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="8462c-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8462c-302">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="8462c-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8462c-303">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="8462c-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-305">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8462c-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-307">Indique si l’appareil est verrouillé, empêchant l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8462c-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="8462c-308">Cette propriété est héritée de la [**\_ UserDevice CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8462c-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-310">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8462c-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-312">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8462c-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="8462c-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-314">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="8462c-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-315">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8462c-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-317">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="8462c-317">This property has been deprecated.</span></span> <span data-ttu-id="8462c-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-319">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8462c-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8462c-322">Qualificateurs : **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="8462c-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8462c-323">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="8462c-323">The label by which the object is known.</span></span> <span data-ttu-id="8462c-324">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="8462c-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="8462c-325">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-326">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="8462c-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-327">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="8462c-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-329">Nombre de boutons sur le dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="8462c-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="8462c-330">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-331">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8462c-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-332">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-334">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8462c-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8462c-335">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8462c-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8462c-336">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8462c-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8462c-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8462c-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="8462c-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="8462c-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="8462c-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="8462c-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="8462c-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="8462c-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="8462c-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="8462c-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="8462c-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="8462c-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="8462c-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="8462c-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="8462c-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="8462c-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="8462c-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8462c-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8462c-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8462c-356">)</span><span class="sxs-lookup"><span data-stu-id="8462c-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8462c-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8462c-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-358">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8462c-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-360">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8462c-360">The current status of the element.</span></span> <span data-ttu-id="8462c-361">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8462c-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-363">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-365">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="8462c-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8462c-366">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="8462c-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8462c-367">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8462c-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8462c-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-369">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8462c-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8462c-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-371">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="8462c-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="8462c-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-373">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="8462c-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-374">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-376">Type du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="8462c-376">The type of pointing device.</span></span> <span data-ttu-id="8462c-377">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="8462c-378">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-378">Value</span></span>                                                                        | <span data-ttu-id="8462c-379">Signification</span><span class="sxs-lookup"><span data-stu-id="8462c-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="8462c-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8462c-381">Souris</span><span class="sxs-lookup"><span data-stu-id="8462c-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8462c-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8462c-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-383">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8462c-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-385">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8462c-385">The power management capabilities of the device.</span></span> <span data-ttu-id="8462c-386">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8462c-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-388">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8462c-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-390">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="8462c-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="8462c-391">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8462c-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-393">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8462c-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-395">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="8462c-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="8462c-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8462c-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-398">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-400">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="8462c-400">Provides high level status information.</span></span> <span data-ttu-id="8462c-401">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="8462c-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8462c-402">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8462c-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8462c-403">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8462c-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8462c-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="8462c-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="8462c-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="8462c-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8462c-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8462c-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8462c-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8462c-410">)</span><span class="sxs-lookup"><span data-stu-id="8462c-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8462c-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8462c-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-412">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-414">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="8462c-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="8462c-415">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8462c-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8462c-416">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-416">Value</span></span>                                                                         | <span data-ttu-id="8462c-417">Signification</span><span class="sxs-lookup"><span data-stu-id="8462c-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8462c-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="8462c-419">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8462c-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8462c-420">**Résolution :**</span><span class="sxs-lookup"><span data-stu-id="8462c-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-421">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8462c-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-423">Résolution de suivi du dispositif de pointage, en nombre par pouce.</span><span class="sxs-lookup"><span data-stu-id="8462c-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="8462c-424">Cette propriété est héritée de la [**\_ PointingDevice CIM**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-425">**ScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="8462c-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-426">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8462c-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-427">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8462c-428">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="8462c-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="8462c-429">Position de la coordonnée z du périphérique de la souris.</span><span class="sxs-lookup"><span data-stu-id="8462c-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-430">**État**</span><span class="sxs-lookup"><span data-stu-id="8462c-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-431">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-433">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8462c-433">The current status of the object.</span></span> <span data-ttu-id="8462c-434">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-435">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8462c-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-436">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8462c-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8462c-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-438">Chaînes qui décrivent les différentes valeurs de tableau [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="8462c-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="8462c-439">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8462c-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8462c-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-441">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-443">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8462c-443">The current state of the logical device.</span></span> <span data-ttu-id="8462c-444">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-445">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8462c-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-446">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8462c-448">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8462c-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8462c-449">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8462c-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="8462c-450">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-451">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8462c-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-452">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8462c-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8462c-454">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8462c-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8462c-455">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8462c-455">The name of the scoping system.</span></span> <span data-ttu-id="8462c-456">Cette valeur correspond à la valeur de la propriété [**Name**](msvm-computersystem.md) de la classe **MSVM \_ ComputerSystem** pour l’ordinateur virtuel d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8462c-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="8462c-457">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8462c-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8462c-458">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8462c-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-459">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8462c-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-461">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8462c-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8462c-462">Si l’état de l’élément n’a pas été modifié et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="8462c-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="8462c-463">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8462c-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="8462c-464">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="8462c-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8462c-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-466">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8462c-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-468">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="8462c-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="8462c-469">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8462c-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-470">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8462c-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-471">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8462c-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-473">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="8462c-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8462c-474">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="8462c-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8462c-475">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="8462c-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8462c-476">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8462c-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8462c-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8462c-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8462c-478">Coordonnée y absolue du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="8462c-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8462c-479">Notes</span><span class="sxs-lookup"><span data-stu-id="8462c-479">Remarks</span></span>

<span data-ttu-id="8462c-480">L’accès à la classe **MSVM \_ SyntheticMouse** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="8462c-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8462c-481">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8462c-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8462c-482">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8462c-482">Requirements</span></span>



| <span data-ttu-id="8462c-483">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8462c-483">Requirement</span></span> | <span data-ttu-id="8462c-484">Valeur</span><span class="sxs-lookup"><span data-stu-id="8462c-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8462c-485">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8462c-485">Minimum supported client</span></span><br/> | <span data-ttu-id="8462c-486">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8462c-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8462c-487">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8462c-487">Minimum supported server</span></span><br/> | <span data-ttu-id="8462c-488">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8462c-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8462c-489">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8462c-489">Namespace</span></span><br/>                | <span data-ttu-id="8462c-490">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8462c-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8462c-491">MOF</span><span class="sxs-lookup"><span data-stu-id="8462c-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8462c-492"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8462c-493">DLL</span><span class="sxs-lookup"><span data-stu-id="8462c-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8462c-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8462c-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8462c-495">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8462c-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8462c-496">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8462c-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="8462c-497">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8462c-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="8462c-498">Classes d’entrée</span><span class="sxs-lookup"><span data-stu-id="8462c-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

