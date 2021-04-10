---
description: Le \_ SystemSlot Win32 &\# 32 ; La classe WMI représente les points de connexion physiques, y compris les ports, les emplacements de carte mère et les périphériques, ainsi que les points de connexion propriétaires.
ms.assetid: 0bdce597-dcbe-4593-b0d6-68c3bfecd0ee
ms.tgt_platform: multiple
title: Classe Win32_SystemSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSlot
- Win32_SystemSlot.BusNumber
- Win32_SystemSlot.Caption
- Win32_SystemSlot.ConnectorPinout
- Win32_SystemSlot.ConnectorType
- Win32_SystemSlot.CreationClassName
- Win32_SystemSlot.CurrentUsage
- Win32_SystemSlot.Description
- Win32_SystemSlot.DeviceNumber
- Win32_SystemSlot.FunctionNumber
- Win32_SystemSlot.HeightAllowed
- Win32_SystemSlot.InstallDate
- Win32_SystemSlot.LengthAllowed
- Win32_SystemSlot.Manufacturer
- Win32_SystemSlot.MaxDataWidth
- Win32_SystemSlot.Model
- Win32_SystemSlot.Name
- Win32_SystemSlot.Number
- Win32_SystemSlot.OtherIdentifyingInfo
- Win32_SystemSlot.PartNumber
- Win32_SystemSlot.PMESignal
- Win32_SystemSlot.PoweredOn
- Win32_SystemSlot.PurposeDescription
- Win32_SystemSlot.SegmentGroupNumber
- Win32_SystemSlot.SerialNumber
- Win32_SystemSlot.Shared
- Win32_SystemSlot.SKU
- Win32_SystemSlot.SlotDesignation
- Win32_SystemSlot.SpecialPurpose
- Win32_SystemSlot.Status
- Win32_SystemSlot.SupportsHotPlug
- Win32_SystemSlot.Tag
- Win32_SystemSlot.ThermalRating
- Win32_SystemSlot.VccMixedVoltageSupport
- Win32_SystemSlot.Version
- Win32_SystemSlot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e2913aa2d8850aae4fdad8fbca71f216cd848f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111478"
---
# <a name="win32_systemslot-class"></a><span data-ttu-id="0ea05-103">\_Classe SystemSlot Win32</span><span class="sxs-lookup"><span data-stu-id="0ea05-103">Win32\_SystemSlot class</span></span>

<span data-ttu-id="0ea05-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemSlot** WMI représente des points de connexion physiques, y compris les ports, les emplacements de carte mère et les périphériques, ainsi que les points de connexion propriétaires.</span><span class="sxs-lookup"><span data-stu-id="0ea05-104">The **Win32\_SystemSlot** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection points including ports, motherboard slots and peripherals, and proprietary connection points.</span></span>

<span data-ttu-id="0ea05-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0ea05-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0ea05-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0ea05-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea05-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ea05-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B91-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSlot : CIM_Slot
{
  uint32   BusNumber;
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  uint16   CurrentUsage;
  string   Description;
  uint32   DeviceNumber;
  uint32   FunctionNumber;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PMESignal;
  boolean  PoweredOn;
  string   PurposeDescription;
  uint32   SegmentGroupNumber;
  string   SerialNumber;
  boolean  Shared;
  string   SKU;
  string   SlotDesignation;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="0ea05-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0ea05-108">Members</span></span>

<span data-ttu-id="0ea05-109">La classe **Win32 \_ SystemSlot** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0ea05-109">The **Win32\_SystemSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="0ea05-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ea05-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ea05-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ea05-111">Properties</span></span>

<span data-ttu-id="0ea05-112">La classe **Win32 \_ SystemSlot** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0ea05-112">The **Win32\_SystemSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ea05-113">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="0ea05-113">**BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ea05-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-116">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| bus Number")</span><span class="sxs-lookup"><span data-stu-id="0ea05-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Bus Number")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-117">Numéro de bus SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-117">SMBIOS Bus Number.</span></span>

