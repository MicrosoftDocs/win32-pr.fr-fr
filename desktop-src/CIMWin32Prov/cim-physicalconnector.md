---
description: La \_ classe CIM PhysicalConnector représente tout élément physique utilisé pour se connecter à d’autres éléments. Tout objet qui peut se connecter et transmettre des signaux ou de la puissance entre deux ou plusieurs éléments physiques est un descendant (ou membre) de cette classe.
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: Classe CIM_PhysicalConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 106b8ab30296b77be550809771db3b0208485872
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512898"
---
# <a name="cim_physicalconnector-class"></a><span data-ttu-id="0a433-104">\_Classe CIM PhysicalConnector</span><span class="sxs-lookup"><span data-stu-id="0a433-104">CIM\_PhysicalConnector class</span></span>

<span data-ttu-id="0a433-105">La classe **CIM \_ PhysicalConnector** représente tout élément physique utilisé pour se connecter à d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="0a433-105">The **CIM\_PhysicalConnector** class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="0a433-106">Tout objet qui peut se connecter et transmettre des signaux ou de la puissance entre deux ou plusieurs éléments physiques est un descendant (ou membre) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0a433-106">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span> <span data-ttu-id="0a433-107">Par exemple, les emplacements et les connecteurs D-Shell sont des types de connecteurs physiques.</span><span class="sxs-lookup"><span data-stu-id="0a433-107">For example, slots and D-shell connectors are types of physical connectors.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a433-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0a433-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0a433-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0a433-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0a433-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0a433-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0a433-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0a433-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a433-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a433-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a><span data-ttu-id="0a433-113">Membres</span><span class="sxs-lookup"><span data-stu-id="0a433-113">Members</span></span>

<span data-ttu-id="0a433-114">La classe **CIM \_ PhysicalConnector** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0a433-114">The **CIM\_PhysicalConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="0a433-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a433-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a433-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a433-116">Properties</span></span>

<span data-ttu-id="0a433-117">La classe **CIM \_ PhysicalConnector** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a433-117">The **CIM\_PhysicalConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a433-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0a433-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0a433-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0a433-122">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0a433-122">A short textual description of the object.</span></span>

<span data-ttu-id="0a433-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-124">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="0a433-124">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a433-127">Chaîne de forme libre qui décrit la configuration du code confidentiel et l’utilisation des signaux d’un connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-127">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

</dd> <dt>

