---
description: La \_ classe de châssis CIM représente les éléments physiques qui englobent d’autres éléments et fournissent des fonctionnalités définissables, telles qu’un ordinateur de bureau, un nœud de traitement, des onduleurs, un stockage sur disque ou sur bande, ou une combinaison de ces éléments.
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: Classe CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110999"
---
# <a name="cim_chassis-class"></a><span data-ttu-id="02248-103">\_Classe de châssis CIM</span><span class="sxs-lookup"><span data-stu-id="02248-103">CIM\_Chassis class</span></span>

<span data-ttu-id="02248-104">La classe de **\_ châssis CIM** représente les éléments physiques qui englobent d’autres éléments et fournissent des fonctionnalités définissables, telles qu’un ordinateur de bureau, un nœud de traitement, des onduleurs, un stockage sur disque ou sur bande, ou une combinaison de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="02248-104">The **CIM\_Chassis** class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02248-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="02248-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="02248-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="02248-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="02248-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="02248-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="02248-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="02248-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02248-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02248-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
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
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="02248-110">Membres</span><span class="sxs-lookup"><span data-stu-id="02248-110">Members</span></span>

<span data-ttu-id="02248-111">La classe de **\_ châssis CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="02248-111">The **CIM\_Chassis** class has these types of members:</span></span>

-   [<span data-ttu-id="02248-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="02248-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="02248-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="02248-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="02248-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="02248-114">Methods</span></span>

<span data-ttu-id="02248-115">La classe de **\_ châssis CIM** présente ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="02248-115">The **CIM\_Chassis** class has these methods.</span></span>



| <span data-ttu-id="02248-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="02248-116">Method</span></span>                                                           | <span data-ttu-id="02248-117">Description</span><span class="sxs-lookup"><span data-stu-id="02248-117">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02248-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="02248-118">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-chassis.md) | <span data-ttu-id="02248-119">Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="02248-119">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="02248-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="02248-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="02248-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="02248-121">Properties</span></span>

<span data-ttu-id="02248-122">La classe de **\_ châssis CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="02248-122">The **CIM\_Chassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02248-123">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="02248-123">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-124">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="02248-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02248-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-126">Si la **valeur est true**, le cadre est équipé d’une alarme sonore.</span><span class="sxs-lookup"><span data-stu-id="02248-126">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="02248-127">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-127">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="02248-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="02248-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="02248-132">Chaîne de forme libre qui fournit plus d’informations si la propriété **SecurityBreach** indique qu’une violation ou un autre événement lié à la sécurité s’est produit.</span><span class="sxs-lookup"><span data-stu-id="02248-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="02248-133">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-133">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-134">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="02248-134">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-137">Chaîne de forme libre qui contient des informations sur la façon dont les différents câbles sont connectés et regroupés pour le cadre.</span><span class="sxs-lookup"><span data-stu-id="02248-137">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="02248-138">Avec de nombreuses connexions réseau, liées au stockage et aux câbles d’alimentation, la gestion des câbles peut être un défi complexe et difficile.</span><span class="sxs-lookup"><span data-stu-id="02248-138">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="02248-139">Cette propriété de type chaîne contient des informations pour faciliter l’assembly et le service du frame.</span><span class="sxs-lookup"><span data-stu-id="02248-139">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="02248-140">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-140">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="02248-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-144">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="02248-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="02248-145">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="02248-145">A short textual description of the object.</span></span>

<span data-ttu-id="02248-146">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-147">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="02248-147">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02248-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="02248-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-150">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Table globale du conteneur physique DMTF \| 002,1 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ châssis CIM**.**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="02248-150">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="02248-151">Tableau énuméré, à valeurs entières, qui indique le type de châssis.</span><span class="sxs-lookup"><span data-stu-id="02248-151">Enumerated, integer-valued array that indicates the type of chassis.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="02248-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="02248-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="02248-153">Autre.</span><span class="sxs-lookup"><span data-stu-id="02248-153">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02248-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="02248-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="02248-155">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="02248-155">Unknown.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="02248-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Bureau** (3)</span><span class="sxs-lookup"><span data-stu-id="02248-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span></span>


</dt> <dd>

<span data-ttu-id="02248-157">Bureau.</span><span class="sxs-lookup"><span data-stu-id="02248-157">Desktop.</span></span>

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="02248-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Bureau à profil bas** (4)</span><span class="sxs-lookup"><span data-stu-id="02248-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Low Profile Desktop** (4)</span></span>


</dt> <dd>

<span data-ttu-id="02248-159">Bureau à profil bas.</span><span class="sxs-lookup"><span data-stu-id="02248-159">Low-profile desktop.</span></span>

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="02248-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Boîte pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="02248-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span></span>


</dt> <dd>

<span data-ttu-id="02248-161">Boîte pizza.</span><span class="sxs-lookup"><span data-stu-id="02248-161">Pizza box.</span></span>

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="02248-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini tour** (6)</span><span class="sxs-lookup"><span data-stu-id="02248-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Tower** (6)</span></span>


</dt> <dd>

<span data-ttu-id="02248-163">Mini tour.</span><span class="sxs-lookup"><span data-stu-id="02248-163">Mini tower.</span></span>

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="02248-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tour** (7)</span><span class="sxs-lookup"><span data-stu-id="02248-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span></span>


</dt> <dd>

<span data-ttu-id="02248-165">Tour.</span><span class="sxs-lookup"><span data-stu-id="02248-165">Tower.</span></span>

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="02248-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span><span class="sxs-lookup"><span data-stu-id="02248-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span></span>


</dt> <dd>

<span data-ttu-id="02248-167">Portatif.</span><span class="sxs-lookup"><span data-stu-id="02248-167">Portable.</span></span>

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="02248-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Ordinateur portable** (9)</span><span class="sxs-lookup"><span data-stu-id="02248-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span></span>


</dt> <dd>

<span data-ttu-id="02248-169">Ordinateur portable.</span><span class="sxs-lookup"><span data-stu-id="02248-169">Laptop.</span></span>

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="02248-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="02248-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span></span>


</dt> <dd>

<span data-ttu-id="02248-171">Équipés.</span><span class="sxs-lookup"><span data-stu-id="02248-171">Notebook.</span></span>

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="02248-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Tenu** à la main (11)</span><span class="sxs-lookup"><span data-stu-id="02248-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)</span></span>