<span data-ttu-id="0ea05-118">Cette valeur provient du membre du **numéro de bus** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-118">This value comes from the **Bus Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-119">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="0ea05-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0ea05-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-123">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-124">Description succincte d’un objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="0ea05-124">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="0ea05-125">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-126">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="0ea05-126">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-129">Chaîne de forme libre qui décrit la configuration du code confidentiel et l’utilisation des signaux d’un connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-129">Free-form string that describes the pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="0ea05-130">Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-130">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-131">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="0ea05-131">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-132">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ea05-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-134">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("type d' \| emplacement SMBIOS type 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="0ea05-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Type")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-135">Tableau d’attributs physiques du connecteur utilisé par cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="0ea05-135">Array of physical attributes of the connector that this slot uses.</span></span>

<span data-ttu-id="0ea05-136">Cette valeur provient du membre de **type d’emplacement** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-136">This value comes from the **Slot Type** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-137">Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-137">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="0ea05-138">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="0ea05-138">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ea05-139">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0ea05-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0ea05-140">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0ea05-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="0ea05-141">**Mâle** (2)</span><span class="sxs-lookup"><span data-stu-id="0ea05-141">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="0ea05-142">**Femme** (3)</span><span class="sxs-lookup"><span data-stu-id="0ea05-142">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="0ea05-143">**Protégé** (4)</span><span class="sxs-lookup"><span data-stu-id="0ea05-143">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="0ea05-144">**Unblindée** (5)</span><span class="sxs-lookup"><span data-stu-id="0ea05-144">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="0ea05-145">**SCSI (A) High-Density (50 broches)** (6)</span><span class="sxs-lookup"><span data-stu-id="0ea05-145">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="0ea05-146">**SCSI (A) Low-Density (pin 50)** (7)</span><span class="sxs-lookup"><span data-stu-id="0ea05-146">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="0ea05-147">**SCSI (P) High-Density (68 broches)** (8)</span><span class="sxs-lookup"><span data-stu-id="0ea05-147">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="0ea05-148">**SCSI SCA-I (80 broches)** (9)</span><span class="sxs-lookup"><span data-stu-id="0ea05-148">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="0ea05-149">**SCSI SCA-II (80 broches)** (10)</span><span class="sxs-lookup"><span data-stu-id="0ea05-149">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="0ea05-150">**Fibre Channel SCSI (DB-9, cuivre)** (11)</span><span class="sxs-lookup"><span data-stu-id="0ea05-150">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="0ea05-151">**Fibre Channel SCSI (fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="0ea05-151">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="0ea05-152">**SCSI Fibre Channel SCA-II (40 broches)** (13)</span><span class="sxs-lookup"><span data-stu-id="0ea05-152">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="0ea05-153">**SCSI Fibre Channel SCA-II (20 broches)** (14)</span><span class="sxs-lookup"><span data-stu-id="0ea05-153">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="0ea05-154">**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="0ea05-154">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="0ea05-155">**ATA 3-1/2 pouces (40 broches)** (16)</span><span class="sxs-lookup"><span data-stu-id="0ea05-155">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="0ea05-156">**ATA 2-1/2 pouces (44 broches)** (17)</span><span class="sxs-lookup"><span data-stu-id="0ea05-156">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="0ea05-157">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="0ea05-157">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="0ea05-158">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="0ea05-158">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="0ea05-159">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="0ea05-159">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="0ea05-160">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="0ea05-160">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="0ea05-161">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="0ea05-161">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="0ea05-162">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="0ea05-162">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="0ea05-163">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="0ea05-163">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="0ea05-164">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="0ea05-164">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="0ea05-165">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="0ea05-165">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="0ea05-166">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="0ea05-166">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="0ea05-167">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="0ea05-167">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="0ea05-168">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="0ea05-168">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="0ea05-169">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="0ea05-169">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="0ea05-170">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="0ea05-170">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="0ea05-171">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="0ea05-171">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="0ea05-172">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="0ea05-172">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="0ea05-173">**UTP catégorie 3** (34)</span><span class="sxs-lookup"><span data-stu-id="0ea05-173">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="0ea05-174">**UTP catégorie 4** (35)</span><span class="sxs-lookup"><span data-stu-id="0ea05-174">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="0ea05-175">**UTP catégorie 5** (36)</span><span class="sxs-lookup"><span data-stu-id="0ea05-175">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="0ea05-176">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="0ea05-176">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="0ea05-177">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="0ea05-177">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="0ea05-178">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="0ea05-178">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="0ea05-179">**Fibre optique** (40)</span><span class="sxs-lookup"><span data-stu-id="0ea05-179">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="0ea05-180">**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="0ea05-180">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="0ea05-181">**Port Apple** (42)</span><span class="sxs-lookup"><span data-stu-id="0ea05-181">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="0ea05-182">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="0ea05-182">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="0ea05-183">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="0ea05-183">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="0ea05-184">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="0ea05-184">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="0ea05-185">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="0ea05-185">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="0ea05-186">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="0ea05-186">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="0ea05-187">**PCMCIA, type I** (48)</span><span class="sxs-lookup"><span data-stu-id="0ea05-187">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="0ea05-188">**PCMCIA type II** (49)</span><span class="sxs-lookup"><span data-stu-id="0ea05-188">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="0ea05-189">**PCMCIA type III** (50)</span><span class="sxs-lookup"><span data-stu-id="0ea05-189">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="0ea05-190">**Port ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="0ea05-190">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="0ea05-191">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="0ea05-191">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="0ea05-192">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="0ea05-192">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="0ea05-193">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="0ea05-193">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="0ea05-194">**HIPPA** (55)</span><span class="sxs-lookup"><span data-stu-id="0ea05-194">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="0ea05-195">**HSSDC (6 broches)** (56)</span><span class="sxs-lookup"><span data-stu-id="0ea05-195">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="0ea05-196">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="0ea05-196">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="0ea05-197">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="0ea05-197">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="0ea05-198">**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="0ea05-198">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="0ea05-199">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="0ea05-199">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="0ea05-200">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="0ea05-200">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="0ea05-201">**Infrarouge** (62)</span><span class="sxs-lookup"><span data-stu-id="0ea05-201">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="0ea05-202">**HP-HIL** (63)</span><span class="sxs-lookup"><span data-stu-id="0ea05-202">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="0ea05-203">**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="0ea05-203">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="0ea05-204">**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="0ea05-204">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="0ea05-205">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="0ea05-205">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="0ea05-206">**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="0ea05-206">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="0ea05-207">**Type Mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="0ea05-207">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="0ea05-208">**Mini-Centronics type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="0ea05-208">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="0ea05-209">**Mini-Centronics type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="0ea05-209">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="0ea05-210">**Souris bus** (71)</span><span class="sxs-lookup"><span data-stu-id="0ea05-210">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="0ea05-211">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="0ea05-211">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="0ea05-212">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="0ea05-212">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="0ea05-213">**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="0ea05-213">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="0ea05-214">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="0ea05-214">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="0ea05-215">**Propriétaire** (76)</span><span class="sxs-lookup"><span data-stu-id="0ea05-215">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="0ea05-216">**Emplacement de la carte de processeur propriétaire** (77)</span><span class="sxs-lookup"><span data-stu-id="0ea05-216">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="0ea05-217">**Emplacement de carte mémoire propriétaire** (78)</span><span class="sxs-lookup"><span data-stu-id="0ea05-217">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="0ea05-218">**Emplacement de la carte de montage des e/s propriétaire** (79)</span><span class="sxs-lookup"><span data-stu-id="0ea05-218">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="0ea05-219">**PCI-66 MHz** (80)</span><span class="sxs-lookup"><span data-stu-id="0ea05-219">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="0ea05-220">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="0ea05-220">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="0ea05-221">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="0ea05-221">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="0ea05-222">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="0ea05-222">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="0ea05-223">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="0ea05-223">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="0ea05-224">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="0ea05-224">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="0ea05-225">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="0ea05-225">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="0ea05-226">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="0ea05-226">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="0ea05-227">**PCI-X** (88)</span><span class="sxs-lookup"><span data-stu-id="0ea05-227">**PCI-X** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="0ea05-228">**SBus IEEE 1396-1993 32 bits** (89)</span><span class="sxs-lookup"><span data-stu-id="0ea05-228">**Sbus IEEE 1396-1993 32 bit** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="0ea05-229">**SBus IEEE 1396-1993 64 bits** (90)</span><span class="sxs-lookup"><span data-stu-id="0ea05-229">**Sbus IEEE 1396-1993 64 bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="0ea05-230">**MCA** (91)</span><span class="sxs-lookup"><span data-stu-id="0ea05-230">**MCA** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="0ea05-231">**Gio** (92)</span><span class="sxs-lookup"><span data-stu-id="0ea05-231">**GIO** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="0ea05-232">**XIO** (93)</span><span class="sxs-lookup"><span data-stu-id="0ea05-232">**XIO** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="0ea05-233">**HIO** (94)</span><span class="sxs-lookup"><span data-stu-id="0ea05-233">**HIO** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="0ea05-234">**NGIO** (95)</span><span class="sxs-lookup"><span data-stu-id="0ea05-234">**NGIO** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="0ea05-235">**PMC** (96)</span><span class="sxs-lookup"><span data-stu-id="0ea05-235">**PMC** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="0ea05-236">**E/s futures** (97)</span><span class="sxs-lookup"><span data-stu-id="0ea05-236">**Future I/O** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="0ea05-237">**InfiniBand** (98)</span><span class="sxs-lookup"><span data-stu-id="0ea05-237">**InfiniBand** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

<span data-ttu-id="0ea05-238">**AGP8X** (99)</span><span class="sxs-lookup"><span data-stu-id="0ea05-238">**AGP8X** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

<span data-ttu-id="0ea05-239">**PCI-E** (100)</span><span class="sxs-lookup"><span data-stu-id="0ea05-239">**PCI-E** (100)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ea05-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0ea05-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-243">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0ea05-243">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-244">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0ea05-244">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0ea05-245">Lorsqu’elle est utilisée avec les autres propriétés de clé d’une classe, cette propriété permet d’identifier toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-245">When used with the other key properties of a class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="0ea05-246">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-246">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-247">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="0ea05-247">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-248">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ea05-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-250">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| Current usage")</span><span class="sxs-lookup"><span data-stu-id="0ea05-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Current Usage")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-251">État de l’utilisation de l’emplacement système.</span><span class="sxs-lookup"><span data-stu-id="0ea05-251">Status of system slot use.</span></span>

<span data-ttu-id="0ea05-252">Cette valeur provient du membre d' **utilisation actuel** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-252">This value comes from the **Current Usage** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-253">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="0ea05-253">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="0ea05-254">**Réservé** (0)</span><span class="sxs-lookup"><span data-stu-id="0ea05-254">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0ea05-255">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0ea05-255">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ea05-256">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0ea05-256">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="0ea05-257">**Disponible** (3)</span><span class="sxs-lookup"><span data-stu-id="0ea05-257">**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

<span data-ttu-id="0ea05-258">**En cours d’utilisation** (4)</span><span class="sxs-lookup"><span data-stu-id="0ea05-258">**In use** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ea05-259">**Description**</span><span class="sxs-lookup"><span data-stu-id="0ea05-259">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-262">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0ea05-262">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-263">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0ea05-263">Description of the object.</span></span>

<span data-ttu-id="0ea05-264">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-264">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-265">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="0ea05-265">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-266">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ea05-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-268">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| Device Number")</span><span class="sxs-lookup"><span data-stu-id="0ea05-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Device Number")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-269">Numéro d’appareil SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-269">SMBIOS Device Number.</span></span>

<span data-ttu-id="0ea05-270">Cette valeur provient du membre du numéro de l' **appareil ou** de la fonction de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-270">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-271">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="0ea05-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-272">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="0ea05-272">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-273">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ea05-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-275">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| Function Number")</span><span class="sxs-lookup"><span data-stu-id="0ea05-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Function Number")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-276">Numéro de fonction SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-276">SMBIOS Function Number.</span></span>

<span data-ttu-id="0ea05-277">Cette valeur provient du membre du numéro de l' **appareil ou** de la fonction de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-277">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-278">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="0ea05-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-279">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="0ea05-279">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-280">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="0ea05-280">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-282">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-282">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-283">Hauteur maximale d’une carte d’adaptateur pouvant être insérée dans l’emplacement, en pouces.</span><span class="sxs-lookup"><span data-stu-id="0ea05-283">Maximum height of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="0ea05-284">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-284">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-285">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0ea05-285">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-286">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0ea05-286">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-288">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0ea05-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-289">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0ea05-289">Date and time the object is installed.</span></span> <span data-ttu-id="0ea05-290">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="0ea05-290">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0ea05-291">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-292">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="0ea05-292">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-293">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="0ea05-293">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-295">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-295">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-296">Longueur maximale d’une carte d’adaptateur pouvant être insérée dans l’emplacement, en pouces.</span><span class="sxs-lookup"><span data-stu-id="0ea05-296">Maximum length of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="0ea05-297">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-297">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-298">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="0ea05-298">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-301">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0ea05-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-302">Nom de l’organisation qui produit l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-302">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="0ea05-303">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-303">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-304">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="0ea05-304">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-305">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ea05-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-307">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Emplacement système DMTF \| 004,3 "), [**unités**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="0ea05-307">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-308">Largeur de bus maximale des cartes réseau qui peuvent être insérées dans cet emplacement, en bits.</span><span class="sxs-lookup"><span data-stu-id="0ea05-308">Maximum bus width of adapter cards that can be inserted into this slot—in bits.</span></span> <span data-ttu-id="0ea05-309">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ea05-309">This can be one of the following values.</span></span>

<span data-ttu-id="0ea05-310">Cette valeur provient du membre de la **largeur du bus de données** de l’emplacement de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-310">This value comes from the **Slot Data Bus Width** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-311">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-311">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="0ea05-312">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="0ea05-312">The possible values are.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="0ea05-313"><span id="8"></span>**8** (0)</span><span class="sxs-lookup"><span data-stu-id="0ea05-313"><span id="8"></span>**8** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0ea05-314">Largeur maximale des données (bits) : 8</span><span class="sxs-lookup"><span data-stu-id="0ea05-314">Maximum data width (bits): 8</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="0ea05-315"><span id="16"></span>**16** (1)</span><span class="sxs-lookup"><span data-stu-id="0ea05-315"><span id="16"></span>**16** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0ea05-316">Largeur maximale des données (bits) : 16</span><span class="sxs-lookup"><span data-stu-id="0ea05-316">Maximum data width (bits): 16</span></span>

</dd> <dt>

<span id="32"></span>

<span data-ttu-id="0ea05-317"><span id="32"></span>**32** (2)</span><span class="sxs-lookup"><span data-stu-id="0ea05-317"><span id="32"></span>**32** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0ea05-318">Largeur maximale des données (bits) : 32</span><span class="sxs-lookup"><span data-stu-id="0ea05-318">Maximum data width (bits): 32</span></span>

</dd> <dt>

<span id="64"></span>

<span data-ttu-id="0ea05-319"><span id="64"></span>**64** (3)</span><span class="sxs-lookup"><span data-stu-id="0ea05-319"><span id="64"></span>**64** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0ea05-320">Largeur maximale des données (bits) : 64</span><span class="sxs-lookup"><span data-stu-id="0ea05-320">Maximum data width (bits): 64</span></span>

</dd> <dt>

<span id="128"></span>

<span data-ttu-id="0ea05-321"><span id="128"></span>**128** (4)</span><span class="sxs-lookup"><span data-stu-id="0ea05-321"><span id="128"></span>**128** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0ea05-322">Largeur maximale des données (bits) : 128</span><span class="sxs-lookup"><span data-stu-id="0ea05-322">Maximum data width (bits): 128</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ea05-323">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="0ea05-323">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-326">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0ea05-326">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-327">Nom de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-327">Name for the physical element.</span></span>

<span data-ttu-id="0ea05-328">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-328">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-329">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0ea05-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-332">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0ea05-332">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-333">Étiquette de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0ea05-333">Label for the object.</span></span> <span data-ttu-id="0ea05-334">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0ea05-334">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0ea05-335">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-336">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0ea05-336">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-337">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ea05-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-339">Numéro d’emplacement physique qui peut être utilisé comme index dans une table d’emplacements système, que cet emplacement soit ou non physiquement vide.</span><span class="sxs-lookup"><span data-stu-id="0ea05-339">Physical slot number that can be used as an index into a system slot table, whether or not that slot is physically empty.</span></span>

<span data-ttu-id="0ea05-340">Cette valeur provient du membre **ID d’emplacement** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-340">This value comes from the **Slot ID** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-341">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-341">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0ea05-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-345">Données supplémentaires (autrement dit, plus que les informations sur les balises de ressource) qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-345">Additional data (that is, more than the asset tag information), that can be used to identify a physical element.</span></span> <span data-ttu-id="0ea05-346">Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="0ea05-346">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="0ea05-347">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques ou peuvent être utilisées comme clé d’élément, cette propriété a la **valeur null** et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="0ea05-347">Note that if only bar code data is available, and it is unique or can be used as an element key, this property is **NULL**, and the bar code data is used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="0ea05-348">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-348">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-349">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="0ea05-349">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-352">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0ea05-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-353">Numéro de référence que le producteur ou le fabricant attribue à l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-353">Part number that the producer or manufacturer assigns to the physical element.</span></span>

<span data-ttu-id="0ea05-354">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-355">**PMESignal**</span><span class="sxs-lookup"><span data-stu-id="0ea05-355">**PMESignal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-356">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0ea05-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-358">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| slot CARACTERISTIQUES 2")</span><span class="sxs-lookup"><span data-stu-id="0ea05-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 2")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-359">Si la **valeur est true**, le signal de gestion de l’alimentation du bus PCI activé (PME) est pris en charge par cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="0ea05-359">If **TRUE**, the PCI bus Power Management Enabled (PME) signal is supported by this slot.</span></span>