<span data-ttu-id="0a433-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="0a433-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-129">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a433-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0a433-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a433-131">Type de connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-131">Type of physical connector.</span></span> <span data-ttu-id="0a433-132">Un tableau est spécifié pour autoriser la description des combinaisons d’informations de connecteur.</span><span class="sxs-lookup"><span data-stu-id="0a433-132">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="0a433-133">Par exemple, une entrée de tableau peut spécifier RS-232, une autre DB-25 et une troisième entrée peut définir le connecteur comme « mâle ».</span><span class="sxs-lookup"><span data-stu-id="0a433-133">For example, one array entry could specify RS-232, another DB-25, and a third entry could define the connector as "male".</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a433-134">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0a433-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0a433-135">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0a433-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="0a433-136">**Mâle** (2)</span><span class="sxs-lookup"><span data-stu-id="0a433-136">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="0a433-137">**Femme** (3)</span><span class="sxs-lookup"><span data-stu-id="0a433-137">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="0a433-138">**Protégé** (4)</span><span class="sxs-lookup"><span data-stu-id="0a433-138">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="0a433-139">**Unblindée** (5)</span><span class="sxs-lookup"><span data-stu-id="0a433-139">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="0a433-140">**SCSI (A) High-Density (50 broches)** (6)</span><span class="sxs-lookup"><span data-stu-id="0a433-140">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="0a433-141">**SCSI (A) Low-Density (pin 50)** (7)</span><span class="sxs-lookup"><span data-stu-id="0a433-141">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="0a433-142">**SCSI (P) High-Density (68 broches)** (8)</span><span class="sxs-lookup"><span data-stu-id="0a433-142">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="0a433-143">**SCSI SCA-I (80 broches)** (9)</span><span class="sxs-lookup"><span data-stu-id="0a433-143">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="0a433-144">**SCSI SCA-II (80 broches)** (10)</span><span class="sxs-lookup"><span data-stu-id="0a433-144">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="0a433-145">**Fibre Channel SCSI (DB-9, cuivre)** (11)</span><span class="sxs-lookup"><span data-stu-id="0a433-145">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="0a433-146">**Fibre Channel SCSI (fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="0a433-146">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="0a433-147">**SCSI Fibre Channel SCA-II (40 broches)** (13)</span><span class="sxs-lookup"><span data-stu-id="0a433-147">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="0a433-148">**SCSI Fibre Channel SCA-II (20 broches)** (14)</span><span class="sxs-lookup"><span data-stu-id="0a433-148">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="0a433-149">**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="0a433-149">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="0a433-150">**ATA 3-1/2 pouces (40 broches)** (16)</span><span class="sxs-lookup"><span data-stu-id="0a433-150">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="0a433-151">**ATA 2-1/2 pouces (44 broches)** (17)</span><span class="sxs-lookup"><span data-stu-id="0a433-151">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="0a433-152">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="0a433-152">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="0a433-153">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="0a433-153">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="0a433-154">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="0a433-154">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="0a433-155">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="0a433-155">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="0a433-156">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="0a433-156">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="0a433-157">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="0a433-157">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="0a433-158">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="0a433-158">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="0a433-159">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="0a433-159">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="0a433-160">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="0a433-160">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="0a433-161">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="0a433-161">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="0a433-162">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="0a433-162">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="0a433-163">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="0a433-163">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="0a433-164">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="0a433-164">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="0a433-165">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="0a433-165">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="0a433-166">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="0a433-166">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="0a433-167">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="0a433-167">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="0a433-168">**UTP catégorie 3** (34)</span><span class="sxs-lookup"><span data-stu-id="0a433-168">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="0a433-169">**UTP catégorie 4** (35)</span><span class="sxs-lookup"><span data-stu-id="0a433-169">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="0a433-170">**UTP catégorie 5** (36)</span><span class="sxs-lookup"><span data-stu-id="0a433-170">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="0a433-171">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="0a433-171">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="0a433-172">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="0a433-172">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="0a433-173">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="0a433-173">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="0a433-174">**Fibre optique** (40)</span><span class="sxs-lookup"><span data-stu-id="0a433-174">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="0a433-175">**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="0a433-175">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="0a433-176">**Port Apple** (42)</span><span class="sxs-lookup"><span data-stu-id="0a433-176">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="0a433-177">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="0a433-177">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="0a433-178">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="0a433-178">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="0a433-179">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="0a433-179">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="0a433-180">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="0a433-180">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="0a433-181">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="0a433-181">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="0a433-182">**PCMCIA, type I** (48)</span><span class="sxs-lookup"><span data-stu-id="0a433-182">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="0a433-183">**PCMCIA type II** (49)</span><span class="sxs-lookup"><span data-stu-id="0a433-183">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="0a433-184">**PCMCIA type III** (50)</span><span class="sxs-lookup"><span data-stu-id="0a433-184">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="0a433-185">**Port ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="0a433-185">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="0a433-186">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="0a433-186">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="0a433-187">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="0a433-187">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="0a433-188">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="0a433-188">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="0a433-189">**HIPPA** (55)</span><span class="sxs-lookup"><span data-stu-id="0a433-189">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="0a433-190">**HSSDC (6 broches)** (56)</span><span class="sxs-lookup"><span data-stu-id="0a433-190">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="0a433-191">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="0a433-191">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="0a433-192">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="0a433-192">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="0a433-193">**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="0a433-193">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="0a433-194">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="0a433-194">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="0a433-195">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="0a433-195">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="0a433-196">**Infrarouge** (62)</span><span class="sxs-lookup"><span data-stu-id="0a433-196">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="0a433-197">**HP-HIL** (63)</span><span class="sxs-lookup"><span data-stu-id="0a433-197">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="0a433-198">**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="0a433-198">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="0a433-199">**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="0a433-199">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="0a433-200">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="0a433-200">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="0a433-201">**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="0a433-201">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="0a433-202">**Type Mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="0a433-202">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="0a433-203">**Mini-Centronics type-20** (69)</span><span class="sxs-lookup"><span data-stu-id="0a433-203">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="0a433-204">**Mini-Centronics type-26** (70)</span><span class="sxs-lookup"><span data-stu-id="0a433-204">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="0a433-205">**Souris bus** (71)</span><span class="sxs-lookup"><span data-stu-id="0a433-205">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="0a433-206">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="0a433-206">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="0a433-207">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="0a433-207">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="0a433-208">**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="0a433-208">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="0a433-209">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="0a433-209">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="0a433-210">**Propriétaire** (76)</span><span class="sxs-lookup"><span data-stu-id="0a433-210">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="0a433-211">**Emplacement de la carte de processeur propriétaire** (77)</span><span class="sxs-lookup"><span data-stu-id="0a433-211">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="0a433-212">**Emplacement de carte mémoire propriétaire** (78)</span><span class="sxs-lookup"><span data-stu-id="0a433-212">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="0a433-213">**Emplacement de la carte de montage des e/s propriétaire** (79)</span><span class="sxs-lookup"><span data-stu-id="0a433-213">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="0a433-214">**PCI-66 MHz** (80)</span><span class="sxs-lookup"><span data-stu-id="0a433-214">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="0a433-215">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="0a433-215">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="0a433-216">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="0a433-216">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="0a433-217">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="0a433-217">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="0a433-218">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="0a433-218">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="0a433-219">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="0a433-219">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="0a433-220">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="0a433-220">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="0a433-221">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="0a433-221">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="0a433-222">**SCSI SSA** (88)</span><span class="sxs-lookup"><span data-stu-id="0a433-222">**SSA SCSI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