</dt> <dd>

<span data-ttu-id="02248-173">Tenu à la main.</span><span class="sxs-lookup"><span data-stu-id="02248-173">Hand-held.</span></span>

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="02248-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Station d’accueil** (12)</span><span class="sxs-lookup"><span data-stu-id="02248-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span></span>


</dt> <dd>

<span data-ttu-id="02248-175">Station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="02248-175">Docking station.</span></span>

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="02248-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Tout-en-un** (13)</span><span class="sxs-lookup"><span data-stu-id="02248-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**All in One** (13)</span></span>


</dt> <dd>

<span data-ttu-id="02248-177">Tout-en-un.</span><span class="sxs-lookup"><span data-stu-id="02248-177">All-in-one.</span></span>

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="02248-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sous-bloc-notes** (14)</span><span class="sxs-lookup"><span data-stu-id="02248-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span></span>


</dt> <dd>

<span data-ttu-id="02248-179">Sous-bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="02248-179">Subnotebook.</span></span>

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="02248-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Économise de l’espace** (15)</span><span class="sxs-lookup"><span data-stu-id="02248-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Space-Saving** (15)</span></span>


</dt> <dd>

<span data-ttu-id="02248-181">Économise de l’espace.</span><span class="sxs-lookup"><span data-stu-id="02248-181">Space-saving.</span></span>

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="02248-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Zone déjeuner** (16)</span><span class="sxs-lookup"><span data-stu-id="02248-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="02248-183">Zone déjeuner.</span><span class="sxs-lookup"><span data-stu-id="02248-183">Lunch box.</span></span>

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="02248-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Châssis principal du système** (17)</span><span class="sxs-lookup"><span data-stu-id="02248-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Main System Chassis** (17)</span></span>


</dt> <dd>

<span data-ttu-id="02248-185">Châssis principal du système.</span><span class="sxs-lookup"><span data-stu-id="02248-185">Main system chassis.</span></span>

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="02248-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Châssis d’extension** (18)</span><span class="sxs-lookup"><span data-stu-id="02248-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Expansion Chassis** (18)</span></span>


</dt> <dd>

<span data-ttu-id="02248-187">Châssis d’extension.</span><span class="sxs-lookup"><span data-stu-id="02248-187">Expansion chassis.</span></span>

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="02248-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>Sous- **châssis** (19)</span><span class="sxs-lookup"><span data-stu-id="02248-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)</span></span>


</dt> <dd>

<span data-ttu-id="02248-189">Sous-châssis.</span><span class="sxs-lookup"><span data-stu-id="02248-189">Subchassis.</span></span>

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="02248-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Châssis d’extension de bus** (20)</span><span class="sxs-lookup"><span data-stu-id="02248-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Bus Expansion Chassis** (20)</span></span>