<span data-ttu-id="0ea05-360">Cette valeur provient du membre des caractéristiques de l' **emplacement 2** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-360">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-361">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="0ea05-361">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-362">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0ea05-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-364">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="0ea05-364">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="0ea05-365">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-365">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-366">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="0ea05-366">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-369">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ emplacement CIM**](cim-slot.md).**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="0ea05-369">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-370">Chaîne de forme libre qui décrit comment cet emplacement est physiquement unique et peut contenir des types de matériel spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0ea05-370">Free-form string that describes how this slot is physically unique and may hold special types of hardware.</span></span> <span data-ttu-id="0ea05-371">Cette propriété n’a de signification que lorsque la propriété correspondante **SpecialPurpose** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="0ea05-371">This property only has meaning when the corresponding property **SpecialPurpose** is **TRUE**.</span></span>

<span data-ttu-id="0ea05-372">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-372">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-373">**SegmentGroupNumber**</span><span class="sxs-lookup"><span data-stu-id="0ea05-373">**SegmentGroupNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-374">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ea05-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-376">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| segment Group Number")</span><span class="sxs-lookup"><span data-stu-id="0ea05-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Segment Group Number")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-377">Numéro de groupe de segments SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-377">SMBIOS Segment Group Number.</span></span>

<span data-ttu-id="0ea05-378">Cette valeur provient du membre de **numéro de groupe de segments** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-378">This value comes from the **Segment Group Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-379">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="0ea05-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-380">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0ea05-380">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-383">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0ea05-383">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-384">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-384">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="0ea05-385">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-385">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-386">**Partagé**</span><span class="sxs-lookup"><span data-stu-id="0ea05-386">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-387">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0ea05-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-389">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| slot characteristics 1")</span><span class="sxs-lookup"><span data-stu-id="0ea05-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 1")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-390">Si la **valeur est true**, deux ou plusieurs emplacements partagent un emplacement sur la carte de site, tel qu’un emplacement partagé PCI/EISA.</span><span class="sxs-lookup"><span data-stu-id="0ea05-390">If **TRUE**, two or more slots share a location on the baseboard, such as a PCI/EISA shared slot.</span></span>

