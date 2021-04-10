---
description: La \_ classe WMI PortConnector WMI représente des ports de connexion physiques, tels que DB-25 pin mâle, Centronics ou PS/2.
ms.assetid: 85788d1d-0641-4dba-b4ae-a84eb6c4992a
ms.tgt_platform: multiple
title: Classe Win32_PortConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortConnector
- Win32_PortConnector.Caption
- Win32_PortConnector.ConnectorPinout
- Win32_PortConnector.ConnectorType
- Win32_PortConnector.CreationClassName
- Win32_PortConnector.Description
- Win32_PortConnector.ExternalReferenceDesignator
- Win32_PortConnector.InstallDate
- Win32_PortConnector.InternalReferenceDesignator
- Win32_PortConnector.Manufacturer
- Win32_PortConnector.Model
- Win32_PortConnector.Name
- Win32_PortConnector.OtherIdentifyingInfo
- Win32_PortConnector.PartNumber
- Win32_PortConnector.PortType
- Win32_PortConnector.PoweredOn
- Win32_PortConnector.SerialNumber
- Win32_PortConnector.SKU
- Win32_PortConnector.Status
- Win32_PortConnector.Tag
- Win32_PortConnector.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcf9eea51d3a65ad07879cca3e47ae79bde92d53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200887"
---
# <a name="win32_portconnector-class"></a><span data-ttu-id="b17aa-103">\_Classe PortConnector Win32</span><span class="sxs-lookup"><span data-stu-id="b17aa-103">Win32\_PortConnector class</span></span>

<span data-ttu-id="b17aa-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortConnector** WMI représente des ports de connexion physiques, tels que DB-25 pin mâle, Centronics ou PS/2.</span><span class="sxs-lookup"><span data-stu-id="b17aa-104">The **Win32\_PortConnector** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection ports, such as DB-25 pin male, Centronics, or PS/2.</span></span>

<span data-ttu-id="b17aa-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b17aa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b17aa-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b17aa-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17aa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b17aa-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B92-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortConnector : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  string   ExternalReferenceDesignator;
  datetime InstallDate;
  string   InternalReferenceDesignator;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint16   PortType;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="b17aa-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b17aa-108">Members</span></span>

<span data-ttu-id="b17aa-109">La classe **Win32 \_ PortConnector** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b17aa-109">The **Win32\_PortConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="b17aa-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b17aa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b17aa-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b17aa-111">Properties</span></span>

<span data-ttu-id="b17aa-112">La classe **Win32 \_ PortConnector** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b17aa-112">The **Win32\_PortConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b17aa-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b17aa-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-116">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-117">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="b17aa-117">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="b17aa-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-119">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="b17aa-119">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-122">Configuration du code confidentiel et utilisation des signaux d’un connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-122">Pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="b17aa-123">Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-123">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-124">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="b17aa-124">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-125">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b17aa-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-127">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 8 \| Internal/External Connector type")</span><span class="sxs-lookup"><span data-stu-id="b17aa-127">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal/External Connector Type")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-128">Tableau d’attributs physiques du connecteur utilisé par ce port.</span><span class="sxs-lookup"><span data-stu-id="b17aa-128">Array of physical attributes of the connector used by this port.</span></span>

