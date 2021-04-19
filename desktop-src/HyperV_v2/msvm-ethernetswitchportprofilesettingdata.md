---
description: Représente les paramètres de profil de port.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Classe Msvm_EthernetSwitchPortProfileSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529508"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a><span data-ttu-id="6238a-103">MSVM \_ EthernetSwitchPortProfileSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="6238a-103">Msvm\_EthernetSwitchPortProfileSettingData class</span></span>

<span data-ttu-id="6238a-104">Représente les paramètres de profil de port.</span><span class="sxs-lookup"><span data-stu-id="6238a-104">Represents the port profile settings.</span></span>

<span data-ttu-id="6238a-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6238a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6238a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6238a-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a><span data-ttu-id="6238a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6238a-107">Members</span></span>

<span data-ttu-id="6238a-108">La classe **MSVM \_ EthernetSwitchPortProfileSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6238a-108">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6238a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6238a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6238a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6238a-110">Properties</span></span>

<span data-ttu-id="6238a-111">La classe **MSVM \_ EthernetSwitchPortProfileSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6238a-111">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6238a-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6238a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6238a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6238a-115">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6238a-115">A short description of the object.</span></span> <span data-ttu-id="6238a-116">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du profil de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="6238a-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="6238a-117">**CdnLabelId**</span><span class="sxs-lookup"><span data-stu-id="6238a-117">**CdnLabelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-118">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6238a-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-120">Qualificateurs : **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-120">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-121">Identificateur d’étiquette CDN.</span><span class="sxs-lookup"><span data-stu-id="6238a-121">The CDN label identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-122">**CdnLabelString**</span><span class="sxs-lookup"><span data-stu-id="6238a-122">**CdnLabelString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-125">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-126">Chaîne de l’étiquette CDN.</span><span class="sxs-lookup"><span data-stu-id="6238a-126">The CDN label string.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="6238a-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6238a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6238a-130">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="6238a-130">A description of the object.</span></span> <span data-ttu-id="6238a-131">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « représente les paramètres du profil de port ».</span><span class="sxs-lookup"><span data-stu-id="6238a-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port profile settings.".</span></span>

</dd> <dt>

<span data-ttu-id="6238a-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6238a-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6238a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6238a-135">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6238a-135">A display name for the object.</span></span> <span data-ttu-id="6238a-136">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du profil de port de commutateur Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="6238a-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="6238a-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6238a-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6238a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6238a-140">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="6238a-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6238a-141">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="6238a-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6238a-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6238a-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6238a-143">**ID NetCfgInstanceId**</span><span class="sxs-lookup"><span data-stu-id="6238a-143">**NetCfgInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-146">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-147">Identificateur d’appareil unique de la sous-interface.</span><span class="sxs-lookup"><span data-stu-id="6238a-147">An unique device identifier of the subinterface.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-148">**PciBusNumber**</span><span class="sxs-lookup"><span data-stu-id="6238a-148">**PciBusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6238a-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-151">Qualificateurs : **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-151">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-152">Numéro de bus PCI.</span><span class="sxs-lookup"><span data-stu-id="6238a-152">The PCI bus number.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-153">**PciDeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="6238a-153">**PciDeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-154">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6238a-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-156">Qualificateurs : **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-156">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-157">Numéro du périphérique PCI.</span><span class="sxs-lookup"><span data-stu-id="6238a-157">The PCI device number.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-158">**PciFunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="6238a-158">**PciFunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-159">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6238a-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-161">Qualificateurs : **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-161">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-162">Numéro de fonction PCI.</span><span class="sxs-lookup"><span data-stu-id="6238a-162">The PCI function number.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-163">**PciSegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="6238a-163">**PciSegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-164">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6238a-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-166">Qualificateurs : **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-166">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-167">Numéro de segment PCI.</span><span class="sxs-lookup"><span data-stu-id="6238a-167">The PCI segment number.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-168">**ProfileData**</span><span class="sxs-lookup"><span data-stu-id="6238a-168">**ProfileData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-169">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6238a-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-171">Qualificateurs : **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-171">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-172">Données supplémentaires pour le profil de port.</span><span class="sxs-lookup"><span data-stu-id="6238a-172">Additional data for the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-173">**ID**</span><span class="sxs-lookup"><span data-stu-id="6238a-173">**ProfileId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-176">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-177">Identificateur du profil de port.</span><span class="sxs-lookup"><span data-stu-id="6238a-177">The identifier of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-178">**ProfileName**</span><span class="sxs-lookup"><span data-stu-id="6238a-178">**ProfileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-180">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-181">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-182">Nom du profil de port.</span><span class="sxs-lookup"><span data-stu-id="6238a-182">The name of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-183">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="6238a-183">**VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-186">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-187">Identificateur du fournisseur définissant le profil.</span><span class="sxs-lookup"><span data-stu-id="6238a-187">The identifier of the vendor defining the profile.</span></span>

</dd> <dt>

<span data-ttu-id="6238a-188">**VendorName**</span><span class="sxs-lookup"><span data-stu-id="6238a-188">**VendorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6238a-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6238a-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6238a-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6238a-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6238a-191">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="6238a-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="6238a-192">Nom du fournisseur définissant le profil.</span><span class="sxs-lookup"><span data-stu-id="6238a-192">The name of the vendor defining the profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6238a-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6238a-193">Requirements</span></span>



| <span data-ttu-id="6238a-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6238a-194">Requirement</span></span> | <span data-ttu-id="6238a-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="6238a-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6238a-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6238a-196">Minimum supported client</span></span><br/> | <span data-ttu-id="6238a-197">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6238a-197">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6238a-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6238a-198">Minimum supported server</span></span><br/> | <span data-ttu-id="6238a-199">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6238a-199">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6238a-200">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6238a-200">Namespace</span></span><br/>                | <span data-ttu-id="6238a-201">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6238a-201">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6238a-202">MOF</span><span class="sxs-lookup"><span data-stu-id="6238a-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6238a-203"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6238a-203"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6238a-204">DLL</span><span class="sxs-lookup"><span data-stu-id="6238a-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6238a-205"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6238a-205"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