<span data-ttu-id="0ea05-391">Cette valeur provient du membre des caractéristiques de l' **emplacement 1** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-391">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-392">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="0ea05-392">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-393">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-395">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0ea05-395">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-396">Numéro de point de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-396">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="0ea05-397">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-397">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-398">**SlotDesignation**</span><span class="sxs-lookup"><span data-stu-id="0ea05-398">**SlotDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-399">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-401">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 9 \| slot désignation")</span><span class="sxs-lookup"><span data-stu-id="0ea05-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Designation")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-402">Chaîne SMBIOS qui identifie la désignation de l’emplacement système de l’emplacement sur la carte mère.</span><span class="sxs-lookup"><span data-stu-id="0ea05-402">SMBIOS string that identifies the system slot designation of the slot on the motherboard.</span></span>

<span data-ttu-id="0ea05-403">Exemple : « PCI-1 »</span><span class="sxs-lookup"><span data-stu-id="0ea05-403">Example: "PCI-1"</span></span>

<span data-ttu-id="0ea05-404">Cette valeur provient du membre de **désignation d’emplacement** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-404">This value comes from the **Slot Designation** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-405">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="0ea05-405">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-406">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0ea05-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-408">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ emplacement CIM**](cim-slot.md).**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="0ea05-408">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-409">Si la **valeur est true**, cet emplacement est physiquement unique et peut contenir des types de matériel spéciaux, tels qu’un emplacement de processeur graphique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-409">If **TRUE**, this slot is physically unique and may hold special types of hardware, such as a graphics processor slot.</span></span> <span data-ttu-id="0ea05-410">Si la **valeur est true**, **PurposeDescription** doit spécifier la nature de l’unicité ou de l’objectif de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="0ea05-410">If **TRUE**, then **PurposeDescription** should specify the nature of the uniqueness or purpose of the slot.</span></span>