<span data-ttu-id="b17aa-129">Cette propriété est héritée de la [**\_ PhysicalConnector CIM**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-129">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span> <span data-ttu-id="b17aa-130">La liste suivante répertorie les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b17aa-130">The following list lists the values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b17aa-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="b17aa-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b17aa-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="b17aa-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="b17aa-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Mâle** (2)</span><span class="sxs-lookup"><span data-stu-id="b17aa-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="b17aa-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Femme** (3)</span><span class="sxs-lookup"><span data-stu-id="b17aa-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="b17aa-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Protégé** (4)</span><span class="sxs-lookup"><span data-stu-id="b17aa-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="b17aa-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unblindée** (5)</span><span class="sxs-lookup"><span data-stu-id="b17aa-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="b17aa-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 broches)** (6)</span><span class="sxs-lookup"><span data-stu-id="b17aa-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="b17aa-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (pin 50)** (7)</span><span class="sxs-lookup"><span data-stu-id="b17aa-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="b17aa-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 broches)** (8)</span><span class="sxs-lookup"><span data-stu-id="b17aa-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="b17aa-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 broches)** (9)</span><span class="sxs-lookup"><span data-stu-id="b17aa-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="b17aa-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 broches)** (10)</span><span class="sxs-lookup"><span data-stu-id="b17aa-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="b17aa-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**Fibre Channel SCSI (DB-9, cuivre)** (11)</span><span class="sxs-lookup"><span data-stu-id="b17aa-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="b17aa-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**Fibre Channel SCSI (fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="b17aa-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="b17aa-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 broches)** (13)</span><span class="sxs-lookup"><span data-stu-id="b17aa-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="b17aa-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 broches)** (14)</span><span class="sxs-lookup"><span data-stu-id="b17aa-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="b17aa-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="b17aa-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="b17aa-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 pouces (40 broches)** (16)</span><span class="sxs-lookup"><span data-stu-id="b17aa-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="b17aa-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 pouces (44 broches)** (17)</span><span class="sxs-lookup"><span data-stu-id="b17aa-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="b17aa-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="b17aa-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="b17aa-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="b17aa-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="b17aa-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="b17aa-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="b17aa-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="b17aa-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="b17aa-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="b17aa-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="b17aa-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="b17aa-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="b17aa-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="b17aa-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="b17aa-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="b17aa-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="b17aa-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="b17aa-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="b17aa-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="b17aa-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="b17aa-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="b17aa-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="b17aa-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="b17aa-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="b17aa-161"><span id="v.35"></span>**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="b17aa-161"><span id="v.35"></span>**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="b17aa-162"><span id="x.21"></span>**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="b17aa-162"><span id="x.21"></span>**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="b17aa-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="b17aa-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="b17aa-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="b17aa-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="b17aa-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP catégorie 3** (34)</span><span class="sxs-lookup"><span data-stu-id="b17aa-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="b17aa-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP catégorie 4** (35)</span><span class="sxs-lookup"><span data-stu-id="b17aa-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="b17aa-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP catégorie 5** (36)</span><span class="sxs-lookup"><span data-stu-id="b17aa-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="b17aa-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="b17aa-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="b17aa-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="b17aa-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="b17aa-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="b17aa-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="b17aa-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fibre optique** (40)</span><span class="sxs-lookup"><span data-stu-id="b17aa-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="b17aa-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="b17aa-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="b17aa-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Port Apple** (42)</span><span class="sxs-lookup"><span data-stu-id="b17aa-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="b17aa-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="b17aa-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="b17aa-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="b17aa-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="b17aa-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="b17aa-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="b17aa-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="b17aa-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="b17aa-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="b17aa-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="b17aa-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA, type I** (48)</span><span class="sxs-lookup"><span data-stu-id="b17aa-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="b17aa-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA type II** (49)</span><span class="sxs-lookup"><span data-stu-id="b17aa-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="b17aa-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA type III** (50)</span><span class="sxs-lookup"><span data-stu-id="b17aa-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="b17aa-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**Port ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="b17aa-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="b17aa-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="b17aa-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="b17aa-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="b17aa-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="b17aa-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="b17aa-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="b17aa-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPA** (55)</span><span class="sxs-lookup"><span data-stu-id="b17aa-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="b17aa-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 broches)** (56)</span><span class="sxs-lookup"><span data-stu-id="b17aa-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="b17aa-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="b17aa-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="b17aa-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="b17aa-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="b17aa-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="b17aa-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="b17aa-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="b17aa-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="b17aa-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="b17aa-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="b17aa-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarouge** (62)</span><span class="sxs-lookup"><span data-stu-id="b17aa-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="b17aa-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span><span class="sxs-lookup"><span data-stu-id="b17aa-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="b17aa-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="b17aa-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="b17aa-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="b17aa-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="b17aa-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="b17aa-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="b17aa-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="b17aa-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="b17aa-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Type Mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="b17aa-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="b17aa-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="b17aa-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="b17aa-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="b17aa-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="b17aa-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Souris bus** (71)</span><span class="sxs-lookup"><span data-stu-id="b17aa-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="b17aa-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="b17aa-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="b17aa-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="b17aa-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="b17aa-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="b17aa-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="b17aa-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="b17aa-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="b17aa-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Propriétaire** (76)</span><span class="sxs-lookup"><span data-stu-id="b17aa-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="b17aa-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Emplacement de la carte de processeur propriétaire** (77)</span><span class="sxs-lookup"><span data-stu-id="b17aa-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="b17aa-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Emplacement de carte mémoire propriétaire** (78)</span><span class="sxs-lookup"><span data-stu-id="b17aa-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="b17aa-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Emplacement de la carte de montage des e/s propriétaire** (79)</span><span class="sxs-lookup"><span data-stu-id="b17aa-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="b17aa-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66 MHz** (80)</span><span class="sxs-lookup"><span data-stu-id="b17aa-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="b17aa-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="b17aa-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="b17aa-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="b17aa-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="b17aa-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="b17aa-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span data-ttu-id="b17aa-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="b17aa-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-216">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="b17aa-216">PC-98-Hireso</span></span>

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="b17aa-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="b17aa-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="b17aa-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="b17aa-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="b17aa-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="b17aa-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="b17aa-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-jack** (88)</span><span class="sxs-lookup"><span data-stu-id="b17aa-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-221">SCSI SSA</span><span class="sxs-lookup"><span data-stu-id="b17aa-221">SSA SCSI</span></span>

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span data-ttu-id="b17aa-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**Disquette sur carte** (89)</span><span class="sxs-lookup"><span data-stu-id="b17aa-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**On Board Floppy** (89)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-223">Circulaire</span><span class="sxs-lookup"><span data-stu-id="b17aa-223">Circular</span></span>

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span data-ttu-id="b17aa-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 pin double inline (broche 10 coupées)** (90)</span><span class="sxs-lookup"><span data-stu-id="b17aa-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Pin Dual Inline (pin 10 cut)** (90)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-225">Connecteur IDE de la carte</span><span class="sxs-lookup"><span data-stu-id="b17aa-225">On Board IDE Connector</span></span>

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span data-ttu-id="b17aa-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 broches en ligne double (broche 26 coup)** (91)</span><span class="sxs-lookup"><span data-stu-id="b17aa-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (pin 26 cut)** (91)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-227">Connecteur de disquette sur carte</span><span class="sxs-lookup"><span data-stu-id="b17aa-227">On Board Floppy Connector</span></span>

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="b17aa-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 broche double Inline** (92)</span><span class="sxs-lookup"><span data-stu-id="b17aa-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-229">9 broches en double en ligne</span><span class="sxs-lookup"><span data-stu-id="b17aa-229">9 Pin Dual Inline</span></span>

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span data-ttu-id="b17aa-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 broche double Inline** (93)</span><span class="sxs-lookup"><span data-stu-id="b17aa-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-231">25 broche en double en ligne</span><span class="sxs-lookup"><span data-stu-id="b17aa-231">25 Pin Dual Inline</span></span>

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span data-ttu-id="b17aa-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**Entrée audio à la carte à partir du CD-ROM** (94)</span><span class="sxs-lookup"><span data-stu-id="b17aa-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**On Board Sound Input from CD-ROM** (94)</span></span>


</dt> <dd>

<span data-ttu-id="b17aa-233">50 pin double Inline</span><span class="sxs-lookup"><span data-stu-id="b17aa-233">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-234">95</span><span class="sxs-lookup"><span data-stu-id="b17aa-234">95</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-235">68 pin double Inline</span><span class="sxs-lookup"><span data-stu-id="b17aa-235">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-236">96</span><span class="sxs-lookup"><span data-stu-id="b17aa-236">96</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-237">Connecteur audio sur carte</span><span class="sxs-lookup"><span data-stu-id="b17aa-237">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-238">97</span><span class="sxs-lookup"><span data-stu-id="b17aa-238">97</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-239">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="b17aa-239">Mini-Jack</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-240">98</span><span class="sxs-lookup"><span data-stu-id="b17aa-240">98</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-241">PCI-X</span><span class="sxs-lookup"><span data-stu-id="b17aa-241">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-242">99</span><span class="sxs-lookup"><span data-stu-id="b17aa-242">99</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-243">SBus IEEE 1396-1993 32 bits</span><span class="sxs-lookup"><span data-stu-id="b17aa-243">Sbus IEEE 1396-1993 32 Bit</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-244">100</span><span class="sxs-lookup"><span data-stu-id="b17aa-244">100</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-245">SBus IEEE 1396-1993 64 bits</span><span class="sxs-lookup"><span data-stu-id="b17aa-245">Sbus IEEE 1396-1993 64 Bit</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-246">101</span><span class="sxs-lookup"><span data-stu-id="b17aa-246">101</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-247">MCA</span><span class="sxs-lookup"><span data-stu-id="b17aa-247">MCA</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-248">102</span><span class="sxs-lookup"><span data-stu-id="b17aa-248">102</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-249">GIO</span><span class="sxs-lookup"><span data-stu-id="b17aa-249">GIO</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-250">103</span><span class="sxs-lookup"><span data-stu-id="b17aa-250">103</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-251">XIO</span><span class="sxs-lookup"><span data-stu-id="b17aa-251">XIO</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-252">104</span><span class="sxs-lookup"><span data-stu-id="b17aa-252">104</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-253">HIO</span><span class="sxs-lookup"><span data-stu-id="b17aa-253">HIO</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-254">105</span><span class="sxs-lookup"><span data-stu-id="b17aa-254">105</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-255">NGIO</span><span class="sxs-lookup"><span data-stu-id="b17aa-255">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-256">106</span><span class="sxs-lookup"><span data-stu-id="b17aa-256">106</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-257">PMC</span><span class="sxs-lookup"><span data-stu-id="b17aa-257">PMC</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-258">107</span><span class="sxs-lookup"><span data-stu-id="b17aa-258">107</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-259">MTRJ</span><span class="sxs-lookup"><span data-stu-id="b17aa-259">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-260">108</span><span class="sxs-lookup"><span data-stu-id="b17aa-260">108</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-261">VF-45</span><span class="sxs-lookup"><span data-stu-id="b17aa-261">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-262">109</span><span class="sxs-lookup"><span data-stu-id="b17aa-262">109</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-263">E/s futures</span><span class="sxs-lookup"><span data-stu-id="b17aa-263">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-264">110</span><span class="sxs-lookup"><span data-stu-id="b17aa-264">110</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-265">SC</span><span class="sxs-lookup"><span data-stu-id="b17aa-265">SC</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-266">111</span><span class="sxs-lookup"><span data-stu-id="b17aa-266">111</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-267">SG</span><span class="sxs-lookup"><span data-stu-id="b17aa-267">SG</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-268">112</span><span class="sxs-lookup"><span data-stu-id="b17aa-268">112</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-269">Electrical</span><span class="sxs-lookup"><span data-stu-id="b17aa-269">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-270">113</span><span class="sxs-lookup"><span data-stu-id="b17aa-270">113</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-271">Optique</span><span class="sxs-lookup"><span data-stu-id="b17aa-271">Optical</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-272">114</span><span class="sxs-lookup"><span data-stu-id="b17aa-272">114</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-273">Ruban</span><span class="sxs-lookup"><span data-stu-id="b17aa-273">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-274">115</span><span class="sxs-lookup"><span data-stu-id="b17aa-274">115</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-275">GLM</span><span class="sxs-lookup"><span data-stu-id="b17aa-275">GLM</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-276">116</span><span class="sxs-lookup"><span data-stu-id="b17aa-276">116</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-277">1x9</span><span class="sxs-lookup"><span data-stu-id="b17aa-277">1x9</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-278">117</span><span class="sxs-lookup"><span data-stu-id="b17aa-278">117</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-279">Mini SG</span><span class="sxs-lookup"><span data-stu-id="b17aa-279">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-280">118</span><span class="sxs-lookup"><span data-stu-id="b17aa-280">118</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-281">LC</span><span class="sxs-lookup"><span data-stu-id="b17aa-281">LC</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-282">119</span><span class="sxs-lookup"><span data-stu-id="b17aa-282">119</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-283">HSSC</span><span class="sxs-lookup"><span data-stu-id="b17aa-283">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-284">120</span><span class="sxs-lookup"><span data-stu-id="b17aa-284">120</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-285">VHDCI protégé (68 broches)</span><span class="sxs-lookup"><span data-stu-id="b17aa-285">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-286">121</span><span class="sxs-lookup"><span data-stu-id="b17aa-286">121</span></span>
</dt> <dd>

<span data-ttu-id="b17aa-287">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="b17aa-287">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b17aa-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b17aa-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-291">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b17aa-291">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-292">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="b17aa-292">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b17aa-293">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-293">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b17aa-294">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-294">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-295">**Description**</span><span class="sxs-lookup"><span data-stu-id="b17aa-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-298">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b17aa-298">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-299">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b17aa-299">Description of the object.</span></span>

<span data-ttu-id="b17aa-300">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-301">**ExternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="b17aa-301">**ExternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-304">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 8 \| External Reference désignateur")</span><span class="sxs-lookup"><span data-stu-id="b17aa-304">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|External Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-305">Indicateur de référence externe du port.</span><span class="sxs-lookup"><span data-stu-id="b17aa-305">External reference designator of the port.</span></span> <span data-ttu-id="b17aa-306">Les indicateurs de référence externe sont des identificateurs qui déterminent le type et l’utilisation du port.</span><span class="sxs-lookup"><span data-stu-id="b17aa-306">External reference designators are identifiers that determine the type and use of the port.</span></span>

<span data-ttu-id="b17aa-307">Exemple : « COM1 »</span><span class="sxs-lookup"><span data-stu-id="b17aa-307">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b17aa-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-309">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b17aa-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-311">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="b17aa-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-312">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b17aa-312">Date and time the object is installed.</span></span> <span data-ttu-id="b17aa-313">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="b17aa-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b17aa-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-315">**InternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="b17aa-315">**InternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-318">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 8 \| Internal Reference désignateur")</span><span class="sxs-lookup"><span data-stu-id="b17aa-318">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-319">Indicateur de référence interne du port.</span><span class="sxs-lookup"><span data-stu-id="b17aa-319">Internal reference designator of the port.</span></span> <span data-ttu-id="b17aa-320">Les indicateurs de référence internes sont spécifiques au fabricant et identifient l’emplacement du circuit ou l’utilisation du port.</span><span class="sxs-lookup"><span data-stu-id="b17aa-320">Internal reference designators are specific to the manufacturer, and identify the circuit board location or use of the port.</span></span>

<span data-ttu-id="b17aa-321">Exemple : « J101 »</span><span class="sxs-lookup"><span data-stu-id="b17aa-321">Example: "J101"</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-322">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="b17aa-322">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-323">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-325">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b17aa-325">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-326">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-326">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="b17aa-327">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-327">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-328">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="b17aa-328">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-331">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b17aa-331">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-332">Nom de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-332">Name for the physical element.</span></span>

<span data-ttu-id="b17aa-333">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-333">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-334">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b17aa-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-335">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-337">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b17aa-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-338">Étiquette de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b17aa-338">Label for the object.</span></span> <span data-ttu-id="b17aa-339">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="b17aa-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b17aa-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b17aa-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-344">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-344">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="b17aa-345">Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="b17aa-345">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="b17aa-346">Si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, cette propriété a la **valeur null** et les données de code-barres sont utilisées comme clé de classe dans la propriété de balise.</span><span class="sxs-lookup"><span data-stu-id="b17aa-346">If only bar code data is available and unique or able to be used as an element key, this property is **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="b17aa-347">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-347">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-348">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="b17aa-348">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-351">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b17aa-351">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-352">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-352">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="b17aa-353">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-353">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-354">**PortType**</span><span class="sxs-lookup"><span data-stu-id="b17aa-354">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-355">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b17aa-355">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-357">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 8 \| port type")</span><span class="sxs-lookup"><span data-stu-id="b17aa-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Port Type")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-358">Fonction du port.</span><span class="sxs-lookup"><span data-stu-id="b17aa-358">Function of the port.</span></span> <span data-ttu-id="b17aa-359">La liste suivante répertorie les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b17aa-359">The following list lists the values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b17aa-360">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="b17aa-360">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="b17aa-361">**Port parallèle XT/AT compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="b17aa-361">**Parallel Port XT/AT Compatible** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

<span data-ttu-id="b17aa-362">**Port parallèle PS/2** (2)</span><span class="sxs-lookup"><span data-stu-id="b17aa-362">**Parallel Port PS/2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

<span data-ttu-id="b17aa-363">**Port parallèle ECP** (3)</span><span class="sxs-lookup"><span data-stu-id="b17aa-363">**Parallel Port ECP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

<span data-ttu-id="b17aa-364">**Port parallèle EPP** (4)</span><span class="sxs-lookup"><span data-stu-id="b17aa-364">**Parallel Port EPP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

<span data-ttu-id="b17aa-365">**Port parallèle ECP/EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="b17aa-365">**Parallel Port ECP/EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="b17aa-366">**Port série à compatibilité XT/AT** (6)</span><span class="sxs-lookup"><span data-stu-id="b17aa-366">**Serial Port XT/AT Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

<span data-ttu-id="b17aa-367">**Port série 16450 compatible** (7)</span><span class="sxs-lookup"><span data-stu-id="b17aa-367">**Serial Port 16450 Compatible** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

<span data-ttu-id="b17aa-368">**Port série 16550 compatible** (8)</span><span class="sxs-lookup"><span data-stu-id="b17aa-368">**Serial Port 16550 Compatible** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

<span data-ttu-id="b17aa-369">**Port série 16550A compatible** (9)</span><span class="sxs-lookup"><span data-stu-id="b17aa-369">**Serial Port 16550A Compatible** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

<span data-ttu-id="b17aa-370">**Port SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="b17aa-370">**SCSI Port** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

<span data-ttu-id="b17aa-371">**Port MIDI** (11)</span><span class="sxs-lookup"><span data-stu-id="b17aa-371">**MIDI Port** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

<span data-ttu-id="b17aa-372">**Port de joie Stick** (12)</span><span class="sxs-lookup"><span data-stu-id="b17aa-372">**Joy Stick Port** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

<span data-ttu-id="b17aa-373">**Port clavier** (13)</span><span class="sxs-lookup"><span data-stu-id="b17aa-373">**Keyboard Port** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

<span data-ttu-id="b17aa-374">**Port de souris** (14)</span><span class="sxs-lookup"><span data-stu-id="b17aa-374">**Mouse Port** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="b17aa-375">**SCSI SSA** (15)</span><span class="sxs-lookup"><span data-stu-id="b17aa-375">**SSA SCSI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="b17aa-376">**USB** (16)</span><span class="sxs-lookup"><span data-stu-id="b17aa-376">**USB** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

<span data-ttu-id="b17aa-377">**FireWire (IEEE P1394)** (17)</span><span class="sxs-lookup"><span data-stu-id="b17aa-377">**FireWire (IEEE P1394)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="b17aa-378">**PCMCIA type II** (18)</span><span class="sxs-lookup"><span data-stu-id="b17aa-378">**PCMCIA Type II** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="b17aa-379">**PCMCIA type II** (19)</span><span class="sxs-lookup"><span data-stu-id="b17aa-379">**PCMCIA Type II** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="b17aa-380">**Type PCMCIA III** (20)</span><span class="sxs-lookup"><span data-stu-id="b17aa-380">**PCMCIA Type III** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="b17aa-381">**CardBus** (21)</span><span class="sxs-lookup"><span data-stu-id="b17aa-381">**Cardbus** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

<span data-ttu-id="b17aa-382">**Port du bus d’accès** (22)</span><span class="sxs-lookup"><span data-stu-id="b17aa-382">**Access Bus Port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

<span data-ttu-id="b17aa-383">**SCSI II** (23)</span><span class="sxs-lookup"><span data-stu-id="b17aa-383">**SCSI II** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

<span data-ttu-id="b17aa-384">**Largeur SCSI** (24)</span><span class="sxs-lookup"><span data-stu-id="b17aa-384">**SCSI Wide** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="b17aa-385">**PC-98** (25)</span><span class="sxs-lookup"><span data-stu-id="b17aa-385">**PC-98** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="b17aa-386">**PC-98-Hireso** (26)</span><span class="sxs-lookup"><span data-stu-id="b17aa-386">**PC-98-Hireso** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="b17aa-387">**PC-H98** (27)</span><span class="sxs-lookup"><span data-stu-id="b17aa-387">**PC-H98** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

<span data-ttu-id="b17aa-388">**Port vidéo** (28)</span><span class="sxs-lookup"><span data-stu-id="b17aa-388">**Video Port** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

<span data-ttu-id="b17aa-389">**Port audio** (29)</span><span class="sxs-lookup"><span data-stu-id="b17aa-389">**Audio Port** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

<span data-ttu-id="b17aa-390">**Port du modem** (30)</span><span class="sxs-lookup"><span data-stu-id="b17aa-390">**Modem Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

<span data-ttu-id="b17aa-391">**Port réseau** (31)</span><span class="sxs-lookup"><span data-stu-id="b17aa-391">**Network Port** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="b17aa-392">**Compatible 8251** (32)</span><span class="sxs-lookup"><span data-stu-id="b17aa-392">**8251 Compatible** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

<span data-ttu-id="b17aa-393">**8251 compatible FIFO** (33)</span><span class="sxs-lookup"><span data-stu-id="b17aa-393">**8251 FIFO Compatible** (33)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b17aa-394">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="b17aa-394">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-395">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b17aa-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-397">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="b17aa-397">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="b17aa-398">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-398">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-399">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b17aa-399">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-401">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-402">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b17aa-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-403">Numéro alloué par le fabricant utilisé pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-403">Manufacturer-allocated number used to identify a physical element.</span></span>

<span data-ttu-id="b17aa-404">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-404">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-405">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="b17aa-405">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-408">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b17aa-408">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-409">Numéro d’unité de conservation de stock pour un élément physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-409">Stock keeping unit number for a physical element.</span></span>

<span data-ttu-id="b17aa-410">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-410">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-411">**État**</span><span class="sxs-lookup"><span data-stu-id="b17aa-411">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-412">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-414">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b17aa-414">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-415">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b17aa-415">Current status of the object.</span></span> <span data-ttu-id="b17aa-416">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="b17aa-416">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b17aa-417">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="b17aa-417">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b17aa-418">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="b17aa-418">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b17aa-419">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="b17aa-419">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b17aa-420">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="b17aa-420">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b17aa-421">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b17aa-422">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b17aa-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b17aa-423">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b17aa-424">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b17aa-425">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b17aa-426">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="b17aa-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b17aa-427">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b17aa-428">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b17aa-429">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b17aa-430">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b17aa-431">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b17aa-432">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b17aa-433">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b17aa-434">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="b17aa-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b17aa-435">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b17aa-435">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-438">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b17aa-438">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-439">Identificateur unique d’une connexion de port sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-439">Unique identifier of a port connection on the computer system.</span></span>

<span data-ttu-id="b17aa-440">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-440">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="b17aa-441">Exemple : « connecteur de port 1 »</span><span class="sxs-lookup"><span data-stu-id="b17aa-441">Example: "Port Connector 1"</span></span>

</dd> <dt>

<span data-ttu-id="b17aa-442">**Version**</span><span class="sxs-lookup"><span data-stu-id="b17aa-442">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17aa-443">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b17aa-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b17aa-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b17aa-445">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b17aa-445">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b17aa-446">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b17aa-446">Version of the physical element.</span></span>

<span data-ttu-id="b17aa-447">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b17aa-448">Notes</span><span class="sxs-lookup"><span data-stu-id="b17aa-448">Remarks</span></span>

<span data-ttu-id="b17aa-449">La classe **Win32 \_ PortConnector** est dérivée de [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="b17aa-449">The **Win32\_PortConnector** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b17aa-450">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b17aa-450">Requirements</span></span>



| <span data-ttu-id="b17aa-451">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b17aa-451">Requirement</span></span> | <span data-ttu-id="b17aa-452">Valeur</span><span class="sxs-lookup"><span data-stu-id="b17aa-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b17aa-453">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17aa-453">Minimum supported client</span></span><br/> | <span data-ttu-id="b17aa-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b17aa-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b17aa-455">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17aa-455">Minimum supported server</span></span><br/> | <span data-ttu-id="b17aa-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b17aa-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b17aa-457">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b17aa-457">Namespace</span></span><br/>                | <span data-ttu-id="b17aa-458">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b17aa-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b17aa-459">MOF</span><span class="sxs-lookup"><span data-stu-id="b17aa-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b17aa-460"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b17aa-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b17aa-461">DLL</span><span class="sxs-lookup"><span data-stu-id="b17aa-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b17aa-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b17aa-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17aa-463">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b17aa-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17aa-464">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="b17aa-464">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dt>

[<span data-ttu-id="b17aa-465">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b17aa-465">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