</dt> <dd>

<span data-ttu-id="02248-191">Châssis d’extension de bus.</span><span class="sxs-lookup"><span data-stu-id="02248-191">Bus-expansion chassis.</span></span>

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="02248-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Châssis périphérique** (21)</span><span class="sxs-lookup"><span data-stu-id="02248-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripheral Chassis** (21)</span></span>


</dt> <dd>

<span data-ttu-id="02248-193">Châssis périphérique.</span><span class="sxs-lookup"><span data-stu-id="02248-193">Peripheral chassis.</span></span>

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="02248-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Châssis de stockage** (22)</span><span class="sxs-lookup"><span data-stu-id="02248-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage Chassis** (22)</span></span>


</dt> <dd>

<span data-ttu-id="02248-195">Châssis de stockage.</span><span class="sxs-lookup"><span data-stu-id="02248-195">Storage chassis.</span></span>

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="02248-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Châssis de montage en rack** (23)</span><span class="sxs-lookup"><span data-stu-id="02248-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span></span>


</dt> <dd>

<span data-ttu-id="02248-197">Châssis monté en rack.</span><span class="sxs-lookup"><span data-stu-id="02248-197">Rack-mount chassis.</span></span>

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="02248-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**PC en boîtier scellé** (24)</span><span class="sxs-lookup"><span data-stu-id="02248-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case PC** (24)</span></span>


</dt> <dd>

<span data-ttu-id="02248-199">Ordinateur scellé.</span><span class="sxs-lookup"><span data-stu-id="02248-199">Sealed-case computer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="02248-200">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="02248-200">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-203">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="02248-203">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="02248-204">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="02248-204">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="02248-205">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="02248-205">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="02248-206">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-207">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="02248-207">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-208">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="02248-208">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="02248-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-210">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« ampères à 120 volts »)</span><span class="sxs-lookup"><span data-stu-id="02248-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="02248-211">Actuellement requis par le châssis à 120 volts.</span><span class="sxs-lookup"><span data-stu-id="02248-211">Currently required by the chassis at 120 volts.</span></span> <span data-ttu-id="02248-212">Si l’alimentation est fournie par le châssis (comme dans le cas d’un onduleur), cette propriété peut indiquer l’intensité produite, sous la forme d’un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="02248-212">If power is provided by the chassis (as in the case of a UPS), this property can indicate the amperage produced, as a negative number.</span></span>

</dd> <dt>

<span data-ttu-id="02248-213">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="02248-213">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-214">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="02248-214">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="02248-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-216">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="02248-216">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="02248-217">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="02248-217">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="02248-218">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="02248-218">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-219">**Description**</span><span class="sxs-lookup"><span data-stu-id="02248-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-222">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="02248-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="02248-223">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="02248-223">A textual description of the object.</span></span>

<span data-ttu-id="02248-224">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-225">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="02248-225">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-226">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02248-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="02248-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-228">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« BTU par heure »)</span><span class="sxs-lookup"><span data-stu-id="02248-228">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="02248-229">Quantité de chaleur générée par le châssis en BTU/heure.</span><span class="sxs-lookup"><span data-stu-id="02248-229">Amount of heat generated by the chassis in Btu/hour.</span></span>

</dd> <dt>

<span data-ttu-id="02248-230">**Height**</span><span class="sxs-lookup"><span data-stu-id="02248-230">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-231">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="02248-231">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="02248-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-233">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="02248-233">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="02248-234">Hauteur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="02248-234">Height of the physical package, in inches.</span></span>

<span data-ttu-id="02248-235">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="02248-235">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-236">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="02248-236">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-237">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="02248-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02248-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-239">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="02248-239">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="02248-240">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="02248-240">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="02248-241">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="02248-241">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="02248-242">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="02248-242">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="02248-243">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="02248-243">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-244">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="02248-244">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-245">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="02248-245">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="02248-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-247">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="02248-247">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="02248-248">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="02248-248">Indicates when the object was installed.</span></span> <span data-ttu-id="02248-249">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="02248-249">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="02248-250">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-250">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-251">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="02248-251">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-252">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="02248-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02248-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-254">Si la **valeur est true**, le frame est protégé par un verrou.</span><span class="sxs-lookup"><span data-stu-id="02248-254">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="02248-255">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-255">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-256">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="02248-256">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-259">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="02248-259">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="02248-260">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="02248-260">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="02248-261">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="02248-261">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="02248-262">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-263">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="02248-263">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-266">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="02248-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="02248-267">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="02248-267">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="02248-268">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-269">**Nom**</span><span class="sxs-lookup"><span data-stu-id="02248-269">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-272">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="02248-272">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="02248-273">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="02248-273">Label by which the object is known.</span></span> <span data-ttu-id="02248-274">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="02248-274">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="02248-275">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-276">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="02248-276">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-277">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02248-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="02248-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-279">Nombre de cordons d’alimentation qui doivent être connectés au châssis afin que tous les composants puissent fonctionner.</span><span class="sxs-lookup"><span data-stu-id="02248-279">Number of power cords that must be connected to the chassis so that all of the components can operate.</span></span>

