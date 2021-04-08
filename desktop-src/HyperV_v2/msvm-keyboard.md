---
description: Représente un périphérique clavier.
ms.assetid: 2a59fe90-12e2-471c-b49e-dfb4f4a31e0c
title: Classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard
- Msvm_Keyboard.SetPowerState
- Msvm_Keyboard.EnableDevice
- Msvm_Keyboard.OnlineDevice
- Msvm_Keyboard.QuiesceDevice
- Msvm_Keyboard.SaveProperties
- Msvm_Keyboard.RestoreProperties
- Msvm_Keyboard.InstanceID
- Msvm_Keyboard.Caption
- Msvm_Keyboard.Description
- Msvm_Keyboard.ElementName
- Msvm_Keyboard.InstallDate
- Msvm_Keyboard.Name
- Msvm_Keyboard.OperationalStatus
- Msvm_Keyboard.StatusDescriptions
- Msvm_Keyboard.Status
- Msvm_Keyboard.HealthState
- Msvm_Keyboard.CommunicationStatus
- Msvm_Keyboard.DetailedStatus
- Msvm_Keyboard.OperatingStatus
- Msvm_Keyboard.PrimaryStatus
- Msvm_Keyboard.EnabledState
- Msvm_Keyboard.OtherEnabledState
- Msvm_Keyboard.RequestedState
- Msvm_Keyboard.EnabledDefault
- Msvm_Keyboard.TimeOfLastStateChange
- Msvm_Keyboard.AvailableRequestedStates
- Msvm_Keyboard.TransitioningToState
- Msvm_Keyboard.SystemCreationClassName
- Msvm_Keyboard.SystemName
- Msvm_Keyboard.CreationClassName
- Msvm_Keyboard.DeviceID
- Msvm_Keyboard.PowerManagementSupported
- Msvm_Keyboard.PowerManagementCapabilities
- Msvm_Keyboard.Availability
- Msvm_Keyboard.StatusInfo
- Msvm_Keyboard.LastErrorCode
- Msvm_Keyboard.ErrorDescription
- Msvm_Keyboard.ErrorCleared
- Msvm_Keyboard.OtherIdentifyingInfo
- Msvm_Keyboard.PowerOnHours
- Msvm_Keyboard.TotalPowerOnHours
- Msvm_Keyboard.IdentifyingDescriptions
- Msvm_Keyboard.AdditionalAvailability
- Msvm_Keyboard.MaxQuiesceTime
- Msvm_Keyboard.IsLocked
- Msvm_Keyboard.Layout
- Msvm_Keyboard.NumberOfFunctionKeys
- Msvm_Keyboard.Password
- Msvm_Keyboard.UnicodeSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37c4faceb9072c1851868eb23c031e715cb6e1c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034492"
---
# <a name="msvm_keyboard-class"></a><span data-ttu-id="5a536-103">\_Classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="5a536-103">Msvm\_Keyboard class</span></span>

<span data-ttu-id="5a536-104">Représente un périphérique clavier.</span><span class="sxs-lookup"><span data-stu-id="5a536-104">Represents a keyboard device.</span></span> <span data-ttu-id="5a536-105">Les claviers sont des périphériques logiques qui sont toujours présents sur une machine virtuelle et ne sont donc pas alloués par le biais d’un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="5a536-105">Keyboards are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="5a536-106">Une instance est toujours présente dans un système d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5a536-106">One instance is always present in a virtual computer system.</span></span>

