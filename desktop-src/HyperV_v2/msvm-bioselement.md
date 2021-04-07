---
description: Représente le logiciel de bas niveau qui est chargé dans la mémoire RAM pour configurer et démarrer le système.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Classe Msvm_BIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863114"
---
# <a name="msvm_bioselement-class"></a><span data-ttu-id="ccf0f-103">MSVM \_ BIOSElement, classe</span><span class="sxs-lookup"><span data-stu-id="ccf0f-103">Msvm\_BIOSElement class</span></span>

<span data-ttu-id="ccf0f-104">Représente le logiciel de bas niveau qui est chargé dans la mémoire RAM pour configurer et démarrer le système.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-104">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span> <span data-ttu-id="ccf0f-105">Le BIOS n’est pas un périphérique logique. par conséquent, le BIOS virtuel ne doit pas être considéré comme un périphérique de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-105">The BIOS is not a logical device, hence the virtual BIOS should not be thought of as a virtual machine device.</span></span> <span data-ttu-id="ccf0f-106">Comme il ne s’agit pas d’un appareil, il n’a pas de pool de ressources correspondant.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-106">As it is not a device, it does not have a corresponding resource pool.</span></span> <span data-ttu-id="ccf0f-107">L’objet BIOS est associé à la machine virtuelle via l’Association [**MSVM \_ SystemBIOS**](msvm-systembios.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf0f-107">The BIOS object is associated with the virtual machine through the [**Msvm\_SystemBIOS**](msvm-systembios.md) association.</span></span>

<span data-ttu-id="ccf0f-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf0f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccf0f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
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
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a><span data-ttu-id="ccf0f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ccf0f-110">Members</span></span>

<span data-ttu-id="ccf0f-111">La classe **MSVM \_ BIOSElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ccf0f-111">The **Msvm\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ccf0f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ccf0f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccf0f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ccf0f-113">Properties</span></span>