</dd> <dt>

<span data-ttu-id="02248-280">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="02248-280">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-283">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="02248-283">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="02248-284">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="02248-284">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="02248-285">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="02248-285">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="02248-286">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-287">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="02248-287">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-290">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="02248-290">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="02248-291">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="02248-291">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="02248-292">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-293">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="02248-293">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-294">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="02248-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02248-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-296">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="02248-296">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="02248-297">Dans le cas contraire, elle est actuellement désactivée.</span><span class="sxs-lookup"><span data-stu-id="02248-297">Otherwise, it is currently off.</span></span>

<span data-ttu-id="02248-298">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-299">**Bande**</span><span class="sxs-lookup"><span data-stu-id="02248-299">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-300">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="02248-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02248-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-302">Si la **valeur est true**, le package est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="02248-302">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="02248-303">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="02248-303">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="02248-304">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="02248-304">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="02248-305">Par exemple, une puce de processeur extensible est amovible.</span><span class="sxs-lookup"><span data-stu-id="02248-305">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="02248-306">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="02248-306">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-307">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="02248-307">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-308">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="02248-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02248-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-310">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="02248-310">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="02248-311">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="02248-311">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="02248-312">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="02248-312">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="02248-313">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="02248-313">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="02248-314">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="02248-314">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-315">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="02248-315">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-316">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02248-316">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="02248-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-318">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Table globale du conteneur physique DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="02248-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="02248-319">Indique si une violation physique du frame a été tentée, mais a échoué ou a été tentée et réussie.</span><span class="sxs-lookup"><span data-stu-id="02248-319">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<span data-ttu-id="02248-320">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-320">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="02248-321">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="02248-321">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02248-322">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="02248-322">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="02248-323">**Aucune violation** (3)</span><span class="sxs-lookup"><span data-stu-id="02248-323">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="02248-324">**Tentative de violation** (4)</span><span class="sxs-lookup"><span data-stu-id="02248-324">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="02248-325">**Violation réussie** (5)</span><span class="sxs-lookup"><span data-stu-id="02248-325">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02248-326">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="02248-326">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-327">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-329">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="02248-329">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="02248-330">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="02248-330">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="02248-331">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-331">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-332">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="02248-332">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-333">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="02248-333">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="02248-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-335">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="02248-335">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="02248-336">Chaînes de forme libre qui fournissent des explications détaillées sur les entrées dans le tableau **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="02248-336">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="02248-337">Chaque entrée de ce tableau est liée à l’entrée dans le tableau **ServicePhilosophy** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="02248-337">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

