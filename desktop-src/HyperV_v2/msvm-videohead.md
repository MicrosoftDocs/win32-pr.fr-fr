---
description: Décrit la surface de dessin principale sur un contrôleur d’affichage.
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Msvm_VideoHead, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114203"
---
# <a name="msvm_videohead-class"></a><span data-ttu-id="603cd-103">MSVM \_ VideoHead, classe</span><span class="sxs-lookup"><span data-stu-id="603cd-103">Msvm\_VideoHead class</span></span>

<span data-ttu-id="603cd-104">Décrit la surface de dessin principale sur un contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="603cd-104">Describes the primary drawing surface on a display controller.</span></span>

<span data-ttu-id="603cd-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="603cd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="603cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="603cd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="603cd-107">Membres</span><span class="sxs-lookup"><span data-stu-id="603cd-107">Members</span></span>

<span data-ttu-id="603cd-108">La classe **MSVM \_ VideoHead** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="603cd-108">The **Msvm\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="603cd-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="603cd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="603cd-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="603cd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="603cd-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="603cd-111">Methods</span></span>

<span data-ttu-id="603cd-112">La classe **MSVM \_ VideoHead** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="603cd-112">The **Msvm\_VideoHead** class has these methods.</span></span>



| <span data-ttu-id="603cd-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="603cd-113">Method</span></span>                                                          | <span data-ttu-id="603cd-114">Description</span><span class="sxs-lookup"><span data-stu-id="603cd-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="603cd-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="603cd-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="603cd-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="603cd-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="603cd-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="603cd-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="603cd-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="603cd-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="603cd-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="603cd-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="603cd-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="603cd-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="603cd-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="603cd-121">**RequestStateChange**</span></span>](msvm-videohead-requeststatechange.md) | <span data-ttu-id="603cd-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="603cd-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="603cd-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="603cd-123">**Reset**</span></span>](msvm-videohead-reset.md)                           | <span data-ttu-id="603cd-124">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="603cd-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="603cd-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="603cd-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="603cd-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="603cd-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="603cd-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="603cd-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="603cd-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="603cd-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="603cd-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="603cd-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="603cd-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="603cd-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="603cd-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="603cd-131">Properties</span></span>