<span data-ttu-id="0ea05-411">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-411">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-412">**État**</span><span class="sxs-lookup"><span data-stu-id="0ea05-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-413">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-415">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0ea05-415">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-416">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0ea05-416">Current status of the object.</span></span> <span data-ttu-id="0ea05-417">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0ea05-417">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0ea05-418">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0ea05-418">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0ea05-419">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0ea05-419">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0ea05-420">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0ea05-420">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0ea05-421">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0ea05-421">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0ea05-422">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0ea05-423">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="0ea05-423">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0ea05-424">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-424">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0ea05-425">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-425">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0ea05-426">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-426">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ea05-427">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0ea05-427">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0ea05-428">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-428">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0ea05-429">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-429">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0ea05-430">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-430">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0ea05-431">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-431">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0ea05-432">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-432">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0ea05-433">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-433">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0ea05-434">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-434">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0ea05-435">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0ea05-435">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ea05-436">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="0ea05-436">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-437">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0ea05-437">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-438">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-439">Si la **valeur est true**, l’emplacement prend en charge la connexion à chaud des cartes d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="0ea05-439">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

<span data-ttu-id="0ea05-440">Cette valeur provient du membre des caractéristiques de l' **emplacement 2** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-440">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-441">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-441">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-442">**Tag**</span><span class="sxs-lookup"><span data-stu-id="0ea05-442">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-445">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0ea05-445">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-446">Emplacement système représenté par une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0ea05-446">System slot represented by an instance of this class.</span></span>

