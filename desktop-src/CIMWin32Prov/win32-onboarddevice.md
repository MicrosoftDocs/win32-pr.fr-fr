---
description: La \_ classe WMI OnBoardDevice WMI représente les périphériques d’adaptateur courants intégrés à la carte mère (carte système).
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Classe Win32_OnBoardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201109"
---
# <a name="win32_onboarddevice-class"></a><span data-ttu-id="0d89e-103">\_Classe OnBoardDevice Win32</span><span class="sxs-lookup"><span data-stu-id="0d89e-103">Win32\_OnBoardDevice class</span></span>

<span data-ttu-id="0d89e-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OnBoardDevice** WMI représente les périphériques d’adaptateur courants intégrés à la carte mère (carte système).</span><span class="sxs-lookup"><span data-stu-id="0d89e-104">The **Win32\_OnBoardDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents common adapter devices built into the motherboard (system board).</span></span>

<span data-ttu-id="0d89e-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0d89e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0d89e-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0d89e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d89e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d89e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="0d89e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0d89e-108">Members</span></span>

<span data-ttu-id="0d89e-109">La classe **Win32 \_ OnBoardDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0d89e-109">The **Win32\_OnBoardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="0d89e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d89e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d89e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d89e-111">Properties</span></span>

<span data-ttu-id="0d89e-112">La classe **Win32 \_ OnBoardDevice** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0d89e-112">The **Win32\_OnBoardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d89e-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0d89e-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-116">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-117">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d89e-117">Short description of the object.</span></span>

<span data-ttu-id="0d89e-118">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0d89e-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-122">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0d89e-122">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-123">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0d89e-123">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0d89e-124">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0d89e-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0d89e-125">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-125">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="0d89e-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-129">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 10 \| Description")</span><span class="sxs-lookup"><span data-stu-id="0d89e-129">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-130">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d89e-130">Description of the object.</span></span>

<span data-ttu-id="0d89e-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-132">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="0d89e-132">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d89e-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-135">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 10 \| device type n")</span><span class="sxs-lookup"><span data-stu-id="0d89e-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Type n")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-136">Type d’appareil représenté.</span><span class="sxs-lookup"><span data-stu-id="0d89e-136">Type of device being represented.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d89e-137">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0d89e-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d89e-138">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0d89e-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="0d89e-139">**Vidéo** (3)</span><span class="sxs-lookup"><span data-stu-id="0d89e-139">**Video** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

<span data-ttu-id="0d89e-140">**Contrôleur SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="0d89e-140">**SCSI Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="0d89e-141">**Ethernet** (5)</span><span class="sxs-lookup"><span data-stu-id="0d89e-141">**Ethernet** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="0d89e-142">**Token Ring** (6)</span><span class="sxs-lookup"><span data-stu-id="0d89e-142">**Token Ring** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