<span data-ttu-id="5a536-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5a536-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a536-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a536-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Keyboard : CIM_UserDevice
{
  string   InstanceID;
  string   Caption = "Keyboard";
  string   Description = "Microsoft Virtual Keyboard";
  string   ElementName = "Keyboard";
  datetime InstallDate;
  string   Name = "Keyboard";
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
  string   CreationClassName = "Msvm_Keyboard";
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
  boolean  IsLocked = False;
  string   Layout = "00000409";
  uint16   NumberOfFunctionKeys = 12;
  uint16   Password = 5;
  boolean  UnicodeSupported;
};
```

## <a name="members"></a><span data-ttu-id="5a536-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5a536-109">Members</span></span>

<span data-ttu-id="5a536-110">La classe de **\_ clavier MSVM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5a536-110">The **Msvm\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="5a536-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a536-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a536-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a536-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a536-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a536-113">Methods</span></span>

<span data-ttu-id="5a536-114">La classe de **\_ clavier MSVM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5a536-114">The **Msvm\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="5a536-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="5a536-115">Method</span></span>                                                         | <span data-ttu-id="5a536-116">Description</span><span class="sxs-lookup"><span data-stu-id="5a536-116">Description</span></span>                                                   |
|:---------------------------------------------------------------|:--------------------------------------------------------------|
| <span data-ttu-id="5a536-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="5a536-117">**EnableDevice**</span></span>                                               | <span data-ttu-id="5a536-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5a536-118">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="5a536-119">**IsKeyPressed**</span><span class="sxs-lookup"><span data-stu-id="5a536-119">**IsKeyPressed**</span></span>](iskeypressed-msvm-keyboard.md)             | <span data-ttu-id="5a536-120">Récupère l’état de clé d’une clé.</span><span class="sxs-lookup"><span data-stu-id="5a536-120">Retrieves the key state of a key.</span></span><br/>                  |
| <span data-ttu-id="5a536-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="5a536-121">**OnlineDevice**</span></span>                                               | <span data-ttu-id="5a536-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5a536-122">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="5a536-123">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="5a536-123">**PressKey**</span></span>](presskey-msvm-keyboard.md)                     | <span data-ttu-id="5a536-124">Simule une pression sur une touche.</span><span class="sxs-lookup"><span data-stu-id="5a536-124">Simulates a key press.</span></span><br/>                             |
| <span data-ttu-id="5a536-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="5a536-125">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="5a536-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5a536-126">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="5a536-127">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="5a536-127">**ReleaseKey**</span></span>](releasekey-msvm-keyboard.md)                 | <span data-ttu-id="5a536-128">Simule une version de clé.</span><span class="sxs-lookup"><span data-stu-id="5a536-128">Simulates a key release.</span></span><br/>                           |
| [<span data-ttu-id="5a536-129">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5a536-129">**RequestStateChange**</span></span>](msvm-keyboard-requeststatechange.md) | <span data-ttu-id="5a536-130">Demande que l’état de l’élément soit modifié.</span><span class="sxs-lookup"><span data-stu-id="5a536-130">Requests that the state of the element be changed.</span></span><br/> |
| [<span data-ttu-id="5a536-131">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="5a536-131">**Reset**</span></span>](msvm-keyboard-reset.md)                           | <span data-ttu-id="5a536-132">Réinitialise le clavier virtuel.</span><span class="sxs-lookup"><span data-stu-id="5a536-132">Resets the virtual keyboard.</span></span><br/>                       |
| <span data-ttu-id="5a536-133">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="5a536-133">**RestoreProperties**</span></span>                                          | <span data-ttu-id="5a536-134">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5a536-134">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="5a536-135">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="5a536-135">**SaveProperties**</span></span>                                             | <span data-ttu-id="5a536-136">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5a536-136">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="5a536-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5a536-137">**SetPowerState**</span></span>                                              | <span data-ttu-id="5a536-138">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5a536-138">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="5a536-139">**TypeCtrlAltDel**</span><span class="sxs-lookup"><span data-stu-id="5a536-139">**TypeCtrlAltDel**</span></span>](typectrlaltdel-msvm-keyboard.md)         | <span data-ttu-id="5a536-140">Simule une séquence de touches Ctrl + Alt + Suppr.</span><span class="sxs-lookup"><span data-stu-id="5a536-140">Simulates a Ctrl+Alt+Del key sequence.</span></span><br/>             |
| [<span data-ttu-id="5a536-141">**TypeKey**</span><span class="sxs-lookup"><span data-stu-id="5a536-141">**TypeKey**</span></span>](typekey-msvm-keyboard.md)                       | <span data-ttu-id="5a536-142">Simule une séquence de touches d’appui sur la touche.</span><span class="sxs-lookup"><span data-stu-id="5a536-142">Simulates a press-release key sequence.</span></span><br/>            |
| [<span data-ttu-id="5a536-143">**TypeScancodes**</span><span class="sxs-lookup"><span data-stu-id="5a536-143">**TypeScancodes**</span></span>](msvm-keyboard-typescancodes.md)           | <span data-ttu-id="5a536-144">Simule une séquence de touches à l’aide de codes d’analyse.</span><span class="sxs-lookup"><span data-stu-id="5a536-144">Simulates a key sequence using scan codes.</span></span><br/>         |
| [<span data-ttu-id="5a536-145">**TypeText**</span><span class="sxs-lookup"><span data-stu-id="5a536-145">**TypeText**</span></span>](typetext-msvm-keyboard.md)                     | <span data-ttu-id="5a536-146">Simule une série de caractères typés.</span><span class="sxs-lookup"><span data-stu-id="5a536-146">Simulates a series of typed characters.</span></span><br/>            |



 

### <a name="properties"></a><span data-ttu-id="5a536-147">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a536-147">Properties</span></span>

<span data-ttu-id="5a536-148">La classe de **\_ clavier MSVM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5a536-148">The **Msvm\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a536-149">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="5a536-149">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-150">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a536-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-152">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="5a536-152">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="5a536-153">La propriété de **disponibilité** indique l’état principal et la disponibilité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a536-153">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="5a536-154">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5a536-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-155">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="5a536-155">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-156">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-158">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a536-158">The primary availability and status of the device.</span></span> <span data-ttu-id="5a536-159">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5a536-159">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-160">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5a536-160">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-161">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a536-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-163">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5a536-163">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="5a536-164">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5a536-164">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5a536-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a536-168">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="5a536-168">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a536-169">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5a536-169">A short description of the object.</span></span> <span data-ttu-id="5a536-170">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-171">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5a536-171">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-174">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="5a536-174">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5a536-175">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5a536-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a536-176">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5a536-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5a536-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5a536-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="5a536-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="5a536-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="5a536-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5a536-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5a536-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5a536-184">)</span><span class="sxs-lookup"><span data-stu-id="5a536-184">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a536-185">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a536-185">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a536-188">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5a536-188">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a536-189">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="5a536-189">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5a536-190">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="5a536-190">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="5a536-191">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5a536-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-192">**Description**</span><span class="sxs-lookup"><span data-stu-id="5a536-192">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-195">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="5a536-195">A description of the object.</span></span> <span data-ttu-id="5a536-196">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-197">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5a536-197">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-200">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5a536-200">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5a536-201">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5a536-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a536-202">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5a536-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="5a536-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="5a536-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="5a536-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="5a536-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="5a536-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="5a536-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5a536-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5a536-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5a536-211">)</span><span class="sxs-lookup"><span data-stu-id="5a536-211">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a536-212">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5a536-212">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-215">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="5a536-215">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="5a536-216">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID*».</span><span class="sxs-lookup"><span data-stu-id="5a536-216">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="5a536-217">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5a536-217">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-220">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5a536-220">A display name for the object.</span></span> <span data-ttu-id="5a536-221">Cette propriété permet à chaque instance de définir un nom complet en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="5a536-221">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="5a536-222">La propriété [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la **classe \_ ManagedSystemElement CIM** est également définie en tant que nom complet.</span><span class="sxs-lookup"><span data-stu-id="5a536-222">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="5a536-223">Toutefois, il est souvent sous-classé comme une clé.</span><span class="sxs-lookup"><span data-stu-id="5a536-223">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="5a536-224">Il n’est pas raisonnable que la même propriété puisse transmettre à la fois l’identité et un nom d’affichage, sans incohérence.</span><span class="sxs-lookup"><span data-stu-id="5a536-224">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="5a536-225">Où le **nom** existe et n’est pas une clé (par exemple, pour les instances de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), les mêmes informations peuvent être présentes dans les propriétés **Name** et **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="5a536-225">Where **Name** exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="5a536-226">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5a536-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-228">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-230">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5a536-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5a536-231">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a536-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5a536-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a536-232">Value</span></span>                                                                        | <span data-ttu-id="5a536-233">Signification</span><span class="sxs-lookup"><span data-stu-id="5a536-233">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="5a536-234"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-234"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5a536-235">activé</span><span class="sxs-lookup"><span data-stu-id="5a536-235">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a536-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5a536-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-237">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-239">Indique les États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5a536-239">Indicates the enabled and disabled states of an element.</span></span> <span data-ttu-id="5a536-240">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="5a536-240">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5a536-241">Par exemple, l’arrêt (valeur = 4) et le démarrage (valeur = 10) sont des États transitoires entre activé et désactivé.</span><span class="sxs-lookup"><span data-stu-id="5a536-241">For example, shutting down (value=4) and starting (value=10) are transient states between enabled and disabled.</span></span>



| <span data-ttu-id="5a536-242">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a536-242">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="5a536-243">Signification</span><span class="sxs-lookup"><span data-stu-id="5a536-243">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="5a536-244"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-244"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="5a536-245">Unknown</span><span class="sxs-lookup"><span data-stu-id="5a536-245">Unknown</span></span><br/>                                                                                                                                                                                              |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="5a536-246"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-246"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="5a536-247">Autres</span><span class="sxs-lookup"><span data-stu-id="5a536-247">Other</span></span><br/>                                                                                                                                                                                                |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="5a536-248"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-248"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="5a536-249">L’élément est ou peut exécuter des commandes, traite toutes les commandes mises en file d’attente et met en file d’attente les nouvelles requêtes.</span><span class="sxs-lookup"><span data-stu-id="5a536-249">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="5a536-250"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-250"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="5a536-251">L’élément n’exécutera pas de commande et supprimera toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="5a536-251">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="5a536-252"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-252"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="5a536-253">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="5a536-253">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="5a536-254"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-254"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="5a536-255">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="5a536-255">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="5a536-256"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-256"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="5a536-257">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="5a536-257">The element might be completing commands and will drop any new requests.</span></span><br/>                                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="5a536-258"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-258"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="5a536-259">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="5a536-259">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="5a536-260"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-260"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="5a536-261">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="5a536-261">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="5a536-262"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-262"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="5a536-263">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="5a536-263">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="5a536-264">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="5a536-264">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="5a536-265">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5a536-265">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="5a536-266">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-266"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="5a536-267">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="5a536-267">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="5a536-268">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5a536-268">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="5a536-269"><dt>**DMTF réservé**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-269"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="5a536-270">Cette valeur est réservée.</span><span class="sxs-lookup"><span data-stu-id="5a536-270">This value is reserved.</span></span><br/>                                                                                                                                                                              |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="5a536-271"><dt>**Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-271"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="5a536-272">Cette valeur est réservée.</span><span class="sxs-lookup"><span data-stu-id="5a536-272">This value is reserved.</span></span><br/>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="5a536-273">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5a536-273">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-274">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5a536-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-276">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="5a536-276">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="5a536-277">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-277">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-278">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5a536-278">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-281">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="5a536-281">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="5a536-282">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-283">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5a536-283">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-284">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-286">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="5a536-286">The current health of the element.</span></span> <span data-ttu-id="5a536-287">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="5a536-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5a536-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-289">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5a536-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a536-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-291">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="5a536-291">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="5a536-292">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5a536-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5a536-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-294">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a536-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-296">Date et heure de création de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5a536-296">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="5a536-297">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a536-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a536-301">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="5a536-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5a536-302">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="5a536-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5a536-303">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="5a536-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-305">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5a536-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-307">Indique si l’appareil est verrouillé, empêchant l’entrée ou la sortie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5a536-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="5a536-308">Cette propriété est héritée de la [**\_ UserDevice CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="5a536-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5a536-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-310">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a536-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-312">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="5a536-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="5a536-313">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-314">**Disposition**</span><span class="sxs-lookup"><span data-stu-id="5a536-314">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-317">Chaîne indiquant le format et la mise en page du clavier.</span><span class="sxs-lookup"><span data-stu-id="5a536-317">A string indicating the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-318">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="5a536-318">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-319">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a536-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-321">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="5a536-321">This property has been deprecated.</span></span> <span data-ttu-id="5a536-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-323">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5a536-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a536-326">Qualificateurs : **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="5a536-326">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="5a536-327">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="5a536-327">The label by which the object is known.</span></span> <span data-ttu-id="5a536-328">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="5a536-328">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="5a536-329">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-330">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="5a536-330">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-331">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-333">Nombre de touches de fonction sur le clavier.</span><span class="sxs-lookup"><span data-stu-id="5a536-333">The number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-334">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5a536-334">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-335">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-337">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5a536-337">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5a536-338">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5a536-338">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a536-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5a536-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5a536-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5a536-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="5a536-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="5a536-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="5a536-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="5a536-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="5a536-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="5a536-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="5a536-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="5a536-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="5a536-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="5a536-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="5a536-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="5a536-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="5a536-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="5a536-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="5a536-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5a536-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5a536-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5a536-359">)</span><span class="sxs-lookup"><span data-stu-id="5a536-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a536-360">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5a536-360">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-361">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a536-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-363">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="5a536-363">The current status of the element.</span></span> <span data-ttu-id="5a536-364">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="5a536-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-365">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5a536-365">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-366">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-368">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="5a536-368">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5a536-369">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="5a536-369">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5a536-370">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a536-370">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-371">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5a536-371">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-372">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5a536-372">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a536-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-374">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="5a536-374">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="5a536-375">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5a536-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-376">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="5a536-376">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-377">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-379">Indique si un mot de passe de niveau matériel est activé sur le clavier, ce qui empêche l’entrée locale.</span><span class="sxs-lookup"><span data-stu-id="5a536-379">Indicates whether a hardware-level password is enabled at the keyboard, preventing local input.</span></span>

<dt>

<span data-ttu-id="5a536-380">5</span><span class="sxs-lookup"><span data-stu-id="5a536-380">5</span></span>
</dt> <dd>

<span data-ttu-id="5a536-381">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="5a536-381">Not implemented.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a536-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5a536-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-383">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a536-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-385">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5a536-385">The power management capabilities of the device.</span></span> <span data-ttu-id="5a536-386">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5a536-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-388">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5a536-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-390">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="5a536-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="5a536-391">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5a536-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-393">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a536-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-395">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="5a536-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="5a536-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5a536-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-398">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-400">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="5a536-400">Provides high level status information.</span></span> <span data-ttu-id="5a536-401">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="5a536-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5a536-402">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5a536-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a536-403">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a536-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5a536-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5a536-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="5a536-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="5a536-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="5a536-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5a536-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5a536-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5a536-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5a536-410">)</span><span class="sxs-lookup"><span data-stu-id="5a536-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a536-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5a536-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-412">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-414">Dernier État demandé pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="5a536-414">The last requested state for the element.</span></span>



| <span data-ttu-id="5a536-415">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a536-415">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="5a536-416">Signification</span><span class="sxs-lookup"><span data-stu-id="5a536-416">Meaning</span></span>                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="5a536-417"><dt>**Non applicable**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-417"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="5a536-418">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="5a536-418">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a536-419">**État**</span><span class="sxs-lookup"><span data-stu-id="5a536-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-420">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-422">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5a536-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-424">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5a536-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a536-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-426">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5a536-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5a536-427">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="5a536-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="5a536-428">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5a536-428">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-429">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-431">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="5a536-431">The current state of the logical device.</span></span> <span data-ttu-id="5a536-432">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a536-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a536-436">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5a536-436">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a536-437">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5a536-437">The scoping system's creation class name.</span></span> <span data-ttu-id="5a536-438">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="5a536-438">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="5a536-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5a536-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-440">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a536-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a536-442">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5a536-442">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a536-443">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5a536-443">The scoping system's name.</span></span> <span data-ttu-id="5a536-444">Cette valeur correspond à la valeur de la propriété **Name** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) pour l’ordinateur virtuel d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5a536-444">This value corresponds to the value of the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for the scoping virtual machine.</span></span> <span data-ttu-id="5a536-445">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5a536-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5a536-446">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5a536-446">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-447">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a536-447">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-449">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="5a536-449">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5a536-450">Si l’état de l’élément n’a pas été modifié et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="5a536-450">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="5a536-451">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5a536-451">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="5a536-452">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5a536-452">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-453">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5a536-453">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-454">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a536-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-456">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="5a536-456">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="5a536-457">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5a536-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-458">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5a536-458">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-459">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a536-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-461">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="5a536-461">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5a536-462">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5a536-462">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5a536-463">**UnicodeSupported**</span><span class="sxs-lookup"><span data-stu-id="5a536-463">**UnicodeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a536-464">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5a536-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a536-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a536-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a536-466">Indique si le clavier virtuel prend en charge les caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a536-466">Indicates if the virtual keyboard supports Unicode characters.</span></span> <span data-ttu-id="5a536-467">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5a536-467">This can be one of the following values.</span></span>



| <span data-ttu-id="5a536-468">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a536-468">Value</span></span>                                                                            | <span data-ttu-id="5a536-469">Signification</span><span class="sxs-lookup"><span data-stu-id="5a536-469">Meaning</span></span>                                                              |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a536-470"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-470"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="5a536-471">Le clavier virtuel prend en charge les caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a536-471">The virtual keyboard supports Unicode characters.</span></span><br/>         |
| <dl> <span data-ttu-id="5a536-472"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-472"><dt>False</dt></span></span> </dl> | <span data-ttu-id="5a536-473">Le clavier virtuel ne prend pas en charge les caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a536-473">The virtual keyboard does not support Unicode characters.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a536-474">Notes</span><span class="sxs-lookup"><span data-stu-id="5a536-474">Remarks</span></span>

<span data-ttu-id="5a536-475">L’accès à la classe de **\_ clavier MSVM** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="5a536-475">Access to the **Msvm\_Keyboard** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5a536-476">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5a536-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a536-477">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a536-477">Requirements</span></span>



| <span data-ttu-id="5a536-478">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a536-478">Requirement</span></span> | <span data-ttu-id="5a536-479">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a536-479">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a536-480">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a536-480">Minimum supported client</span></span><br/> | <span data-ttu-id="5a536-481">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a536-481">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5a536-482">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a536-482">Minimum supported server</span></span><br/> | <span data-ttu-id="5a536-483">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a536-483">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a536-484">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5a536-484">Namespace</span></span><br/>                | <span data-ttu-id="5a536-485">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5a536-485">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5a536-486">MOF</span><span class="sxs-lookup"><span data-stu-id="5a536-486">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a536-487"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-487"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a536-488">DLL</span><span class="sxs-lookup"><span data-stu-id="5a536-488">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a536-489"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a536-489"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a536-490">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a536-490">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a536-491">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5a536-491">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dt>

[<span data-ttu-id="5a536-492">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5a536-492">**CIM\_UserDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-userdevice)
</dt> <dt>

[<span data-ttu-id="5a536-493">Classes d’entrée</span><span class="sxs-lookup"><span data-stu-id="5a536-493">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