<span data-ttu-id="0a433-223">**Circulaire** (89)</span><span class="sxs-lookup"><span data-stu-id="0a433-223">**Circular** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

<span data-ttu-id="0a433-224">**Connecteur IDE sur carte** (90)</span><span class="sxs-lookup"><span data-stu-id="0a433-224">**On Board IDE Connector** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

<span data-ttu-id="0a433-225">**Connecteur de disquette sur carte** (91)</span><span class="sxs-lookup"><span data-stu-id="0a433-225">**On Board Floppy Connector** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

<span data-ttu-id="0a433-226">**2 broches en double en ligne** (92)</span><span class="sxs-lookup"><span data-stu-id="0a433-226">**9 Pin Dual Inline** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

<span data-ttu-id="0a433-227">**25 broches en ligne double** (93)</span><span class="sxs-lookup"><span data-stu-id="0a433-227">**25 Pin Dual Inline** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="0a433-228">**50 broche double Inline** (94)</span><span class="sxs-lookup"><span data-stu-id="0a433-228">**50 Pin Dual Inline** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

<span data-ttu-id="0a433-229">**68 broche double Inline** (95)</span><span class="sxs-lookup"><span data-stu-id="0a433-229">**68 Pin Dual Inline** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

<span data-ttu-id="0a433-230">**Connecteur Sound-Board** (96)</span><span class="sxs-lookup"><span data-stu-id="0a433-230">**On Board Sound Connector** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="0a433-231">**Mini-jack** (97)</span><span class="sxs-lookup"><span data-stu-id="0a433-231">**Mini-jack** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="0a433-232">**PCI-X** (98)</span><span class="sxs-lookup"><span data-stu-id="0a433-232">**PCI-X** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="0a433-233">**SBus IEEE 1396-1993 32 bits** (99)</span><span class="sxs-lookup"><span data-stu-id="0a433-233">**Sbus IEEE 1396-1993 32 bit** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="0a433-234">**SBus IEEE 1396-1993 64 bits** (100)</span><span class="sxs-lookup"><span data-stu-id="0a433-234">**Sbus IEEE 1396-1993 64 bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="0a433-235">**MCA** (101)</span><span class="sxs-lookup"><span data-stu-id="0a433-235">**MCA** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="0a433-236">**Gio** (102)</span><span class="sxs-lookup"><span data-stu-id="0a433-236">**GIO** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="0a433-237">**XIO** (103)</span><span class="sxs-lookup"><span data-stu-id="0a433-237">**XIO** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="0a433-238">**HIO** (104)</span><span class="sxs-lookup"><span data-stu-id="0a433-238">**HIO** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="0a433-239">**NGIO** (105)</span><span class="sxs-lookup"><span data-stu-id="0a433-239">**NGIO** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="0a433-240">**PMC** (106)</span><span class="sxs-lookup"><span data-stu-id="0a433-240">**PMC** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