<span data-ttu-id="0d89e-143">**Son** (7)</span><span class="sxs-lookup"><span data-stu-id="0d89e-143">**Sound** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d89e-144">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="0d89e-144">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d89e-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-147">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 10 \| Device Status n")</span><span class="sxs-lookup"><span data-stu-id="0d89e-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Status n")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-148">Si la **valeur est true**, l’appareil intégré peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="0d89e-148">If **TRUE**, the on-board device is available for use.</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="0d89e-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-150">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d89e-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-152">Si la **valeur est true**, un package physique peut être échangé à chaud (s’il est possible de remplacer l’élément par un autre physiquement, mais équivalent, alors que le package qui le contient est alimenté).</span><span class="sxs-lookup"><span data-stu-id="0d89e-152">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="0d89e-153">Par exemple, un package de lecteur de disque inséré à l’aide de connecteurs SCA est amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="0d89e-153">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="0d89e-154">Tous les packages pouvant être échangés à chaud sont par nature amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="0d89e-154">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="0d89e-155">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-155">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0d89e-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-157">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d89e-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-159">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0d89e-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-160">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d89e-160">Date and time the object was installed.</span></span> <span data-ttu-id="0d89e-161">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="0d89e-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0d89e-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-163">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="0d89e-163">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-166">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0d89e-166">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-167">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0d89e-167">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="0d89e-168">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-168">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-169">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="0d89e-169">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-172">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0d89e-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-173">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="0d89e-173">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="0d89e-174">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-175">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0d89e-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-178">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0d89e-178">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-179">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0d89e-179">Label by which the object is known.</span></span> <span data-ttu-id="0d89e-180">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0d89e-180">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0d89e-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-182">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0d89e-182">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-185">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="0d89e-185">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="0d89e-186">Par exemple, les données de code-barres associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="0d89e-186">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="0d89e-187">Notez que si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, cette propriété est **null** et les données de code-barres sont utilisées comme clé de classe dans la propriété de balise.</span><span class="sxs-lookup"><span data-stu-id="0d89e-187">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="0d89e-188">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-188">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-189">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="0d89e-189">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-192">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0d89e-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-193">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0d89e-193">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="0d89e-194">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-195">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="0d89e-195">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d89e-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-198">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="0d89e-198">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="0d89e-199">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-199">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-200">**Bande**</span><span class="sxs-lookup"><span data-stu-id="0d89e-200">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-201">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d89e-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-203">Si la **valeur est true**, un package physique est amovible (s’il est conçu pour être pris dans et hors du conteneur physique dans lequel il est normalement trouvé, sans altérer la fonction de l’empaquetage global).</span><span class="sxs-lookup"><span data-stu-id="0d89e-203">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="0d89e-204">Un package peut toujours être amovible si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="0d89e-204">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="0d89e-205">Si l’alimentation peut être « activée » et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="0d89e-205">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="0d89e-206">Par exemple, une batterie supplémentaire dans un ordinateur portable est amovible, comme c’est le cas d’un package de lecteur de disque inséré à l’aide de connecteurs SCA.</span><span class="sxs-lookup"><span data-stu-id="0d89e-206">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="0d89e-207">Toutefois, cette dernière peut être permutée à chaud.</span><span class="sxs-lookup"><span data-stu-id="0d89e-207">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="0d89e-208">L’affichage d’un ordinateur portable n’est pas amovible et n’est pas une alimentation non redondante.</span><span class="sxs-lookup"><span data-stu-id="0d89e-208">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="0d89e-209">La suppression de ces composants affecterait la fonction de l’ensemble de l’empaquetage ou est impossible en raison de l’intégration étroite du package.</span><span class="sxs-lookup"><span data-stu-id="0d89e-209">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="0d89e-210">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-210">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-211">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="0d89e-211">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-212">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0d89e-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-214">Si la **valeur est true**, un package physique est remplaçable (s’il est possible de remplacer, d’utiliser FRU ou de mettre à niveau, l’élément avec un différent physiquement).</span><span class="sxs-lookup"><span data-stu-id="0d89e-214">If **TRUE**, a physical package is replaceable (if it is possible to replace, FRU or upgrade, the element with a physically different one).</span></span> <span data-ttu-id="0d89e-215">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="0d89e-215">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="0d89e-216">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="0d89e-216">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="0d89e-217">Un autre exemple est un package d’alimentation monté sur des rails coulissants.</span><span class="sxs-lookup"><span data-stu-id="0d89e-217">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="0d89e-218">Tous les packages amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="0d89e-218">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="0d89e-219">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-219">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0d89e-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-223">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0d89e-223">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-224">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0d89e-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="0d89e-225">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-226">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="0d89e-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-229">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0d89e-229">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-230">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0d89e-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="0d89e-231">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-232">**État**</span><span class="sxs-lookup"><span data-stu-id="0d89e-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-235">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0d89e-235">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-236">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d89e-236">Current status of the object.</span></span> <span data-ttu-id="0d89e-237">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0d89e-237">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0d89e-238">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0d89e-238">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0d89e-239">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0d89e-239">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0d89e-240">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0d89e-240">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0d89e-241">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0d89e-241">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0d89e-242">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0d89e-243">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d89e-243">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0d89e-244">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-244">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0d89e-245">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-245">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d89e-246">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-246">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d89e-247">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0d89e-247">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0d89e-248">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-248">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0d89e-249">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-249">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0d89e-250">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-250">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0d89e-251">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-251">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0d89e-252">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-252">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0d89e-253">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-253">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0d89e-254">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-254">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0d89e-255">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0d89e-255">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d89e-256">**Tag**</span><span class="sxs-lookup"><span data-stu-id="0d89e-256">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-259">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0d89e-259">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-260">Identificateur unique de l’appareil intégré connecté au système.</span><span class="sxs-lookup"><span data-stu-id="0d89e-260">Unique identifier of the on-board device connected to the system.</span></span>

<span data-ttu-id="0d89e-261">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="0d89e-262">Exemple : « on Board Device 1 »</span><span class="sxs-lookup"><span data-stu-id="0d89e-262">Example: "On Board Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="0d89e-263">**Version**</span><span class="sxs-lookup"><span data-stu-id="0d89e-263">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d89e-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d89e-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d89e-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d89e-266">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0d89e-266">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0d89e-267">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0d89e-267">Version of the physical element.</span></span>

<span data-ttu-id="0d89e-268">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d89e-269">Notes</span><span class="sxs-lookup"><span data-stu-id="0d89e-269">Remarks</span></span>

<span data-ttu-id="0d89e-270">La classe **Win32 \_ OnBoardDevice** est dérivée de [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="0d89e-270">The **Win32\_OnBoardDevice** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d89e-271">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d89e-271">Requirements</span></span>



| <span data-ttu-id="0d89e-272">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d89e-272">Requirement</span></span> | <span data-ttu-id="0d89e-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d89e-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d89e-274">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d89e-274">Minimum supported client</span></span><br/> | <span data-ttu-id="0d89e-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d89e-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d89e-276">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d89e-276">Minimum supported server</span></span><br/> | <span data-ttu-id="0d89e-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d89e-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d89e-278">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d89e-278">Namespace</span></span><br/>                | <span data-ttu-id="0d89e-279">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0d89e-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d89e-280">MOF</span><span class="sxs-lookup"><span data-stu-id="0d89e-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d89e-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d89e-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d89e-282">DLL</span><span class="sxs-lookup"><span data-stu-id="0d89e-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d89e-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d89e-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d89e-284">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d89e-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d89e-285">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0d89e-285">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dt>

[<span data-ttu-id="0d89e-286">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0d89e-286">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