<span data-ttu-id="603cd-132">La classe **MSVM \_ VideoHead** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="603cd-132">The **Msvm\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="603cd-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="603cd-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="603cd-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-136">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="603cd-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="603cd-137">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="603cd-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="603cd-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-141">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="603cd-141">The primary availability and status of the device.</span></span> <span data-ttu-id="603cd-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="603cd-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="603cd-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="603cd-143">Value</span></span>                                                                        | <span data-ttu-id="603cd-144">Signification</span><span class="sxs-lookup"><span data-stu-id="603cd-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="603cd-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="603cd-146">Non applicable</span><span class="sxs-lookup"><span data-stu-id="603cd-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="603cd-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="603cd-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="603cd-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-150">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="603cd-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="603cd-151">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="603cd-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="603cd-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-155">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="603cd-155">A short description of the object.</span></span> <span data-ttu-id="603cd-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="603cd-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-158">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-160">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="603cd-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="603cd-161">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="603cd-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="603cd-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="603cd-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="603cd-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="603cd-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="603cd-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="603cd-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="603cd-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="603cd-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="603cd-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="603cd-170">)</span><span class="sxs-lookup"><span data-stu-id="603cd-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="603cd-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="603cd-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-174">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="603cd-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="603cd-175">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="603cd-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-176">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="603cd-176">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603cd-179">Qualificateurs : **unités** (« bits »)</span><span class="sxs-lookup"><span data-stu-id="603cd-179">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="603cd-180">Nombre de bits utilisés pour afficher chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="603cd-180">The number of bits used to display each pixel.</span></span> <span data-ttu-id="603cd-181">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-181">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-182">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="603cd-182">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-183">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603cd-185">Qualificateurs : **unités** (« pixels »)</span><span class="sxs-lookup"><span data-stu-id="603cd-185">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="603cd-186">Nombre actuel de pixels horizontaux.</span><span class="sxs-lookup"><span data-stu-id="603cd-186">The current number of horizontal pixels.</span></span> <span data-ttu-id="603cd-187">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-187">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-188">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="603cd-188">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-189">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="603cd-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-191">Nombre de couleurs prises en charge au niveau des résolutions actuelles.</span><span class="sxs-lookup"><span data-stu-id="603cd-191">The number of colors supported at the current resolutions.</span></span> <span data-ttu-id="603cd-192">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-192">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-193">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="603cd-193">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-194">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-196">En mode caractère, le nombre de colonnes pour ce contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="603cd-196">If in character mode, the number of columns for this display controller.</span></span> <span data-ttu-id="603cd-197">Sinon, il prend la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="603cd-197">Otherwise, 0.</span></span> <span data-ttu-id="603cd-198">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-198">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-199">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="603cd-199">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-200">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-202">En mode caractère, il s’agit du nombre de lignes pour ce contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="603cd-202">If in character mode, the number of rows for this video controller.</span></span> <span data-ttu-id="603cd-203">Sinon, il prend la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="603cd-203">Otherwise, 0.</span></span> <span data-ttu-id="603cd-204">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-204">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-205">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="603cd-205">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-206">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603cd-208">Qualificateurs : **unités** (« Hertz »)</span><span class="sxs-lookup"><span data-stu-id="603cd-208">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="603cd-209">Fréquence d’actualisation actuelle, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="603cd-209">The current refresh rate, in hertz.</span></span> <span data-ttu-id="603cd-210">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-210">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-211">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="603cd-211">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-214">Mode d’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="603cd-214">The current scan mode.</span></span> <span data-ttu-id="603cd-215">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-215">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="603cd-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="603cd-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="603cd-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (2)</span><span class="sxs-lookup"><span data-stu-id="603cd-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Opération non entrelacée** (3)</span><span class="sxs-lookup"><span data-stu-id="603cd-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (3)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Opération entrelacée** (4)</span><span class="sxs-lookup"><span data-stu-id="603cd-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="603cd-221">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="603cd-221">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-222">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603cd-224">Qualificateurs : **unités** (« pixels »)</span><span class="sxs-lookup"><span data-stu-id="603cd-224">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="603cd-225">Nombre actuel de pixels verticaux.</span><span class="sxs-lookup"><span data-stu-id="603cd-225">The current number of vertical pixels.</span></span> <span data-ttu-id="603cd-226">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-226">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-227">**Description**</span><span class="sxs-lookup"><span data-stu-id="603cd-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-230">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="603cd-230">A description of the object.</span></span> <span data-ttu-id="603cd-231">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-232">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="603cd-232">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-233">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-235">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="603cd-235">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="603cd-236">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="603cd-236">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="603cd-237">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="603cd-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="603cd-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="603cd-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="603cd-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="603cd-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="603cd-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="603cd-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="603cd-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="603cd-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="603cd-246">)</span><span class="sxs-lookup"><span data-stu-id="603cd-246">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="603cd-247">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="603cd-247">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-250">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ Head \\ *index*».</span><span class="sxs-lookup"><span data-stu-id="603cd-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\Head\\*Index*".</span></span>

</dd> <dt>