<span data-ttu-id="0a433-241">**MTRJ** (107)</span><span class="sxs-lookup"><span data-stu-id="0a433-241">**MTRJ** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

<span data-ttu-id="0a433-242">**VF-45** (108)</span><span class="sxs-lookup"><span data-stu-id="0a433-242">**VF-45** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="0a433-243">**E/s futures** (109)</span><span class="sxs-lookup"><span data-stu-id="0a433-243">**Future I/O** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

<span data-ttu-id="0a433-244">**SC** (110)</span><span class="sxs-lookup"><span data-stu-id="0a433-244">**SC** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

<span data-ttu-id="0a433-245">**SG** (111)</span><span class="sxs-lookup"><span data-stu-id="0a433-245">**SG** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

<span data-ttu-id="0a433-246">**Électrique** (112)</span><span class="sxs-lookup"><span data-stu-id="0a433-246">**Electrical** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

<span data-ttu-id="0a433-247">**Optique** (113)</span><span class="sxs-lookup"><span data-stu-id="0a433-247">**Optical** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

<span data-ttu-id="0a433-248">**Ruban** (114)</span><span class="sxs-lookup"><span data-stu-id="0a433-248">**Ribbon** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

<span data-ttu-id="0a433-249">**GLM** (115)</span><span class="sxs-lookup"><span data-stu-id="0a433-249">**GLM** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

<span data-ttu-id="0a433-250">**1x9** (116)</span><span class="sxs-lookup"><span data-stu-id="0a433-250">**1x9** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

<span data-ttu-id="0a433-251">**Mini SG** (117)</span><span class="sxs-lookup"><span data-stu-id="0a433-251">**Mini SG** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

<span data-ttu-id="0a433-252">**LC** (118)</span><span class="sxs-lookup"><span data-stu-id="0a433-252">**LC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

<span data-ttu-id="0a433-253">**HSSC** (119)</span><span class="sxs-lookup"><span data-stu-id="0a433-253">**HSSC** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

<span data-ttu-id="0a433-254">**VHDCI protégé (68 broches)** (120)</span><span class="sxs-lookup"><span data-stu-id="0a433-254">**VHDCI Shielded (68 pins)** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="0a433-255">**InfiniBand** (121)</span><span class="sxs-lookup"><span data-stu-id="0a433-255">**InfiniBand** (121)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a433-256">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0a433-256">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-259">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0a433-259">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-260">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0a433-260">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0a433-261">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0a433-261">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0a433-262">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-263">**Description**</span><span class="sxs-lookup"><span data-stu-id="0a433-263">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-266">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0a433-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0a433-267">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0a433-267">A textual description of the object.</span></span>

