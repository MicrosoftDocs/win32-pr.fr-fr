---
description: Représente les propriétés associées à un boîtier système physique.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Classe Win32_SystemEnclosure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950822"
---
# <a name="win32_systemenclosure-class"></a><span data-ttu-id="0e75c-103">\_Classe SystemEnclosure Win32</span><span class="sxs-lookup"><span data-stu-id="0e75c-103">Win32\_SystemEnclosure class</span></span>

<span data-ttu-id="0e75c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemEnclosure** WMI représente les propriétés associées à un boîtier système physique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-104">The **Win32\_SystemEnclosure** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties that are associated with a physical system enclosure.</span></span>

<span data-ttu-id="0e75c-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e75c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0e75c-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0e75c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e75c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e75c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="0e75c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0e75c-108">Members</span></span>

<span data-ttu-id="0e75c-109">La classe **Win32 \_ SystemEnclosure** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e75c-109">The **Win32\_SystemEnclosure** class has these types of members:</span></span>

-   [<span data-ttu-id="0e75c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e75c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e75c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e75c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e75c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e75c-112">Methods</span></span>

<span data-ttu-id="0e75c-113">La classe **Win32 \_ SystemEnclosure** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0e75c-113">The **Win32\_SystemEnclosure** class has these methods.</span></span>



| <span data-ttu-id="0e75c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="0e75c-114">Method</span></span>           | <span data-ttu-id="0e75c-115">Description</span><span class="sxs-lookup"><span data-stu-id="0e75c-115">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="0e75c-116">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="0e75c-116">**IsCompatible**</span></span> | <span data-ttu-id="0e75c-117">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0e75c-117">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0e75c-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e75c-118">Properties</span></span>

<span data-ttu-id="0e75c-119">La classe **Win32 \_ SystemEnclosure** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0e75c-119">The **Win32\_SystemEnclosure** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e75c-120">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="0e75c-120">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-121">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e75c-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-123">Si la **valeur est true**, le cadre est équipé d’une alarme sonore.</span><span class="sxs-lookup"><span data-stu-id="0e75c-123">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="0e75c-124">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-124">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-125">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="0e75c-125">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-128">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="0e75c-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-129">Chaîne de forme libre qui fournit plus d’informations si la propriété **SecurityBreach** indique qu’un événement lié à la sécurité s’est produit.</span><span class="sxs-lookup"><span data-stu-id="0e75c-129">Free-form string that provides more information if the **SecurityBreach** property indicates that a security-related event occurred.</span></span>

<span data-ttu-id="0e75c-130">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-130">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-131">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="0e75c-131">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-134">Chaîne de forme libre qui contient des informations sur la façon dont les différents câbles sont connectés et regroupés pour le frame.</span><span class="sxs-lookup"><span data-stu-id="0e75c-134">Free-form string that contains information about how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="0e75c-135">Avec de nombreuses connexions réseau, liées au stockage et aux câbles d’alimentation, la gestion des câbles peut être un défi complexe et difficile.</span><span class="sxs-lookup"><span data-stu-id="0e75c-135">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="0e75c-136">Cette propriété contient des informations pour faciliter l’assembly et le service du frame.</span><span class="sxs-lookup"><span data-stu-id="0e75c-136">This property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="0e75c-137">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-137">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0e75c-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-141">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-141">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-142">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="0e75c-142">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="0e75c-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-144">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="0e75c-144">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-145">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e75c-145">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-147">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Table globale du conteneur physique DMTF \| 002,1 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ châssis CIM**](cim-chassis.md).**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="0e75c-147">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-148">Tableau de types de châssis.</span><span class="sxs-lookup"><span data-stu-id="0e75c-148">Array of chassis types.</span></span>

