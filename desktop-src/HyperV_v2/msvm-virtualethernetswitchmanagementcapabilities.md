---
description: Décrit les fonctionnalités du VirtualEthernetSwitchManagementService MSVM associé \_ .
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Classe Msvm_VirtualEthernetSwitchManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519996"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a><span data-ttu-id="b4fe1-103">MSVM \_ VirtualEthernetSwitchManagementCapabilities, classe</span><span class="sxs-lookup"><span data-stu-id="b4fe1-103">Msvm\_VirtualEthernetSwitchManagementCapabilities class</span></span>

<span data-ttu-id="b4fe1-104">Décrit les fonctionnalités du [**\_ VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md)associé.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-104">Describes the capabilities of the associated [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md).</span></span>

<span data-ttu-id="b4fe1-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fe1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4fe1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="b4fe1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b4fe1-107">Members</span></span>

<span data-ttu-id="b4fe1-108">La classe **MSVM \_ VirtualEthernetSwitchManagementCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b4fe1-108">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="b4fe1-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4fe1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4fe1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4fe1-110">Properties</span></span>

<span data-ttu-id="b4fe1-111">La classe **MSVM \_ VirtualEthernetSwitchManagementCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-111">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4fe1-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-113">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-116">Tableau d’identificateurs de méthode, chacun identifiant une méthode de la classe [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) qui est prise en charge de façon asynchrone par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-116">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported asynchronously by the implementation.</span></span> <span data-ttu-id="b4fe1-117">Cette propriété est héritée de la **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-117">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

<span data-ttu-id="b4fe1-118">**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-118">**DefineSystem** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

<span data-ttu-id="b4fe1-119">**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-119">**DestroySystem** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

<span data-ttu-id="b4fe1-120">**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-120">**DestroySystemConfiguration** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

<span data-ttu-id="b4fe1-121">**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-121">**ModifyResourceSettings** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

<span data-ttu-id="b4fe1-122">**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-122">**ModifySystemSettings** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

<span data-ttu-id="b4fe1-123">**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-123">**RemoveResources** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

<span data-ttu-id="b4fe1-124">**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-124">**SelectSystemConfiguration** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

<span data-ttu-id="b4fe1-125">**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-125">**SnapshotSystem** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

<span data-ttu-id="b4fe1-126">**AddResources** (10)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-126">**AddResources** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="b4fe1-127">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-127">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="b4fe1-128">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-128">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="b4fe1-129">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-129">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="b4fe1-130">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-130">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="b4fe1-131">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-131">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="b4fe1-132">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-132">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b4fe1-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-136">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-136">A short description of the object.</span></span> <span data-ttu-id="b4fe1-137">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités du service de gestion du commutateur Ethernet virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="b4fe1-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-141">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="b4fe1-141">A description of the object.</span></span> <span data-ttu-id="b4fe1-142">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « définit les fonctionnalités du service de gestion de commutateur Ethernet virtuel ».</span><span class="sxs-lookup"><span data-stu-id="b4fe1-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-146">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-146">A display name for the object.</span></span> <span data-ttu-id="b4fe1-147">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « fonctionnalités du service de gestion du commutateur Ethernet virtuel Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="b4fe1-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-148">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-148">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-149">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-151">Indique si la propriété **ElementName** peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-151">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="b4fe1-152">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-152">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-153">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-153">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-156">Spécifie les restrictions sur **ElementName**, exprimées sous la forme d’une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-156">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="b4fe1-157">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-157">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-158">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-158">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-159">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-161">Tableau d’identificateurs d’indication, chacun identifiant une indication qui est prise en charge par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-161">An array of indication identifiers, each identifying an indication that is supported by the implementation.</span></span> <span data-ttu-id="b4fe1-162">Cette propriété est héritée de la **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-162">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>



