---
description: Représente les fonctionnalités du logiciel de bas niveau utilisé pour démarrer et configurer un système informatique.
ms.assetid: 54d03539-d908-4571-b8fd-934b972e8d84
ms.tgt_platform: multiple
title: Classe CIM_BIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeature
- CIM_BIOSFeature.Caption
- CIM_BIOSFeature.Description
- CIM_BIOSFeature.InstallDate
- CIM_BIOSFeature.Status
- CIM_BIOSFeature.IdentifyingNumber
- CIM_BIOSFeature.ProductName
- CIM_BIOSFeature.Vendor
- CIM_BIOSFeature.Version
- CIM_BIOSFeature.Name
- CIM_BIOSFeature.CharacteristicDescriptions
- CIM_BIOSFeature.Characteristics
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 538dc9e4c18d976901519ae0e2d6f5249fd25c35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861417"
---
# <a name="cim_biosfeature-class"></a><span data-ttu-id="41023-103">\_Classe CIM BIOSFeature</span><span class="sxs-lookup"><span data-stu-id="41023-103">CIM\_BIOSFeature class</span></span>

<span data-ttu-id="41023-104">La classe **CIM \_ BIOSFeature** représente les fonctionnalités du logiciel de bas niveau utilisé pour démarrer et configurer un système informatique.</span><span class="sxs-lookup"><span data-stu-id="41023-104">The **CIM\_BIOSFeature** class represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41023-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="41023-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="41023-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="41023-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="41023-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="41023-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="41023-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="41023-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41023-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41023-109">Syntax</span></span>