<span data-ttu-id="603cd-251">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="603cd-251">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-254">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="603cd-254">A display name for the object.</span></span> <span data-ttu-id="603cd-255">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-256">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="603cd-256">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-259">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="603cd-259">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="603cd-260">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="603cd-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="603cd-261">Valeur</span><span class="sxs-lookup"><span data-stu-id="603cd-261">Value</span></span>                                                                        | <span data-ttu-id="603cd-262">Signification</span><span class="sxs-lookup"><span data-stu-id="603cd-262">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="603cd-263"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-263"><dt>2</dt></span></span> </dl> | <span data-ttu-id="603cd-264">activé</span><span class="sxs-lookup"><span data-stu-id="603cd-264">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="603cd-265"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-265"><dt>3</dt></span></span> </dl> | <span data-ttu-id="603cd-266">Désactivé</span><span class="sxs-lookup"><span data-stu-id="603cd-266">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="603cd-267">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="603cd-267">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-268">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-270">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="603cd-270">The enabled and disabled states of an element.</span></span> <span data-ttu-id="603cd-271">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="603cd-271">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="603cd-272">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-272">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="603cd-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="603cd-273">Value</span></span>                                                                        | <span data-ttu-id="603cd-274">Signification</span><span class="sxs-lookup"><span data-stu-id="603cd-274">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="603cd-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="603cd-276">activé</span><span class="sxs-lookup"><span data-stu-id="603cd-276">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="603cd-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="603cd-278">Désactivé</span><span class="sxs-lookup"><span data-stu-id="603cd-278">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="603cd-279">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="603cd-279">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-280">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="603cd-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-282">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="603cd-282">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="603cd-283">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-284">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="603cd-284">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-287">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="603cd-287">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="603cd-288">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-288">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-289">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="603cd-289">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-290">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-292">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="603cd-292">The current health of the element.</span></span> <span data-ttu-id="603cd-293">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="603cd-293">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="603cd-294">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="603cd-294">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="603cd-295">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="603cd-296">Valeur</span><span class="sxs-lookup"><span data-stu-id="603cd-296">Value</span></span>                                                                        | <span data-ttu-id="603cd-297">Signification</span><span class="sxs-lookup"><span data-stu-id="603cd-297">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="603cd-298"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-298"><dt>5</dt></span></span> </dl> | <span data-ttu-id="603cd-299">Ok</span><span class="sxs-lookup"><span data-stu-id="603cd-299">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="603cd-300">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="603cd-300">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-301">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="603cd-301">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="603cd-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-303">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="603cd-303">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="603cd-304">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="603cd-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="603cd-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-306">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="603cd-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-308">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="603cd-308">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="603cd-309">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-310">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="603cd-310">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-311">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603cd-313">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="603cd-313">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="603cd-314">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="603cd-314">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="603cd-315">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-315">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="603cd-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-317">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-319">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="603cd-319">The last error code reported by the logical device.</span></span> <span data-ttu-id="603cd-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-321">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="603cd-321">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-322">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="603cd-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-324">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="603cd-324">This property has been deprecated.</span></span> <span data-ttu-id="603cd-325">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="603cd-325">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-326">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="603cd-326">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-327">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603cd-329">Qualificateurs : **unités** (« Hertz »)</span><span class="sxs-lookup"><span data-stu-id="603cd-329">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="603cd-330">Taux de rafraîchissement maximal du contrôleur d’affichage, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="603cd-330">The maximum refresh rate of the display controller, in hertz.</span></span> <span data-ttu-id="603cd-331">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-331">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-332">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="603cd-332">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-333">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="603cd-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="603cd-335">Qualificateurs : **unités** (« Hertz »)</span><span class="sxs-lookup"><span data-stu-id="603cd-335">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="603cd-336">Taux d’actualisation minimal du contrôleur vidéo, en Hertz.</span><span class="sxs-lookup"><span data-stu-id="603cd-336">The minimum refresh rate of the video controller, in hertz.</span></span> <span data-ttu-id="603cd-337">Cette propriété est héritée de la [**\_ VideoHead CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-337">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-338">**Nom**</span><span class="sxs-lookup"><span data-stu-id="603cd-338">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-339">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-341">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="603cd-341">The label by which the object is known.</span></span> <span data-ttu-id="603cd-342">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="603cd-342">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-343">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="603cd-343">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-344">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-346">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="603cd-346">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="603cd-347">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="603cd-347">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="603cd-348">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="603cd-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="603cd-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="603cd-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="603cd-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="603cd-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="603cd-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="603cd-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="603cd-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="603cd-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="603cd-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="603cd-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="603cd-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="603cd-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="603cd-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="603cd-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="603cd-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="603cd-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="603cd-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="603cd-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="603cd-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="603cd-368">)</span><span class="sxs-lookup"><span data-stu-id="603cd-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="603cd-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="603cd-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-370">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="603cd-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-372">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="603cd-372">The current statuses of the object.</span></span> <span data-ttu-id="603cd-373">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-374">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="603cd-374">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-375">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-377">Mode d’analyse actuel lorsque la propriété **CurrentScanMode** de l’instance est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="603cd-377">The current scan mode when the instance's **CurrentScanMode** property is 1 (Other).</span></span> <span data-ttu-id="603cd-378">Cette propriété est héritée de [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)) et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="603cd-378">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-379">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="603cd-379">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-380">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-382">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="603cd-382">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="603cd-383">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="603cd-383">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="603cd-384">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="603cd-384">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-385">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="603cd-385">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-386">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="603cd-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="603cd-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-388">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="603cd-388">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="603cd-389">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="603cd-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-390">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="603cd-390">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-391">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="603cd-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-393">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="603cd-393">The power management capabilities of the device.</span></span> <span data-ttu-id="603cd-394">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="603cd-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-396">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="603cd-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-398">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="603cd-398">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="603cd-399">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-400">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="603cd-400">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-401">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="603cd-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-403">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="603cd-403">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="603cd-404">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-404">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-405">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="603cd-405">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-406">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-408">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="603cd-408">Provides high level status information.</span></span> <span data-ttu-id="603cd-409">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="603cd-409">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="603cd-410">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="603cd-410">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="603cd-411">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="603cd-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="603cd-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="603cd-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="603cd-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="603cd-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="603cd-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="603cd-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="603cd-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="603cd-418">)</span><span class="sxs-lookup"><span data-stu-id="603cd-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="603cd-419">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="603cd-419">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-420">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-422">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="603cd-422">The last requested or desired state for the element.</span></span> <span data-ttu-id="603cd-423">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="603cd-423">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="603cd-424">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-424">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="603cd-425">Valeur</span><span class="sxs-lookup"><span data-stu-id="603cd-425">Value</span></span>                                                                         | <span data-ttu-id="603cd-426">Signification</span><span class="sxs-lookup"><span data-stu-id="603cd-426">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="603cd-427"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-427"><dt>12</dt></span></span> </dl> | <span data-ttu-id="603cd-428">Non applicable</span><span class="sxs-lookup"><span data-stu-id="603cd-428">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="603cd-429">**État**</span><span class="sxs-lookup"><span data-stu-id="603cd-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-432">Chaîne qui spécifie l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="603cd-432">A string that specifies the current status of the object.</span></span> <span data-ttu-id="603cd-433">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-433">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-434">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="603cd-434">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-435">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="603cd-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="603cd-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-437">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="603cd-437">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="603cd-438">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="603cd-438">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="603cd-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-440">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-442">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="603cd-442">The current state of the logical device.</span></span> <span data-ttu-id="603cd-443">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-443">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-444">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="603cd-444">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-447">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="603cd-447">The scoping system's creation class name.</span></span> <span data-ttu-id="603cd-448">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="603cd-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="603cd-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-450">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="603cd-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-452">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="603cd-452">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="603cd-453">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="603cd-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="603cd-454">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="603cd-454">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-455">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="603cd-455">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-457">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="603cd-457">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="603cd-458">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="603cd-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-459">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="603cd-459">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-460">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="603cd-460">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-461">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-462">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="603cd-462">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="603cd-463">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="603cd-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="603cd-464">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="603cd-464">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="603cd-465">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="603cd-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="603cd-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="603cd-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="603cd-467">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="603cd-467">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="603cd-468">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="603cd-468">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="603cd-469">Valeur</span><span class="sxs-lookup"><span data-stu-id="603cd-469">Value</span></span>                                                                         | <span data-ttu-id="603cd-470">Signification</span><span class="sxs-lookup"><span data-stu-id="603cd-470">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="603cd-471"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-471"><dt>12</dt></span></span> </dl> | <span data-ttu-id="603cd-472">Non applicable</span><span class="sxs-lookup"><span data-stu-id="603cd-472">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="603cd-473">Notes</span><span class="sxs-lookup"><span data-stu-id="603cd-473">Remarks</span></span>