<span data-ttu-id="02248-338">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-338">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-339">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="02248-339">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-340">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02248-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="02248-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-342">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="02248-342">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="02248-343">Indique si le frame est pris en service à partir du haut, de l’avant, de l’arrière ou du côté ; et s’il a des bacs coulissants ou des côtés amovibles, et si le cadre est mobile (par exemple, des rouleaux).</span><span class="sxs-lookup"><span data-stu-id="02248-343">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="02248-344">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-344">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02248-345">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="02248-345">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="02248-346">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="02248-346">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="02248-347">**Service à partir du haut** (2)</span><span class="sxs-lookup"><span data-stu-id="02248-347">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="02248-348">**Service à l’avant** (3)</span><span class="sxs-lookup"><span data-stu-id="02248-348">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="02248-349">**Service à partir de l’arrière** (4)</span><span class="sxs-lookup"><span data-stu-id="02248-349">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="02248-350">**Service de la côte** (5)</span><span class="sxs-lookup"><span data-stu-id="02248-350">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="02248-351">**Plateaux coulissants** (6)</span><span class="sxs-lookup"><span data-stu-id="02248-351">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="02248-352">**Côtés amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="02248-352">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="02248-353">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="02248-353">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02248-354">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="02248-354">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-357">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="02248-357">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="02248-358">Numéro d’unité de conservation pour cet élément physique.</span><span class="sxs-lookup"><span data-stu-id="02248-358">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="02248-359">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-359">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-360">**État**</span><span class="sxs-lookup"><span data-stu-id="02248-360">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-363">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="02248-363">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="02248-364">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="02248-364">String that indicates the current status of the object.</span></span> <span data-ttu-id="02248-365">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="02248-365">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="02248-366">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="02248-366">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="02248-367">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="02248-367">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="02248-368">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="02248-368">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="02248-369">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="02248-369">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="02248-370">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="02248-370">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="02248-371">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="02248-372">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="02248-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="02248-373">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="02248-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="02248-374">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="02248-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="02248-375">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="02248-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02248-376">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="02248-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="02248-377">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="02248-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="02248-378">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="02248-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="02248-379">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="02248-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="02248-380">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="02248-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="02248-381">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="02248-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="02248-382">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="02248-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="02248-383">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="02248-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="02248-384">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="02248-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02248-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="02248-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-386">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-388">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="02248-388">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="02248-389">Identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="02248-389">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="02248-390">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="02248-390">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="02248-391">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="02248-391">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="02248-392">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="02248-392">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="02248-393">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="02248-393">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="02248-394">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="02248-394">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="02248-395">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-395">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-396">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="02248-396">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-397">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="02248-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="02248-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-399">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ châssis CIM**.**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="02248-399">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="02248-400">Tableau de chaînes de forme libre qui fournit des informations sur les entrées du tableau **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="02248-400">Array of free-form strings that provides information about the **ChassisTypes** array entries.</span></span>

> [!Note]  
> <span data-ttu-id="02248-401">Chaque entrée de tableau est liée à l’entrée dans la propriété **ChassisTypes** , qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="02248-401">Each array entry is related to the entry in the **ChassisTypes** property, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="02248-402">**Version**</span><span class="sxs-lookup"><span data-stu-id="02248-402">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="02248-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02248-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-405">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="02248-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="02248-406">Indique la version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="02248-406">Indicates the version of the physical element.</span></span>

<span data-ttu-id="02248-407">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="02248-407">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-408">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="02248-408">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-409">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="02248-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02248-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02248-411">Si la **valeur est true**, l’équipement comprend une alarme visible.</span><span class="sxs-lookup"><span data-stu-id="02248-411">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="02248-412">Cette propriété est héritée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-412">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-413">**Poids**</span><span class="sxs-lookup"><span data-stu-id="02248-413">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-414">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="02248-414">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="02248-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-416">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="02248-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="02248-417">Poids du package physique, en livres.</span><span class="sxs-lookup"><span data-stu-id="02248-417">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="02248-418">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="02248-418">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="02248-419">**Width**</span><span class="sxs-lookup"><span data-stu-id="02248-419">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02248-420">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="02248-420">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="02248-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02248-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02248-422">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="02248-422">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="02248-423">Largeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="02248-423">Width of the physical package, in inches.</span></span>

<span data-ttu-id="02248-424">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="02248-424">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02248-425">Notes</span><span class="sxs-lookup"><span data-stu-id="02248-425">Remarks</span></span>

<span data-ttu-id="02248-426">La classe de **\_ châssis CIM** est dérivée de la [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="02248-426">The **CIM\_Chassis** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="02248-427">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="02248-427">WMI does not implement this class.</span></span> <span data-ttu-id="02248-428">Pour plus d’informations sur les classes dérivées du **\_ châssis CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="02248-428">For more information about classes derived from **CIM\_Chassis**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="02248-429">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="02248-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="02248-430">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="02248-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02248-431">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02248-431">Requirements</span></span>



| <span data-ttu-id="02248-432">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02248-432">Requirement</span></span> | <span data-ttu-id="02248-433">Valeur</span><span class="sxs-lookup"><span data-stu-id="02248-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02248-434">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02248-434">Minimum supported client</span></span><br/> | <span data-ttu-id="02248-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02248-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02248-436">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02248-436">Minimum supported server</span></span><br/> | <span data-ttu-id="02248-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02248-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02248-438">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02248-438">Namespace</span></span><br/>                | <span data-ttu-id="02248-439">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="02248-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02248-440">MOF</span><span class="sxs-lookup"><span data-stu-id="02248-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02248-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02248-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02248-442">DLL</span><span class="sxs-lookup"><span data-stu-id="02248-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02248-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02248-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02248-444">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02248-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02248-445">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="02248-445">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