<span data-ttu-id="0ea05-447">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="0ea05-448">Exemple : « emplacement système 1 »</span><span class="sxs-lookup"><span data-stu-id="0ea05-448">Example: "System Slot 1"</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-449">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="0ea05-449">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-450">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ea05-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-452">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Emplacement système DMTF \| 004,11 "), [**unités**](../wmisdk/standard-qualifiers.md) (" milliwatts ")</span><span class="sxs-lookup"><span data-stu-id="0ea05-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-453">Dissipation thermique maximale de l’emplacement en milliwatts.</span><span class="sxs-lookup"><span data-stu-id="0ea05-453">Maximum thermal dissipation of the slot in milliwatts.</span></span>

<span data-ttu-id="0ea05-454">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-454">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-455">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="0ea05-455">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-456">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ea05-456">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-458">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Emplacement système DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="0ea05-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-459">Tableau d’entiers énumérés indiquant la tension Vcc prise en charge par cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="0ea05-459">Array of enumerated integers indicating the Vcc voltage supported by this slot.</span></span>

<span data-ttu-id="0ea05-460">Cette valeur provient du membre des caractéristiques de l' **emplacement 1** de la structure des **emplacements système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0ea05-460">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0ea05-461">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-461">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="0ea05-462">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="0ea05-462">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ea05-463">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0ea05-463">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0ea05-464">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0ea05-464">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="0ea05-465">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="0ea05-465">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="0ea05-466">**5 v** (3)</span><span class="sxs-lookup"><span data-stu-id="0ea05-466">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ea05-467">**Version**</span><span class="sxs-lookup"><span data-stu-id="0ea05-467">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-468">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ea05-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-470">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0ea05-470">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-471">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0ea05-471">Version of the physical element.</span></span>