<span data-ttu-id="0e75c-149">Cette valeur provient du membre **type** du **boîtier système ou** de la structure du châssis dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e75c-149">This value comes from the **Type** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e75c-150">Cette propriété est héritée [**du \_ châssis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-150">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e75c-151">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e75c-151">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e75c-152">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e75c-152">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="0e75c-153">**Bureau** (3)</span><span class="sxs-lookup"><span data-stu-id="0e75c-153">**Desktop** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="0e75c-154">**Bureau à profil bas** (4)</span><span class="sxs-lookup"><span data-stu-id="0e75c-154">**Low Profile Desktop** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="0e75c-155">**Boîte pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="0e75c-155">**Pizza Box** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="0e75c-156">**Mini tour** (6)</span><span class="sxs-lookup"><span data-stu-id="0e75c-156">**Mini Tower** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="0e75c-157">**Tour** (7)</span><span class="sxs-lookup"><span data-stu-id="0e75c-157">**Tower** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="0e75c-158">**Portable** (8)</span><span class="sxs-lookup"><span data-stu-id="0e75c-158">**Portable** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="0e75c-159">**Ordinateur portable** (9)</span><span class="sxs-lookup"><span data-stu-id="0e75c-159">**Laptop** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="0e75c-160">**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="0e75c-160">**Notebook** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="0e75c-161">**Tenu** à la main (11)</span><span class="sxs-lookup"><span data-stu-id="0e75c-161">**Hand Held** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="0e75c-162">**Station d’accueil** (12)</span><span class="sxs-lookup"><span data-stu-id="0e75c-162">**Docking Station** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="0e75c-163">**Tout-en-un** (13)</span><span class="sxs-lookup"><span data-stu-id="0e75c-163">**All in One** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="0e75c-164">**Sous-bloc-notes** (14)</span><span class="sxs-lookup"><span data-stu-id="0e75c-164">**Sub Notebook** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="0e75c-165">**Économise de l’espace** (15)</span><span class="sxs-lookup"><span data-stu-id="0e75c-165">**Space-Saving** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="0e75c-166">**Zone déjeuner** (16)</span><span class="sxs-lookup"><span data-stu-id="0e75c-166">**Lunch Box** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="0e75c-167">**Châssis principal du système** (17)</span><span class="sxs-lookup"><span data-stu-id="0e75c-167">**Main System Chassis** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="0e75c-168">**Châssis d’extension** (18)</span><span class="sxs-lookup"><span data-stu-id="0e75c-168">**Expansion Chassis** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="0e75c-169">Sous- **châssis** (19)</span><span class="sxs-lookup"><span data-stu-id="0e75c-169">**SubChassis** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="0e75c-170">**Châssis d’extension de bus** (20)</span><span class="sxs-lookup"><span data-stu-id="0e75c-170">**Bus Expansion Chassis** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="0e75c-171">**Châssis périphérique** (21)</span><span class="sxs-lookup"><span data-stu-id="0e75c-171">**Peripheral Chassis** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="0e75c-172">**Châssis de stockage** (22)</span><span class="sxs-lookup"><span data-stu-id="0e75c-172">**Storage Chassis** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="0e75c-173">**Châssis de montage en rack** (23)</span><span class="sxs-lookup"><span data-stu-id="0e75c-173">**Rack Mount Chassis** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="0e75c-174">**PC en boîtier scellé** (24)</span><span class="sxs-lookup"><span data-stu-id="0e75c-174">**Sealed-Case PC** (24)</span></span>

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

<span data-ttu-id="0e75c-175">**Tablette** (30)</span><span class="sxs-lookup"><span data-stu-id="0e75c-175">**Tablet** (30)</span></span>

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

<span data-ttu-id="0e75c-176">**Convertible** (31)</span><span class="sxs-lookup"><span data-stu-id="0e75c-176">**Convertible** (31)</span></span>

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

<span data-ttu-id="0e75c-177">**Détachable** (32)</span><span class="sxs-lookup"><span data-stu-id="0e75c-177">**Detachable** (32)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e75c-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e75c-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-181">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0e75c-181">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-182">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0e75c-182">Name of the first concrete class that appears in the inheritance chain that is used in the creation of an instance.</span></span> <span data-ttu-id="0e75c-183">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, cette propriété permet d’identifier toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-183">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="0e75c-184">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-184">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-185">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="0e75c-185">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-186">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="0e75c-186">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-188">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« ampères à 120 volts »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-188">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-189">Actuel requis par le châssis à 120 v.</span><span class="sxs-lookup"><span data-stu-id="0e75c-189">Current that is required by the chassis at 120V.</span></span> <span data-ttu-id="0e75c-190">Si l’alimentation est fournie par le châssis (comme dans le cas d’un onduleur), cette propriété peut indiquer l’intensité produite (sous la forme d’un nombre négatif).</span><span class="sxs-lookup"><span data-stu-id="0e75c-190">If power is provided by the chassis—as in the case of an uninterruptible power supply (UPS)—this property may indicate the amperage produced (as a negative number).</span></span>

<span data-ttu-id="0e75c-191">Cette propriété est héritée [**du \_ châssis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-191">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-192">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="0e75c-192">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-193">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="0e75c-193">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-195">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-195">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-196">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="0e75c-196">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="0e75c-197">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-197">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-198">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e75c-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-201">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="0e75c-201">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-202">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e75c-202">Description of the object.</span></span>

<span data-ttu-id="0e75c-203">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-204">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="0e75c-204">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-205">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e75c-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-207">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« BTU par heure »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-207">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-208">Quantité de chaleur générée par le châssis en BTU/heure.</span><span class="sxs-lookup"><span data-stu-id="0e75c-208">Amount of heat that is generated by the chassis in BTU/hour.</span></span>

<span data-ttu-id="0e75c-209">Cette propriété est héritée [**du \_ châssis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-209">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-210">**Height**</span><span class="sxs-lookup"><span data-stu-id="0e75c-210">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-211">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="0e75c-211">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-213">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-213">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-214">Hauteur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="0e75c-214">Height of the physical package—in inches.</span></span>

<span data-ttu-id="0e75c-215">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-215">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-216">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="0e75c-216">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-217">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e75c-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-219">Si la **valeur est true**, un package physique peut être échangé à chaud (s’il est possible de remplacer l’élément par un autre physiquement, mais équivalent, alors que le package qui le contient est alimenté).</span><span class="sxs-lookup"><span data-stu-id="0e75c-219">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="0e75c-220">Par exemple, un package de lecteur de disque inséré à l’aide de connecteurs SCA est amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="0e75c-220">For example, a disk drive package that is inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="0e75c-221">Tous les packages pouvant être échangés à chaud sont par nature amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="0e75c-221">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="0e75c-222">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-222">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-223">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e75c-223">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-224">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e75c-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-226">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="0e75c-226">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-227">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e75c-227">Date and time the object was installed.</span></span> <span data-ttu-id="0e75c-228">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="0e75c-228">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0e75c-229">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-230">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="0e75c-230">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e75c-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-233">Si la **valeur est true**, le frame est protégé par un verrou.</span><span class="sxs-lookup"><span data-stu-id="0e75c-233">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="0e75c-234">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-234">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-235">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="0e75c-235">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-238">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0e75c-238">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-239">Nom de l’organisation qui produit l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-239">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="0e75c-240">Cette valeur provient du membre du **fabricant** de la structure du **boîtier ou du châssis du système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e75c-240">This value comes from the **Manufacturer** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e75c-241">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-241">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-242">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="0e75c-242">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-245">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e75c-245">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-246">Nom par lequel l’élément physique est connu.</span><span class="sxs-lookup"><span data-stu-id="0e75c-246">Name by which the physical element is known.</span></span>

<span data-ttu-id="0e75c-247">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-247">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-248">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0e75c-248">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-251">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0e75c-251">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-252">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0e75c-252">Label by which the object is known.</span></span> <span data-ttu-id="0e75c-253">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="0e75c-253">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0e75c-254">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-255">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="0e75c-255">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-256">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e75c-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-258">Nombre de cordons d’alimentation qui doivent être connectés au châssis pour que tous les composants fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="0e75c-258">Number of power cords that must be connected to the chassis for all of the components to operate.</span></span>

<span data-ttu-id="0e75c-259">Cette propriété est héritée [**du \_ châssis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-259">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-260">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0e75c-260">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-263">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-263">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="0e75c-264">Par exemple, les données de code-barres sont associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="0e75c-264">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="0e75c-265">Sachez que si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, cette propriété serait **null** et les données de code-barres utilisées comme clé de classe, dans la propriété Tag.</span><span class="sxs-lookup"><span data-stu-id="0e75c-265">Be aware that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="0e75c-266">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-266">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-267">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="0e75c-267">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-268">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-270">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="0e75c-270">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-271">Numéro de référence affecté par l’organisation qui produit ou fabrique l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-271">Part number that is assigned by the organization that produces or manufacturing the physical element.</span></span>

<span data-ttu-id="0e75c-272">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-272">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-273">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="0e75c-273">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-274">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e75c-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-276">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="0e75c-276">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="0e75c-277">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-277">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-278">**Bande**</span><span class="sxs-lookup"><span data-stu-id="0e75c-278">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-279">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e75c-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-281">Si la **valeur est true**, un package physique est amovible (s’il est conçu pour être pris dans et hors du conteneur physique dans lequel il est normalement trouvé, sans altérer la fonction de l’empaquetage global).</span><span class="sxs-lookup"><span data-stu-id="0e75c-281">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="0e75c-282">Un package peut toujours être amovible si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="0e75c-282">A package can still be removable if the power must be "OFF" to perform the removal.</span></span> <span data-ttu-id="0e75c-283">Si le package peut être supprimé pendant que l’alimentation est activée, l’élément est amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="0e75c-283">If the package can be removed while the power is ON, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="0e75c-284">Par exemple, une batterie supplémentaire dans un ordinateur portable est amovible, comme c’est le cas pour un lecteur de disque inséré à l’aide de connecteurs de l’application de configuration de serveur (SCA).</span><span class="sxs-lookup"><span data-stu-id="0e75c-284">For example, an extra battery in a laptop is removable, as is a disk drive package that is inserted using Server Configuration Application (SCA) connectors.</span></span> <span data-ttu-id="0e75c-285">Toutefois, cette dernière peut être permutée à chaud.</span><span class="sxs-lookup"><span data-stu-id="0e75c-285">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="0e75c-286">L’affichage d’un ordinateur portable n’est pas amovible et n’est pas une alimentation non redondante.</span><span class="sxs-lookup"><span data-stu-id="0e75c-286">A laptop display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="0e75c-287">La suppression de ces composants affecterait la fonction de l’ensemble de l’empaquetage ou est impossible en raison de l’intégration étroite du package.</span><span class="sxs-lookup"><span data-stu-id="0e75c-287">Removing these components would affect the function of the overall packaging or is impossible because of the tight integration of the package.</span></span>

<span data-ttu-id="0e75c-288">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-288">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-289">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="0e75c-289">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-290">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e75c-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-292">Si la **valeur est true**, ce composant de média physique peut être remplacé par un autre physiquement différent.</span><span class="sxs-lookup"><span data-stu-id="0e75c-292">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="0e75c-293">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="0e75c-293">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="0e75c-294">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="0e75c-294">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="0e75c-295">Un autre exemple est un package d’alimentation monté sur des rails coulissants.</span><span class="sxs-lookup"><span data-stu-id="0e75c-295">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="0e75c-296">Tous les packages amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="0e75c-296">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="0e75c-297">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-297">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-298">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="0e75c-298">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-299">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e75c-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-301">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Table globale du conteneur physique DMTF \| 002,12 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="0e75c-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-302">État d’une violation physique du frame.</span><span class="sxs-lookup"><span data-stu-id="0e75c-302">Status of a physical breach of the frame.</span></span>

<span data-ttu-id="0e75c-303">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-303">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e75c-304">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e75c-304">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e75c-305">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e75c-305">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="0e75c-306">**Aucune violation** (3)</span><span class="sxs-lookup"><span data-stu-id="0e75c-306">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="0e75c-307">**Tentative de violation** (4)</span><span class="sxs-lookup"><span data-stu-id="0e75c-307">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="0e75c-308">**Violation réussie** (5)</span><span class="sxs-lookup"><span data-stu-id="0e75c-308">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e75c-309">**SecurityStatus**</span><span class="sxs-lookup"><span data-stu-id="0e75c-309">**SecurityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-310">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e75c-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-312">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| type 3 \| Security Status")</span><span class="sxs-lookup"><span data-stu-id="0e75c-312">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Security Status")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-313">Paramètre de sécurité pour une entrée externe, par exemple un clavier, sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e75c-313">Security setting for external input, for example, a keyboard, to a computer.</span></span>

<span data-ttu-id="0e75c-314">Cette valeur provient du membre **État de sécurité** de la structure **boîtier ou châssis du système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e75c-314">This value comes from the **Security Status** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e75c-315">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e75c-315">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e75c-316">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="0e75c-316">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0e75c-317">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="0e75c-317">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="0e75c-318">**Interface externe verrouillée** (4)</span><span class="sxs-lookup"><span data-stu-id="0e75c-318">**External interface locked out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="0e75c-319">**Interface externe activée** (5)</span><span class="sxs-lookup"><span data-stu-id="0e75c-319">**External interface enabled** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e75c-320">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="0e75c-320">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-323">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e75c-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-324">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-324">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="0e75c-325">Cette valeur provient du membre du **numéro de série** du **boîtier système ou** de la structure du châssis dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e75c-325">This value comes from the **Serial Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e75c-326">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-327">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0e75c-327">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-328">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0e75c-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-330">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="0e75c-330">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-331">Tableau d’explications plus détaillées sur toutes les entrées du tableau **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="0e75c-331">Array of more detailed explanations for any of the entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="0e75c-332">N’oubliez pas que chaque entrée de ce tableau est liée à l’entrée dans **ServicePhilosophy** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="0e75c-332">Be aware that each entry of this array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="0e75c-333">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-333">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-334">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="0e75c-334">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-335">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e75c-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-337">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="0e75c-337">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-338">Tableau qui indique si le cadre est pris en compte à partir du haut, du premier plan, de l’arrière ou du côté, si le cadre a des bacs coulissants ou des côtés amovibles, et si le cadre est déplaçable, par exemple avec des rouleaux.</span><span class="sxs-lookup"><span data-stu-id="0e75c-338">Array that includes whether the frame is serviced from the top, front, back, or side, whether the frame has sliding trays or removable sides, and whether the frame is moveable—for example, having rollers.</span></span>

<span data-ttu-id="0e75c-339">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-339">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e75c-340">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="0e75c-340">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0e75c-341">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="0e75c-341">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="0e75c-342">**Service à partir du haut** (2)</span><span class="sxs-lookup"><span data-stu-id="0e75c-342">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="0e75c-343">**Service à l’avant** (3)</span><span class="sxs-lookup"><span data-stu-id="0e75c-343">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="0e75c-344">**Service à partir de l’arrière** (4)</span><span class="sxs-lookup"><span data-stu-id="0e75c-344">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="0e75c-345">**Service de la côte** (5)</span><span class="sxs-lookup"><span data-stu-id="0e75c-345">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="0e75c-346">**Plateaux coulissants** (6)</span><span class="sxs-lookup"><span data-stu-id="0e75c-346">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="0e75c-347">**Côtés amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="0e75c-347">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="0e75c-348">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="0e75c-348">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e75c-349">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="0e75c-349">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-352">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e75c-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-353">Numéro d’unité de conservation de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-353">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="0e75c-354">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-355">**SMBIOSAssetTag**</span><span class="sxs-lookup"><span data-stu-id="0e75c-355">**SMBIOSAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-356">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-358">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| étiquette de ressource de type SMBIOS 3 \| ")</span><span class="sxs-lookup"><span data-stu-id="0e75c-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Asset Tag")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-359">Numéro d’identification du boîtier du système.</span><span class="sxs-lookup"><span data-stu-id="0e75c-359">Asset tag number of the system enclosure.</span></span>

<span data-ttu-id="0e75c-360">Cette valeur provient du membre **numéro d’identification** de la ressource du **boîtier système ou** de la structure du châssis dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e75c-360">This value comes from the **Asset Tag Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-361">**État**</span><span class="sxs-lookup"><span data-stu-id="0e75c-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-362">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-364">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="0e75c-364">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-365">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e75c-365">Current status of the object.</span></span> <span data-ttu-id="0e75c-366">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="0e75c-366">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0e75c-367">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="0e75c-367">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0e75c-368">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="0e75c-368">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0e75c-369">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="0e75c-369">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0e75c-370">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="0e75c-370">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0e75c-371">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0e75c-372">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e75c-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0e75c-373">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0e75c-374">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0e75c-375">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0e75c-376">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="0e75c-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0e75c-377">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0e75c-378">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0e75c-379">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0e75c-380">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0e75c-381">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0e75c-382">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0e75c-383">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0e75c-384">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e75c-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="0e75c-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-386">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-388">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="0e75c-388">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-389">Identificateur unique du boîtier système.</span><span class="sxs-lookup"><span data-stu-id="0e75c-389">Unique identifier of the system enclosure.</span></span>

<span data-ttu-id="0e75c-390">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-390">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="0e75c-391">Exemple : « boîtier système 1 »</span><span class="sxs-lookup"><span data-stu-id="0e75c-391">Example: "System Enclosure 1"</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-392">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0e75c-392">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-393">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0e75c-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-395">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexé"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ châssis CIM**](cim-chassis.md).**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="0e75c-395">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-396">Tableau d’informations supplémentaires sur les entrées du tableau **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="0e75c-396">Array of more information about the **ChassisTypes** array entries.</span></span> <span data-ttu-id="0e75c-397">N’oubliez pas que chaque entrée de ce tableau est liée à l’entrée dans **ChassisTypes** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="0e75c-397">Be aware that each entry of this array is related to the entry in **ChassisTypes** that is located at the same index.</span></span>

<span data-ttu-id="0e75c-398">Cette propriété est héritée [**du \_ châssis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-398">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-399">**Version**</span><span class="sxs-lookup"><span data-stu-id="0e75c-399">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e75c-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-401">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-402">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="0e75c-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-403">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="0e75c-403">Version of the physical element.</span></span>

<span data-ttu-id="0e75c-404">Cette valeur provient du membre **version** de la structure **boîtier ou châssis du système** dans les informations SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="0e75c-404">This value comes from the **Version** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="0e75c-405">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-405">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-406">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="0e75c-406">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-407">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0e75c-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-409">Si la **valeur est true**, l’équipement comprend une alarme visible.</span><span class="sxs-lookup"><span data-stu-id="0e75c-409">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="0e75c-410">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-410">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-411">**Poids**</span><span class="sxs-lookup"><span data-stu-id="0e75c-411">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-412">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="0e75c-412">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-414">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-414">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-415">Poids du package physique en livres.</span><span class="sxs-lookup"><span data-stu-id="0e75c-415">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="0e75c-416">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-416">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e75c-417">**Width**</span><span class="sxs-lookup"><span data-stu-id="0e75c-417">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e75c-418">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="0e75c-418">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e75c-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e75c-420">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="0e75c-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="0e75c-421">Largeur du package physique en pouces.</span><span class="sxs-lookup"><span data-stu-id="0e75c-421">Width of the physical package in inches.</span></span>

<span data-ttu-id="0e75c-422">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-422">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e75c-423">Notes</span><span class="sxs-lookup"><span data-stu-id="0e75c-423">Remarks</span></span>

<span data-ttu-id="0e75c-424">La classe **Win32 \_ SystemEnclosure** est dérivée [**du \_ châssis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="0e75c-424">The **Win32\_SystemEnclosure** class is derived from [**CIM\_Chassis**](cim-chassis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e75c-425">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e75c-425">Examples</span></span>

<span data-ttu-id="0e75c-426">L’exemple de [collecte des ressources système multithread avec](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell PowerShell sur la Galerie TechNet utilise un certain nombre de classes, notamment **Win32 \_ SystemEnclosure**, pour récupérer des données d’un système.</span><span class="sxs-lookup"><span data-stu-id="0e75c-426">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell example on TechNet gallery uses a number of classes, including **Win32\_SystemEnclosure**, to retrieve data from a system.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e75c-427">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e75c-427">Requirements</span></span>



| <span data-ttu-id="0e75c-428">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e75c-428">Requirement</span></span> | <span data-ttu-id="0e75c-429">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e75c-429">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e75c-430">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e75c-430">Minimum supported client</span></span><br/> | <span data-ttu-id="0e75c-431">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e75c-431">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e75c-432">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e75c-432">Minimum supported server</span></span><br/> | <span data-ttu-id="0e75c-433">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e75c-433">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e75c-434">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e75c-434">Namespace</span></span><br/>                | <span data-ttu-id="0e75c-435">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0e75c-435">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e75c-436">MOF</span><span class="sxs-lookup"><span data-stu-id="0e75c-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e75c-437"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e75c-437"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e75c-438">DLL</span><span class="sxs-lookup"><span data-stu-id="0e75c-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e75c-439"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e75c-439"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e75c-440">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e75c-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e75c-441">**\_Châssis CIM**</span><span class="sxs-lookup"><span data-stu-id="0e75c-441">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="0e75c-442">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="0e75c-442">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0e75c-443">Tâches WMI : matériel de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="0e75c-443">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