<span data-ttu-id="603cd-474">L’accès à la classe **MSVM \_ VideoHead** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="603cd-474">Access to the **Msvm\_VideoHead** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="603cd-475">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="603cd-475">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="603cd-476">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="603cd-476">Requirements</span></span>



| <span data-ttu-id="603cd-477">Condition requise</span><span class="sxs-lookup"><span data-stu-id="603cd-477">Requirement</span></span> | <span data-ttu-id="603cd-478">Valeur</span><span class="sxs-lookup"><span data-stu-id="603cd-478">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="603cd-479">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603cd-479">Minimum supported client</span></span><br/> | <span data-ttu-id="603cd-480">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603cd-480">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="603cd-481">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603cd-481">Minimum supported server</span></span><br/> | <span data-ttu-id="603cd-482">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603cd-482">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="603cd-483">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="603cd-483">Namespace</span></span><br/>                | <span data-ttu-id="603cd-484">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="603cd-484">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="603cd-485">MOF</span><span class="sxs-lookup"><span data-stu-id="603cd-485">MOF</span></span><br/>                      | <dl> <span data-ttu-id="603cd-486"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-486"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="603cd-487">DLL</span><span class="sxs-lookup"><span data-stu-id="603cd-487">DLL</span></span><br/>                      | <dl> <span data-ttu-id="603cd-488"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="603cd-488"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="603cd-489">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603cd-489">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603cd-490">**\_VIDEOHEAD CIM**</span><span class="sxs-lookup"><span data-stu-id="603cd-490">**CIM\_VideoHead**</span></span>](cim-videohead.md)
</dt> <dt>

<span data-ttu-id="603cd-491">[**\_VIDEOHEAD CIM**](/previous-versions//cc136948(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="603cd-491">[**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="603cd-492">Classes vidéo</span><span class="sxs-lookup"><span data-stu-id="603cd-492">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