<span data-ttu-id="ccf0f-114">La classe **MSVM \_ BIOSElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-114">The **Msvm\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccf0f-115">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-115">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-118">Numéro de série de la carte de base sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-118">The serial number for the base board on the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-119">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-119">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-122">Identificateur unique du BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-122">The unique identifier for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-123">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-123">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-124">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-126">État activé du verrouillage numérique dans le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-126">The enabled state of the Num Lock in the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-127">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-127">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-130">Numéro de série du BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-130">The serial number for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-131">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-131">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-132">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-134">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-134">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-135">L’ordre dans lequel les appareils seront recherchés pour un secteur d’amorçage au démarrage.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-135">The order in which devices will be searched for a boot sector at startup.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-136">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-136">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-139">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-139">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-140">Identificateur interne pour cette compilation d’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-140">The internal identifier for this compilation of software element.</span></span> <span data-ttu-id="ccf0f-141">Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur 14.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-141">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 14.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-145">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-145">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-146">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-146">A short description of the object.</span></span> <span data-ttu-id="ccf0f-147">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-148">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-148">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-151">Renseigné automatiquement par le BIOS lorsque la machine virtuelle est créée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-151">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-152">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-152">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-155">Renseigné automatiquement par le BIOS lorsque la machine virtuelle est créée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-155">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-156">**Codes**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-156">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-159">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-159">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-160">Ensemble de codes utilisé par l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-160">The code set used by the software element.</span></span> <span data-ttu-id="ccf0f-161">Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-161">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-165">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ccf0f-166">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ccf0f-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-168">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-168">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-171">Langue actuellement sélectionnée pour le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-171">The currently selected language for the BIOS.</span></span> <span data-ttu-id="ccf0f-172">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « en \| -US \| iso8859-1 ».</span><span class="sxs-lookup"><span data-stu-id="ccf0f-172">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-173">**Description**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-176">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ccf0f-176">A description of the object.</span></span> <span data-ttu-id="ccf0f-177">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-181">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-181">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ccf0f-182">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ccf0f-183">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-187">Nom complet de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-187">A display name for the element.</span></span> <span data-ttu-id="ccf0f-188">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-192">Spécifie l’intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-192">Specifies the current health of the element.</span></span> <span data-ttu-id="ccf0f-193">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="ccf0f-194">Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-194">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="ccf0f-195">La propriété **EnabledState** peut également contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-195">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="ccf0f-196">Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-196">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="ccf0f-197">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="ccf0f-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccf0f-198">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="ccf0f-199">Signification</span><span class="sxs-lookup"><span data-stu-id="ccf0f-199">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="ccf0f-200"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-200"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="ccf0f-201">L’ordinateur virtuel est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-201">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="ccf0f-202"><dt>**Erreur majeure**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-202"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="ccf0f-203">L’ordinateur virtuel a subi un échec majeur.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-203">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="ccf0f-204">Cette valeur est utilisée lorsqu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque et que l’ordinateur virtuel a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-204">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="ccf0f-205"><dt>**Erreur critique**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-205"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="ccf0f-206">L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-206">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="ccf0f-207">Cela peut indiquer que le processus de travail de l’ordinateur virtuel (Vmwp.exe) ne répond pas aux demandes de contrôle ou d’informations, ou qu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-207">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ccf0f-208">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-208">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-211">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-211">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-212">Identificateur du fabricant de cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-212">The manufacturer's identifier for this software element.</span></span> <span data-ttu-id="ccf0f-213">Il s’agit souvent d’une référence (SKU) ou d’un numéro de référence.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-213">Often this will be a stock keeping unit (SKU) or a part number.</span></span> <span data-ttu-id="ccf0f-214">Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-214">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-216">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-218">Renseigné automatiquement par le BIOS lorsque la machine virtuelle est créée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-218">Automatically populated by the BIOS when the virtual machine is created.</span></span> <span data-ttu-id="ccf0f-219">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-220">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-220">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-223">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-223">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-224">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-224">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ccf0f-225">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-226">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-226">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-229">Qualificateurs : **MaxLen** (32)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-229">Qualifiers: **MaxLen** (32)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-230">Édition linguistique de cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-230">The language edition of this software element.</span></span> <span data-ttu-id="ccf0f-231">Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-231">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-232">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-232">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-233">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-233">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-235">Liste des langues installables pour le BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-235">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="ccf0f-236">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « en \| -US \| iso8859-1 ».</span><span class="sxs-lookup"><span data-stu-id="ccf0f-236">THIS property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-237">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-237">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-238">Type de données : **unit64**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-238">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-240">Adresse de fin de la mémoire occupée par ce BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-240">The ending address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="ccf0f-241">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-241">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-242">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-242">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-243">Type de données : **unit64**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-243">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-245">Adresse de début de la mémoire occupée par ce BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-245">The starting address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="ccf0f-246">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur 0xE0000.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-246">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xE0000.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-247">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-247">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-250">Chaîne qui décrit l’utilitaire Flash/chargement BIOS requis pour mettre à jour l’élément BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-250">A string that describes the BIOS flash/load utility that is required to update the BIOS element.</span></span> <span data-ttu-id="ccf0f-251">La version et d’autres informations peuvent être indiquées dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-251">Version and other information may be indicated in this property.</span></span> <span data-ttu-id="ccf0f-252">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-252">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-253">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-253">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-254">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-256">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-256">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-257">Fabricant de ce BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-257">The manufacturer of this BIOS.</span></span> <span data-ttu-id="ccf0f-258">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « Microsoft Corporation ».</span><span class="sxs-lookup"><span data-stu-id="ccf0f-258">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-259">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-259">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-262">Qualificateurs : **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-262">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-263">Nom utilisé pour identifier cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-263">The name used to identify this software element.</span></span> <span data-ttu-id="ccf0f-264">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-264">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="ccf0f-265">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur « BIOS ».</span><span class="sxs-lookup"><span data-stu-id="ccf0f-265">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "BIOS".</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-269">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ccf0f-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ccf0f-270">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ccf0f-271">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-273">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-275">Tableau qui contient les États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-275">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="ccf0f-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="ccf0f-277">La valeur à l’index zéro (0) est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-277">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="ccf0f-278">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccf0f-278">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="ccf0f-279">Signification</span><span class="sxs-lookup"><span data-stu-id="ccf0f-279">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="ccf0f-280"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-280"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="ccf0f-281">L’ordinateur virtuel est fonctionnel et fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-281">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="ccf0f-282"><dt>**Dégradé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-282"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="ccf0f-283">L’ordinateur virtuel ne fonctionne que partiellement.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-283">The virtual machine is only partially functional.</span></span> <span data-ttu-id="ccf0f-284">Cela indique que le stockage qui contient la configuration n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-284">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="ccf0f-285">Une machine virtuelle dans cet État peut uniquement être désactivée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-285">A virtual machine in this state may only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="ccf0f-286"><dt>**Échec prédictif**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-286"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="ccf0f-287">L’ordinateur virtuel est fonctionnel mais peut échouer à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-287">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="ccf0f-288">Cela indique que l’espace libre est insuffisant sur le stockage qui contient le disque dur virtuel de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-288">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="ccf0f-289">L’ordinateur virtuel sera mis en pause si l’espace disque disponible est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-289">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="ccf0f-290"><dt></dt> <dt>10</dt> arrêtés</span><span class="sxs-lookup"><span data-stu-id="ccf0f-290"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="ccf0f-291">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-291">This value is not supported.</span></span> <span data-ttu-id="ccf0f-292">Si la machine virtuelle est arrêtée, la propriété **EnabledState** aura la valeur 3 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-292">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="ccf0f-293"><dt>**Dans le service**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-293"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="ccf0f-294">L’ordinateur virtuel est en cours de traitement d’une demande.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-294">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="ccf0f-295"><dt>**Dormant**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-295"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="ccf0f-296">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-296">This value is not supported.</span></span> <span data-ttu-id="ccf0f-297">Si la machine virtuelle est interrompue ou suspendue, la propriété **EnabledState** aura la valeur 32769 (suspendu) ou 32768 (suspendu).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-297">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="ccf0f-298">La valeur à l’index 1 (1) est facultative et contient des informations d’état secondaire.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-298">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="ccf0f-299">Un client doit utiliser l’état principal de l’index zéro (0) pour déterminer si une nouvelle demande peut être émise pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-299">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="ccf0f-300">Si **OperationalStatus** \[ 0 \] est égal à 2 (OK), l’opération indiquée par **OperationalStatus** \[ 1 \] peut être interrompue.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-300">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="ccf0f-301">La valeur à **OperationalStatus** \[ 1 \] est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-301">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="ccf0f-302">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccf0f-302">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="ccf0f-303">Signification</span><span class="sxs-lookup"><span data-stu-id="ccf0f-303">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="ccf0f-304"><dt>**Création de l’instantané**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-304"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="ccf0f-305">Un instantané est en cours de création pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-305">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="ccf0f-306"><dt>**Application de l’instantané**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-306"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="ccf0f-307">Un instantané est en cours d’application sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-307">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="ccf0f-308"><dt>**Suppression de l’instantané**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-308"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="ccf0f-309">Un instantané est en cours de suppression de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-309">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="ccf0f-310"><dt>**En attente de démarrage de**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-310"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="ccf0f-311">L’ordinateur virtuel démarre une fois que le délai de démarrage automatique s’est écoulé.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-311">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="ccf0f-312"><dt>**Fusion des disques**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-312"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="ccf0f-313">Les disques durs virtuels des instantanés précédemment supprimés sont en cours de fusion.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-313">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="ccf0f-314"><dt>**Exportation de l’ordinateur virtuel**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-314"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="ccf0f-315">L’ordinateur virtuel est en cours d’exportation.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-315">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="ccf0f-316"><dt>**Migration de la machine virtuelle**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-316"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="ccf0f-317">L’ordinateur virtuel est en cours de migration dynamique d’un ordinateur physique vers un autre.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-317">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="ccf0f-318">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-318">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-321">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-321">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-322">Fabricant et système d’exploitation d’un élément logiciel lorsque la propriété **TargetOperatingSystem** a la valeur 1 (autre), ce qui nécessite que la propriété **OtherTargetOS** ait une valeur non **null** .</span><span class="sxs-lookup"><span data-stu-id="ccf0f-322">The manufacturer and operating system for a software element when the **TargetOperatingSystem** property has a value of 1 (Other), which requires the **OtherTargetOS** property to have a non-**Null** value.</span></span> <span data-ttu-id="ccf0f-323">Pour toutes les autres valeurs de **TargetOperatingSystem**, la propriété **OtherTargetOS** doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-323">For all other values of **TargetOperatingSystem**, the **OtherTargetOS** property must be **Null**.</span></span> <span data-ttu-id="ccf0f-324">Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-324">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-325">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-325">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-326">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-328">Si la valeur est true, il s’agit du BIOS principal du système informatique.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-328">If True, this is the primary BIOS of the computer system.</span></span> <span data-ttu-id="ccf0f-329">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-329">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-330">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-330">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-331">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-333">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-333">Provides high level status information.</span></span> <span data-ttu-id="ccf0f-334">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-334">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="ccf0f-335">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ccf0f-336">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-337">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-337">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-338">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-340">Tableau de chaînes représentant l’emplacement de publication du registre des attributs BIOS ou des registres dont l’implémentation est conforme.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-340">An array of strings representing the publication location of the BIOS attribute registry or registries the implementation complies to.</span></span> <span data-ttu-id="ccf0f-341">Cette propriété est héritée de la [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-341">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-342">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-342">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-343">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-343">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-345">Date à laquelle le BIOS a été publié.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-345">The date that the BIOS was released.</span></span> <span data-ttu-id="ccf0f-346">Cette propriété est héritée de la [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-346">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-347">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-347">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-350">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-350">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-351">Numéro de série attribué au BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-351">The assigned serial number of the BIOS.</span></span> <span data-ttu-id="ccf0f-352">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-352">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-353">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-353">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-354">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-356">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-356">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-357">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-357">An identifier for the software element.</span></span> <span data-ttu-id="ccf0f-358">Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur « Microsoft :*GUID* \\ *Device-Specific Data*».</span><span class="sxs-lookup"><span data-stu-id="ccf0f-358">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-359">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-359">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-360">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-362">État du cycle de vie d’un élément de logiciel.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-362">The state of a software element's life cycle.</span></span> <span data-ttu-id="ccf0f-363">Cette propriété est héritée de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur 2 (exécutable).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-363">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 2 (Executable).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-364">**État**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-365">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-367">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-368">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-368">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-369">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-371">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="ccf0f-371">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-372">Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-372">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="ccf0f-373">Par exemple, si 11 (en service) est la valeur affectée à **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] peut contenir une explication sur la raison pour laquelle l’ordinateur virtuel traite une demande.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-373">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="ccf0f-374">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-375">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-375">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-378">Environnement du système d’exploitation de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-378">The element's operating system environment.</span></span> <span data-ttu-id="ccf0f-379">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)et est toujours définie sur 0 (inconnu).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-379">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 0 (Unknown).</span></span>