| <span data-ttu-id="b4fe1-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4fe1-163">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="b4fe1-164">Signification</span><span class="sxs-lookup"><span data-stu-id="b4fe1-164">Meaning</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="b4fe1-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b4fe1-166">Indique si l’implémentation de prend en charge les notifications sur les modifications d’état des instances [**CIM du \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) qui représentent les ressources des systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-166">Indicates whether the implementation supports notification on state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances that represent resources of virtual systems.</span></span><br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="b4fe1-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="b4fe1-168">Indique si l’implémentation prend en charge la notification des modifications d’état des instances [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b4fe1-168">Indicates whether the implementation supports notification on state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span><br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="b4fe1-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="b4fe1-170">Indique si l’implémentation prend en charge la notification des modifications d’état des instances [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représentent des systèmes virtuels.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-170">Indicates whether the implementation supports notification on state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances that represent virtual systems.</span></span><br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="b4fe1-171"><dt>**DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-171"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="b4fe1-172">32767 <dt> **réservé au fournisseur**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-172"><dt>**Vendor Reserved** </dt> <dt>32767..65535 </dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="b4fe1-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-176">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-177">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b4fe1-178">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b4fe1-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-179">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-179">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-182">Valeur booléenne qui indique si la virtualisation d’e/s (IOV) est prise en charge par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-182">A boolean value that indicates whether I/O virtualization (IOV) is supported by the platform.</span></span> <span data-ttu-id="b4fe1-183">Si la valeur est **true**, IOV est pris en charge par la plateforme et **iovsupportreasons fourniront** sera vide.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-183">If the value is **True**, then IOV is supported by the platform and **IOVSupportReasons** will be empty.</span></span> <span data-ttu-id="b4fe1-184">Sinon, la propriété **iovsupportreasons fourniront** aura les raisons pour lesquelles IOV ne peut pas être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-184">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-185">**Iovsupportreasons fourniront**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-185">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-186">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-188">Tableau de chaînes qui indique les raisons possibles pour lesquelles IOV n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-188">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="b4fe1-189">Si la valeur de **IOVSupport** est **true**, ce tableau sera vide.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-189">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-190">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-190">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-191">Type de données : **unit16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-191">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-193">Qualificateurs : **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-193">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-194">Spécifie la longueur maximale prise en charge de la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="b4fe1-194">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="b4fe1-195">Cette propriété est héritée de la **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-195">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-196">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-196">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-197">Type de données : tableau **unit16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-197">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-199">Indique les États possibles qui peuvent être demandés lors de l’utilisation de la méthode **RequestStateChange** sur l’élément logique activé.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-199">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="b4fe1-200">Cette propriété est héritée de **CIM \_ EnabledLogicalElementCapabilities** et est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-200">This property is inherited from **CIM\_EnabledLogicalElementCapabilities** and is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-201">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-201">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-202">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-202">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-204">Tableau d’identificateurs de méthode, chacun identifiant une méthode de la classe [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) qui est prise en charge de façon synchrone par l’implémentation de.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-204">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported synchronously by the implementation.</span></span> <span data-ttu-id="b4fe1-205">Cette propriété est héritée de la **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-205">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="b4fe1-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b4fe1-218">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-218">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-219">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-219">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b4fe1-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-221">Tableau de chaînes, chacune désignant un type de système virtuel que l’implémentation prend en charge.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-221">An array of strings, each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="b4fe1-222">La valeur de chaque élément de tableau non **null** doit être conforme au format défini pour la propriété **VirtualSystemType** de la [**classe \_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="b4fe1-222">The value of each non-**Null** array element must conform to the format defined for the **VirtualSystemType** property of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span> <span data-ttu-id="b4fe1-223">Cette propriété est héritée de la **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-223">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4fe1-224">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4fe1-224">Requirements</span></span>



| <span data-ttu-id="b4fe1-225">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4fe1-225">Requirement</span></span> | <span data-ttu-id="b4fe1-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4fe1-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fe1-227">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4fe1-227">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fe1-228">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4fe1-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b4fe1-229">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4fe1-229">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fe1-230">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4fe1-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4fe1-231">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b4fe1-231">Namespace</span></span><br/>                | <span data-ttu-id="b4fe1-232">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b4fe1-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b4fe1-233">MOF</span><span class="sxs-lookup"><span data-stu-id="b4fe1-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4fe1-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4fe1-235">DLL</span><span class="sxs-lookup"><span data-stu-id="b4fe1-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4fe1-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