``` syntax
[UUID("{7D33100E-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   IdentifyingNumber;
  string   ProductName;
  string   Vendor;
  string   Version;
  string   Name;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="41023-110">Membres</span><span class="sxs-lookup"><span data-stu-id="41023-110">Members</span></span>

<span data-ttu-id="41023-111">La classe **CIM \_ BIOSFeature** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="41023-111">The **CIM\_BIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="41023-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="41023-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41023-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="41023-113">Properties</span></span>

<span data-ttu-id="41023-114">La classe **CIM \_ BIOSFeature** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="41023-114">The **CIM\_BIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41023-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="41023-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="41023-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="41023-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="41023-119">A short textual description of the object.</span></span>

<span data-ttu-id="41023-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41023-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41023-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="41023-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-122">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="41023-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41023-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-124">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caractéristiques du BIOS DMTF \| 003,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**Caractéristiques**»)</span><span class="sxs-lookup"><span data-stu-id="41023-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="41023-125">Tableau de chaînes de forme libre qui fournit des explications détaillées sur les fonctionnalités du BIOS indiquées dans le tableau des **caractéristiques** .</span><span class="sxs-lookup"><span data-stu-id="41023-125">Array of free-form strings that provides detailed explanations of the BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="41023-126">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **caractéristiques** , qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="41023-126">Each entry in this array is related to the entry in the **Characteristics** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="41023-127">**Caractéristiques**</span><span class="sxs-lookup"><span data-stu-id="41023-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-128">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41023-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41023-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-130">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Caractéristiques du BIOS DMTF \| 003,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="41023-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="41023-131">Tableau d’entiers qui spécifie les fonctionnalités prises en charge par le BIOS.</span><span class="sxs-lookup"><span data-stu-id="41023-131">Array of integers that specifies the features supported by the BIOS.</span></span> <span data-ttu-id="41023-132">La valeur 3 n’est pas valide dans le schéma CIM car elle indique qu’aucune fonctionnalité BIOS n’est prise en charge dans DMI.</span><span class="sxs-lookup"><span data-stu-id="41023-132">The value 3 is not valid in the CIM schema because it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="41023-133">Dans ce cas, cet objet ne doit pas être instancié.</span><span class="sxs-lookup"><span data-stu-id="41023-133">In which case, this object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41023-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="41023-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="41023-135">Autre.</span><span class="sxs-lookup"><span data-stu-id="41023-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41023-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="41023-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="41023-137">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="41023-137">Unknown.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="41023-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Non défini** (3)</span><span class="sxs-lookup"><span data-stu-id="41023-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41023-139">Non défini.</span><span class="sxs-lookup"><span data-stu-id="41023-139">Undefined.</span></span>

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span data-ttu-id="41023-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**Prise en charge d’ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="41023-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA Support** (4)</span></span>


</dt> <dd>

<span data-ttu-id="41023-141">Prise en charge d’ISA.</span><span class="sxs-lookup"><span data-stu-id="41023-141">ISA support.</span></span>

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span data-ttu-id="41023-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**Support MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="41023-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA Support** (5)</span></span>


</dt> <dd>

<span data-ttu-id="41023-143">Prise en charge de MCA.</span><span class="sxs-lookup"><span data-stu-id="41023-143">MCA support.</span></span>

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span data-ttu-id="41023-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**Prise en charge EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="41023-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA Support** (6)</span></span>


</dt> <dd>

<span data-ttu-id="41023-145">Prise en charge de EISA.</span><span class="sxs-lookup"><span data-stu-id="41023-145">EISA support.</span></span>

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span data-ttu-id="41023-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**Prise en charge PCI** (7)</span><span class="sxs-lookup"><span data-stu-id="41023-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI Support** (7)</span></span>


</dt> <dd>

<span data-ttu-id="41023-147">Prise en charge PCI.</span><span class="sxs-lookup"><span data-stu-id="41023-147">PCI support.</span></span>

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span data-ttu-id="41023-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**Prise en charge PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="41023-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA Support** (8)</span></span>


</dt> <dd>

<span data-ttu-id="41023-149">Prise en charge PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="41023-149">PCMCIA support.</span></span>

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span data-ttu-id="41023-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**Prise en charge PNP** (9)</span><span class="sxs-lookup"><span data-stu-id="41023-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP Support** (9)</span></span>


</dt> <dd>

<span data-ttu-id="41023-151">Prise en charge PnP.</span><span class="sxs-lookup"><span data-stu-id="41023-151">PnP support.</span></span>

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span data-ttu-id="41023-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**Prise en charge APM** (10)</span><span class="sxs-lookup"><span data-stu-id="41023-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM Support** (10)</span></span>


</dt> <dd>

<span data-ttu-id="41023-153">Prise en charge APM.</span><span class="sxs-lookup"><span data-stu-id="41023-153">APM support.</span></span>

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span data-ttu-id="41023-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>Mise à **niveau du BIOS** (11)</span><span class="sxs-lookup"><span data-stu-id="41023-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradeable BIOS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="41023-155">Mise à niveau du BIOS.</span><span class="sxs-lookup"><span data-stu-id="41023-155">Upgradeable BIOS.</span></span>

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="41023-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**Masquage du BIOS autorisé** (12)</span><span class="sxs-lookup"><span data-stu-id="41023-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing Allowed** (12)</span></span>


</dt> <dd>

<span data-ttu-id="41023-157">Masquage du BIOS autorisé.</span><span class="sxs-lookup"><span data-stu-id="41023-157">BIOS shadowing allowed.</span></span>

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span data-ttu-id="41023-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**Prise en charge de VL VESA** (13)</span><span class="sxs-lookup"><span data-stu-id="41023-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA Support** (13)</span></span>


</dt> <dd>

<span data-ttu-id="41023-159">Prise en charge VESA de VL.</span><span class="sxs-lookup"><span data-stu-id="41023-159">VL VESA support.</span></span>

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span data-ttu-id="41023-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**Prise en charge ESCD** (14)</span><span class="sxs-lookup"><span data-stu-id="41023-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD Support** (14)</span></span>


</dt> <dd>

<span data-ttu-id="41023-161">Prise en charge ESCD.</span><span class="sxs-lookup"><span data-stu-id="41023-161">ESCD support.</span></span>

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span data-ttu-id="41023-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**Prise en charge LS-120** (15)</span><span class="sxs-lookup"><span data-stu-id="41023-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 Support** (15)</span></span>


</dt> <dd>

<span data-ttu-id="41023-163">Prise en charge LS-120.</span><span class="sxs-lookup"><span data-stu-id="41023-163">LS-120 support.</span></span>

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span data-ttu-id="41023-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**Prise en charge d’ACPI** (16)</span><span class="sxs-lookup"><span data-stu-id="41023-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI Support** (16)</span></span>


</dt> <dd>

<span data-ttu-id="41023-165">Prise en charge d’ACPI.</span><span class="sxs-lookup"><span data-stu-id="41023-165">ACPI support.</span></span>

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span data-ttu-id="41023-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**Prise en charge du démarrage I2O** (17)</span><span class="sxs-lookup"><span data-stu-id="41023-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O Boot Support** (17)</span></span>


</dt> <dd>

<span data-ttu-id="41023-167">Prise en charge du démarrage I2O.</span><span class="sxs-lookup"><span data-stu-id="41023-167">I2O boot support.</span></span>

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span data-ttu-id="41023-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**Prise en charge héritée USB** (18)</span><span class="sxs-lookup"><span data-stu-id="41023-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy Support** (18)</span></span>


</dt> <dd>

<span data-ttu-id="41023-169">Prise en charge héritée USB.</span><span class="sxs-lookup"><span data-stu-id="41023-169">USB legacy support.</span></span>

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span data-ttu-id="41023-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**Prise en charge AGP** (19)</span><span class="sxs-lookup"><span data-stu-id="41023-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP Support** (19)</span></span>


</dt> <dd>

<span data-ttu-id="41023-171">Prise en charge AGP.</span><span class="sxs-lookup"><span data-stu-id="41023-171">AGP support.</span></span>

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span data-ttu-id="41023-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**Carte PC** (20)</span><span class="sxs-lookup"><span data-stu-id="41023-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span></span>


</dt> <dd>

<span data-ttu-id="41023-173">Carte PC.</span><span class="sxs-lookup"><span data-stu-id="41023-173">PC card.</span></span>

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span data-ttu-id="41023-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span><span class="sxs-lookup"><span data-stu-id="41023-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span></span>


</dt> <dd>

<span data-ttu-id="41023-175">Télécommande.</span><span class="sxs-lookup"><span data-stu-id="41023-175">IR.</span></span>

</dd> <dt>

<span id="1394"></span>

<span data-ttu-id="41023-176"><span id="1394"></span>**1394** (22)</span><span class="sxs-lookup"><span data-stu-id="41023-176"><span id="1394"></span>**1394** (22)</span></span>


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="41023-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span><span class="sxs-lookup"><span data-stu-id="41023-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span></span>


</dt> <dd>

<span data-ttu-id="41023-178">I2C.</span><span class="sxs-lookup"><span data-stu-id="41023-178">I2C.</span></span>

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span data-ttu-id="41023-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Batterie intelligente** (24)</span><span class="sxs-lookup"><span data-stu-id="41023-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span></span>


</dt> <dd>

<span data-ttu-id="41023-180">Batterie intelligente.</span><span class="sxs-lookup"><span data-stu-id="41023-180">Smart battery.</span></span>

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="41023-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="41023-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>


</dt> <dd>

<span data-ttu-id="41023-182">PC-98.</span><span class="sxs-lookup"><span data-stu-id="41023-182">PC-98.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41023-183">**Description**</span><span class="sxs-lookup"><span data-stu-id="41023-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-186">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="41023-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="41023-187">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="41023-187">A textual description of the object.</span></span>

<span data-ttu-id="41023-188">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41023-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41023-189">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="41023-189">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-192">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="41023-192">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="41023-193">Identification du produit, telle qu’un numéro de série sur un logiciel ou un numéro gravé sur une puce matérielle.</span><span class="sxs-lookup"><span data-stu-id="41023-193">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

<span data-ttu-id="41023-194">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="41023-194">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="41023-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41023-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-196">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41023-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41023-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-198">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="41023-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="41023-199">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="41023-199">Indicates when the object was installed.</span></span> <span data-ttu-id="41023-200">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="41023-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="41023-201">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41023-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41023-202">**Nom**</span><span class="sxs-lookup"><span data-stu-id="41023-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-205">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41023-205">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41023-206">La propriété Name définit l’étiquette par laquelle l’objet est connu du monde extérieur au système de traitement des données.</span><span class="sxs-lookup"><span data-stu-id="41023-206">The Name property defines the label by which the object is known to the world outside the data processing system.</span></span> <span data-ttu-id="41023-207">Cette étiquette est un nom lisible par l’utilisateur qui identifie de façon unique l’élément dans le contexte de l’espace de noms de l’élément.</span><span class="sxs-lookup"><span data-stu-id="41023-207">This label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="41023-208">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="41023-208">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="41023-209">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="41023-209">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-212">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="41023-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="41023-213">Nom de produit couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="41023-213">Commonly used product name.</span></span>

<span data-ttu-id="41023-214">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="41023-214">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="41023-215">**État**</span><span class="sxs-lookup"><span data-stu-id="41023-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-218">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="41023-218">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="41023-219">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="41023-219">String that indicates the current status of the object.</span></span> <span data-ttu-id="41023-220">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="41023-220">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="41023-221">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="41023-221">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="41023-222">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="41023-222">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="41023-223">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="41023-223">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="41023-224">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="41023-224">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="41023-225">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="41023-225">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="41023-226">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41023-226">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="41023-227">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="41023-227">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="41023-228">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="41023-228">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="41023-229">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="41023-229">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="41023-230">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="41023-230">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41023-231">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="41023-231">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="41023-232">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="41023-232">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="41023-233">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="41023-233">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="41023-234">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="41023-234">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="41023-235">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="41023-235">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="41023-236">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="41023-236">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="41023-237">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="41023-237">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="41023-238">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="41023-238">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="41023-239">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="41023-239">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41023-240">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="41023-240">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-243">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Vendor**»), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« DMTF \| ComponentID \| 001,1 »)</span><span class="sxs-lookup"><span data-stu-id="41023-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="41023-244">Nom du fournisseur du produit, qui correspond à la propriété **Vendor** dans l’objet Product de la norme d’échange de solution DMTF.</span><span class="sxs-lookup"><span data-stu-id="41023-244">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="41023-245">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="41023-245">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="41023-246">**Version**</span><span class="sxs-lookup"><span data-stu-id="41023-246">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41023-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="41023-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41023-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="41023-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41023-249">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Version**"), [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="41023-249">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="41023-250">Les informations de version du produit, qui correspondent à la propriété **version** dans l’objet Product de la norme d’échange de solutions DMTF.</span><span class="sxs-lookup"><span data-stu-id="41023-250">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="41023-251">Cette propriété est héritée de la [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="41023-251">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41023-252">Notes</span><span class="sxs-lookup"><span data-stu-id="41023-252">Remarks</span></span>

<span data-ttu-id="41023-253">La classe **CIM \_ BIOSFeature** est dérivée de [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="41023-253">The **CIM\_BIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="41023-254">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="41023-254">WMI does not implement this class.</span></span>

<span data-ttu-id="41023-255">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="41023-255">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="41023-256">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="41023-256">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="41023-257">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41023-257">Requirements</span></span>



| <span data-ttu-id="41023-258">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41023-258">Requirement</span></span> | <span data-ttu-id="41023-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="41023-259">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41023-260">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41023-260">Minimum supported client</span></span><br/> | <span data-ttu-id="41023-261">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41023-261">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41023-262">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41023-262">Minimum supported server</span></span><br/> | <span data-ttu-id="41023-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41023-263">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41023-264">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="41023-264">Namespace</span></span><br/>                | <span data-ttu-id="41023-265">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="41023-265">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41023-266">MOF</span><span class="sxs-lookup"><span data-stu-id="41023-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41023-267"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41023-267"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41023-268">DLL</span><span class="sxs-lookup"><span data-stu-id="41023-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41023-269"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41023-269"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41023-270">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41023-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41023-271">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="41023-271">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