<span data-ttu-id="0a433-268">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-268">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-269">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0a433-269">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-270">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0a433-270">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-272">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0a433-272">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0a433-273">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="0a433-273">Indicates when the object was installed.</span></span> <span data-ttu-id="0a433-274">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="0a433-274">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0a433-275">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-276">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="0a433-276">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-277">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-279">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0a433-279">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-280">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-280">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="0a433-281">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-281">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="0a433-282">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-283">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="0a433-283">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-286">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0a433-286">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-287">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="0a433-287">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="0a433-288">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-288">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-289">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0a433-289">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-292">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0a433-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0a433-293">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0a433-293">Label by which the object is known.</span></span> <span data-ttu-id="0a433-294">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0a433-294">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0a433-295">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-296">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0a433-296">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a433-299">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-299">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="0a433-300">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="0a433-300">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="0a433-301">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="0a433-301">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="0a433-302">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-303">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="0a433-303">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-306">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0a433-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-307">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-307">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="0a433-308">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-308">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-309">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="0a433-309">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-310">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0a433-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a433-312">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="0a433-312">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="0a433-313">Dans le cas contraire, elle est actuellement désactivée.</span><span class="sxs-lookup"><span data-stu-id="0a433-313">Otherwise, it is currently off.</span></span>

<span data-ttu-id="0a433-314">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-315">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0a433-315">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-318">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0a433-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-319">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-319">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="0a433-320">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-321">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="0a433-321">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-324">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0a433-324">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-325">Numéro d’unité de conservation pour cet élément physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-325">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="0a433-326">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-327">**État**</span><span class="sxs-lookup"><span data-stu-id="0a433-327">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-330">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0a433-330">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0a433-331">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0a433-331">String that indicates the current status of the object.</span></span> <span data-ttu-id="0a433-332">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="0a433-332">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0a433-333">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="0a433-333">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0a433-334">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="0a433-334">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0a433-335">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0a433-335">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0a433-336">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0a433-336">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0a433-337">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0a433-337">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0a433-338">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0a433-339">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a433-339">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0a433-340">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0a433-340">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0a433-341">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0a433-341">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0a433-342">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0a433-342">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a433-343">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0a433-343">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0a433-344">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0a433-344">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0a433-345">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0a433-345">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0a433-346">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0a433-346">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0a433-347">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0a433-347">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0a433-348">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0a433-348">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0a433-349">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0a433-349">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0a433-350">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0a433-350">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0a433-351">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0a433-351">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a433-352">**Tag**</span><span class="sxs-lookup"><span data-stu-id="0a433-352">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-355">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0a433-355">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-356">Identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0a433-356">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="0a433-357">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="0a433-357">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="0a433-358">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="0a433-358">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="0a433-359">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="0a433-359">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="0a433-360">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0a433-360">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="0a433-361">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="0a433-361">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="0a433-362">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-362">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a433-363">**Version**</span><span class="sxs-lookup"><span data-stu-id="0a433-363">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a433-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a433-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a433-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0a433-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a433-366">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0a433-366">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0a433-367">Indique la version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0a433-367">Indicates the version of the physical element.</span></span>

<span data-ttu-id="0a433-368">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-368">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a433-369">Notes</span><span class="sxs-lookup"><span data-stu-id="0a433-369">Remarks</span></span>

<span data-ttu-id="0a433-370">La classe **CIM \_ PhysicalConnector** est dérivée de [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-370">The **CIM\_PhysicalConnector** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="0a433-371">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="0a433-371">WMI does not implement this class.</span></span> <span data-ttu-id="0a433-372">Pour les classes WMI dérivées de **CIM \_ PhysicalConnector**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0a433-372">For WMI classes that are derived from **CIM\_PhysicalConnector**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0a433-373">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0a433-373">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0a433-374">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0a433-374">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a433-375">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a433-375">Requirements</span></span>



| <span data-ttu-id="0a433-376">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a433-376">Requirement</span></span> | <span data-ttu-id="0a433-377">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a433-377">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a433-378">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a433-378">Minimum supported client</span></span><br/> | <span data-ttu-id="0a433-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a433-379">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a433-380">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a433-380">Minimum supported server</span></span><br/> | <span data-ttu-id="0a433-381">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a433-381">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a433-382">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0a433-382">Namespace</span></span><br/>                | <span data-ttu-id="0a433-383">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0a433-383">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a433-384">MOF</span><span class="sxs-lookup"><span data-stu-id="0a433-384">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a433-385"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a433-385"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a433-386">DLL</span><span class="sxs-lookup"><span data-stu-id="0a433-386">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a433-387"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a433-387"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a433-388">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a433-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a433-389">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0a433-389">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