<span data-ttu-id="0ea05-472">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-472">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ea05-473">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="0ea05-473">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ea05-474">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ea05-474">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ea05-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ea05-476">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Emplacement système DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="0ea05-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="0ea05-477">Tableau d’entiers énumérés indiquant la tension VPP prise en charge par cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="0ea05-477">Array of enumerated integers indicating the Vpp voltage supported by this slot.</span></span>

<span data-ttu-id="0ea05-478">Cette propriété est héritée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-478">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="0ea05-479">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="0ea05-479">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ea05-480">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0ea05-480">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0ea05-481">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0ea05-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="0ea05-482">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="0ea05-482">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="0ea05-483">**5 v** (3)</span><span class="sxs-lookup"><span data-stu-id="0ea05-483">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="0ea05-484">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="0ea05-484">**12V** (4)</span></span>


<span data-ttu-id="0ea05-485"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0ea05-485"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0ea05-486">Notes</span><span class="sxs-lookup"><span data-stu-id="0ea05-486">Remarks</span></span>

<span data-ttu-id="0ea05-487">La classe **Win32 \_ SystemSlot** est dérivée de l' [**\_ emplacement CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="0ea05-487">The **Win32\_SystemSlot** class is derived from [**CIM\_Slot**](cim-slot.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea05-488">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ea05-488">Requirements</span></span>



| <span data-ttu-id="0ea05-489">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ea05-489">Requirement</span></span> | <span data-ttu-id="0ea05-490">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ea05-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea05-491">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ea05-491">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea05-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ea05-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ea05-493">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ea05-493">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea05-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ea05-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ea05-495">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ea05-495">Namespace</span></span><br/>                | <span data-ttu-id="0ea05-496">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0ea05-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0ea05-497">MOF</span><span class="sxs-lookup"><span data-stu-id="0ea05-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ea05-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ea05-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ea05-499">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea05-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ea05-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ea05-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea05-501">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea05-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea05-502">**\_Emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="0ea05-502">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dt>

[<span data-ttu-id="0ea05-503">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0ea05-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