</dd> <dt>

<span data-ttu-id="ccf0f-380">**Version**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccf0f-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ccf0f-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccf0f-383">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccf0f-383">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ccf0f-384">Version du BIOS.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-384">The version of the BIOS.</span></span> <span data-ttu-id="ccf0f-385">Cette propriété est héritée de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)et est toujours définie sur « 8.02.00 ».</span><span class="sxs-lookup"><span data-stu-id="ccf0f-385">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "8.02.00".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ccf0f-386">Notes</span><span class="sxs-lookup"><span data-stu-id="ccf0f-386">Remarks</span></span>

<span data-ttu-id="ccf0f-387">L’accès à la classe **MSVM \_ BIOSElement** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="ccf0f-387">Access to the **Msvm\_BIOSElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ccf0f-388">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ccf0f-388">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf0f-389">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccf0f-389">Requirements</span></span>



| <span data-ttu-id="ccf0f-390">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccf0f-390">Requirement</span></span> | <span data-ttu-id="ccf0f-391">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccf0f-391">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf0f-392">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccf0f-392">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf0f-393">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccf0f-393">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ccf0f-394">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccf0f-394">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf0f-395">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccf0f-395">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccf0f-396">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ccf0f-396">Namespace</span></span><br/>                | <span data-ttu-id="ccf0f-397">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ccf0f-397">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ccf0f-398">MOF</span><span class="sxs-lookup"><span data-stu-id="ccf0f-398">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccf0f-399"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-399"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccf0f-400">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf0f-400">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf0f-401"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ccf0f-401"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ccf0f-402">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccf0f-402">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf0f-403">**\_BIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-403">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="ccf0f-404">Classes BIOS</span><span class="sxs-lookup"><span data-stu-id="ccf0f-404">BIOS Classes</span></span>](bios-classes.md)
</dt> <dt>

[<span data-ttu-id="ccf0f-405">**\_BIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ccf0f-405">**CIM\_BIOSElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

