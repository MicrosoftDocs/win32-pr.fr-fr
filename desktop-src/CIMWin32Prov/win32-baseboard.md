---
description: Représente une carte de bureau, également appelée carte mère ou carte système.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Classe Win32_BaseBoard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033768"
---
# <a name="win32_baseboard-class"></a><span data-ttu-id="b8875-103">\_Classe Baseboard de Win32</span><span class="sxs-lookup"><span data-stu-id="b8875-103">Win32\_BaseBoard class</span></span>

<span data-ttu-id="b8875-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **carte de \_ carte Win32** représente une carte mère, également appelée carte mère ou carte système.</span><span class="sxs-lookup"><span data-stu-id="b8875-104">The **Win32\_BaseBoard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a baseboard, which is also known as a motherboard or system board.</span></span>

<span data-ttu-id="b8875-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b8875-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8875-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8875-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="b8875-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b8875-107">Members</span></span>

<span data-ttu-id="b8875-108">La **classe \_ Baseboard de Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8875-108">The **Win32\_BaseBoard** class has these types of members:</span></span>

-   [<span data-ttu-id="b8875-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8875-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8875-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8875-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8875-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8875-111">Methods</span></span>

<span data-ttu-id="b8875-112">La **classe \_ Baseboard de Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b8875-112">The **Win32\_BaseBoard** class has these methods.</span></span>



| <span data-ttu-id="b8875-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="b8875-113">Method</span></span>           | <span data-ttu-id="b8875-114">Description</span><span class="sxs-lookup"><span data-stu-id="b8875-114">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="b8875-115">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="b8875-115">**IsCompatible**</span></span> | <span data-ttu-id="b8875-116">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b8875-116">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8875-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b8875-117">Properties</span></span>

<span data-ttu-id="b8875-118">La **classe \_ Baseboard de Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b8875-118">The **Win32\_BaseBoard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8875-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b8875-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-122">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="b8875-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-123">Description succincte de l’objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="b8875-123">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b8875-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-125">**ConfigOptions**</span><span class="sxs-lookup"><span data-stu-id="b8875-125">**ConfigOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-126">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="b8875-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8875-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-128">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 12 \| configuration options Strings")</span><span class="sxs-lookup"><span data-stu-id="b8875-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 12\|Configuration Options Strings")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-129">Tableau qui représente la configuration des cavaliers et des commutateurs situés sur la carte de carte.</span><span class="sxs-lookup"><span data-stu-id="b8875-129">Array that represents the configuration of the jumpers and switches located on the baseboard.</span></span>

<span data-ttu-id="b8875-130">Exemple : « JP2 : la taille du cache 1-2 est de 256 Ko, 2-3 taille du cache est de 512 Ko, SW1-1 : fermer pour désactiver la vidéo à la carte »</span><span class="sxs-lookup"><span data-stu-id="b8875-130">Example: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"</span></span>

</dd> <dt>

<span data-ttu-id="b8875-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8875-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-134">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b8875-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8875-135">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="b8875-135">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b8875-136">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="b8875-136">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b8875-137">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-138">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="b8875-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-139">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="b8875-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-141">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="b8875-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-142">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="b8875-142">Depth of the physical package in inches.</span></span>

<span data-ttu-id="b8875-143">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-143">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8875-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-147">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b8875-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-148">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b8875-148">Description of the object.</span></span>

<span data-ttu-id="b8875-149">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-150">**Height**</span><span class="sxs-lookup"><span data-stu-id="b8875-150">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-151">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="b8875-151">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-153">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="b8875-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-154">Hauteur du package physique en pouces.</span><span class="sxs-lookup"><span data-stu-id="b8875-154">Height of the physical package in inches.</span></span>

<span data-ttu-id="b8875-155">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-155">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-156">**Hébergement**</span><span class="sxs-lookup"><span data-stu-id="b8875-156">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-157">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b8875-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-159">Si la **valeur est true**, la carte est une carte mère ou une carte de carte dans un châssis.</span><span class="sxs-lookup"><span data-stu-id="b8875-159">If **TRUE**, the card is a motherboard, or a baseboard in a chassis.</span></span>

<span data-ttu-id="b8875-160">Cette propriété est héritée de la [**\_ carte CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-160">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-161">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="b8875-161">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-162">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b8875-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-164">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="b8875-164">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="b8875-165">Un package physique peut être permuté à chaud s’il est possible de remplacer l’élément par un élément équivalent physiquement différent, tandis que le package conteneur a une alimentation qui lui est appliquée, alors qu’il est activé.</span><span class="sxs-lookup"><span data-stu-id="b8875-165">A physical package can be hot-swapped if it is possible to replace the element with a physically different but equivalent element while the containing package has power applied to it that is, while it is ON.</span></span> <span data-ttu-id="b8875-166">Par exemple, un package de lecteur de disque inséré à l’aide de connecteurs SCA est amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="b8875-166">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="b8875-167">Tous les packages pouvant être échangés à chaud sont par nature amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="b8875-167">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="b8875-168">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-169">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8875-169">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-170">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8875-170">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-172">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="b8875-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-173">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b8875-173">Date and time the object was installed.</span></span> <span data-ttu-id="b8875-174">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="b8875-174">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b8875-175">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-175">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-176">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="b8875-176">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-179">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b8875-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8875-180">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b8875-180">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="b8875-181">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-181">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-182">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="b8875-182">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-185">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8875-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8875-186">Nom par lequel l’élément physique est connu.</span><span class="sxs-lookup"><span data-stu-id="b8875-186">Name by which the physical element is known.</span></span>

<span data-ttu-id="b8875-187">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-187">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-188">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b8875-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-191">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b8875-191">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-192">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="b8875-192">Label by which the object is known.</span></span> <span data-ttu-id="b8875-193">Lorsqu’elle est sous-classée, la propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="b8875-193">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b8875-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-195">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b8875-195">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-198">Capture des données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="b8875-198">Captures additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="b8875-199">Par exemple, les données de code-barres sont associées à un élément qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="b8875-199">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="b8875-200">Notez que si seules les données de code-barres sont disponibles et uniques ou peuvent être utilisées comme clé d’élément, la valeur de propriété serait **null** et les données de code de barre seraient utilisées comme clé de classe, dans la propriété Tag.</span><span class="sxs-lookup"><span data-stu-id="b8875-200">Note that if only bar code data is available and unique or able to be used as an element key, the property value would be **NULL** and the bar code data would be used as the class key, in the tag property.</span></span>

<span data-ttu-id="b8875-201">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-202">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="b8875-202">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-205">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b8875-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8875-206">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b8875-206">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="b8875-207">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-207">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-208">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="b8875-208">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-209">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b8875-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-211">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="b8875-211">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="b8875-212">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-213">**Produit**</span><span class="sxs-lookup"><span data-stu-id="b8875-213">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-216">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| type 2 \| Product")</span><span class="sxs-lookup"><span data-stu-id="b8875-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 2\|Product")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-217">Numéro de référence de la carte mère défini par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="b8875-217">Baseboard part number defined by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b8875-218">**Bande**</span><span class="sxs-lookup"><span data-stu-id="b8875-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b8875-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-221">Si la **valeur est true**, un package est amovible.</span><span class="sxs-lookup"><span data-stu-id="b8875-221">If **TRUE**, a package is removable.</span></span> <span data-ttu-id="b8875-222">Un package physique est amovible s’il est conçu pour être mis à l’extérieur du conteneur physique dans lequel il est normalement trouvé sans altérer la fonction de l’ensemble de l’empaquetage.</span><span class="sxs-lookup"><span data-stu-id="b8875-222">A physical package is removable if it is designed to be taken in and out of the physical container in which it is normally found without impairing the function of the overall packaging.</span></span> <span data-ttu-id="b8875-223">Un package peut toujours être amovible si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="b8875-223">A package can still be removable if the power must be OFF to perform the removal.</span></span> <span data-ttu-id="b8875-224">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="b8875-224">If the power can be ON and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="b8875-225">Par exemple, une batterie supplémentaire dans un ordinateur portable est amovible, comme c’est le cas d’un package de lecteur de disque inséré à l’aide de connecteurs SCA.</span><span class="sxs-lookup"><span data-stu-id="b8875-225">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="b8875-226">Toutefois, ce dernier peut également être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="b8875-226">However, the latter can also be hot-swapped.</span></span> <span data-ttu-id="b8875-227">L’affichage d’un ordinateur portable n’est pas amovible et n’est pas une alimentation non redondante.</span><span class="sxs-lookup"><span data-stu-id="b8875-227">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="b8875-228">La suppression de ces composants affecterait la fonction de l’ensemble du Packaging ou est impossible en raison de l’intégration étroite du package.</span><span class="sxs-lookup"><span data-stu-id="b8875-228">Removing these components would impact the function of the overall packaging, or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="b8875-229">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-229">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-230">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="b8875-230">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b8875-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-233">Si la **valeur est true**, un package est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="b8875-233">If **TRUE**, a package is replaceable.</span></span> <span data-ttu-id="b8875-234">Un package physique est remplaçable s’il est possible de remplacer (FRU ou Upgrade) l’élément avec un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="b8875-234">A physical package is replaceable if it is possible to replace (FRU or upgrade) the element with a physically different one.</span></span> <span data-ttu-id="b8875-235">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="b8875-235">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="b8875-236">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="b8875-236">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="b8875-237">Un autre exemple est un package d’alimentation monté sur des rails coulissants.</span><span class="sxs-lookup"><span data-stu-id="b8875-237">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="b8875-238">Tous les packages amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="b8875-238">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="b8875-239">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-239">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-240">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="b8875-240">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-243">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ carte CIM**](cim-card.md).**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="b8875-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-244">Chaîne de forme libre qui décrit la façon dont cette carte est physiquement unique à partir d’autres cartes.</span><span class="sxs-lookup"><span data-stu-id="b8875-244">Free-form string that describes the way in which this card is physically unique from other cards.</span></span> <span data-ttu-id="b8875-245">La propriété n’a de signification que lorsque la propriété booléenne correspondante **SpecialRequirements** a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="b8875-245">The property only has meaning when the corresponding Boolean property **SpecialRequirements** is set to **TRUE**.</span></span>

<span data-ttu-id="b8875-246">Cette propriété est héritée de la [**\_ carte CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-246">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-247">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="b8875-247">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-248">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b8875-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-250">Si la **valeur est true**, au moins une carte fille ou auxiliaire est nécessaire pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="b8875-250">If **TRUE**, at least one daughterboard or auxiliary card is required to function properly.</span></span>

<span data-ttu-id="b8875-251">Cette propriété est héritée de la [**\_ carte CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-251">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-252">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b8875-252">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-255">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8875-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8875-256">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b8875-256">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="b8875-257">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-258">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="b8875-258">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-259">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-261">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8875-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8875-262">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b8875-262">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="b8875-263">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-264">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="b8875-264">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-265">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8875-267">Chaîne de forme libre qui décrit la position de l’emplacement, l’utilisation typique, les restrictions, l’espacement de l’emplacement individuel ou toute autre information pertinente pour les emplacements sur une carte.</span><span class="sxs-lookup"><span data-stu-id="b8875-267">Free-form string that describes the slot position, typical usage, restrictions, individual slot spacing or any other pertinent information for the slots on a card.</span></span>

<span data-ttu-id="b8875-268">Cette propriété est héritée de la [**\_ carte CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-268">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-269">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="b8875-269">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-270">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b8875-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-272">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ carte CIM**](cim-card.md).**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="b8875-272">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-273">Si la **valeur est true**, cette carte est physiquement unique des autres cartes du même type et requiert donc un emplacement spécial.</span><span class="sxs-lookup"><span data-stu-id="b8875-273">If **TRUE**, this card is physically unique from other cards of the same type and therefore requires a special slot.</span></span> <span data-ttu-id="b8875-274">Par exemple, une carte à double largeur requiert deux emplacements.</span><span class="sxs-lookup"><span data-stu-id="b8875-274">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="b8875-275">Autre exemple : une carte peut être utilisée pour la même fonction générale que les autres cartes, mais elle nécessite un emplacement spécial (par exemple, une valeur trop longue), tandis que les autres cartes peuvent être placées dans n’importe quel emplacement disponible.</span><span class="sxs-lookup"><span data-stu-id="b8875-275">Another example is where a certain card may be used for the same general function as other cards but requires a special slot (for example, extra long), whereas the other cards can be placed in any available slot.</span></span> <span data-ttu-id="b8875-276">Si la valeur est **true**, la propriété correspondante, **RequirementsDescription**, doit spécifier la nature de l’unicité ou de l’objectif de la carte.</span><span class="sxs-lookup"><span data-stu-id="b8875-276">If set to **TRUE**, then the corresponding property, **RequirementsDescription**, should specify the nature of the uniqueness or purpose of the card.</span></span>

<span data-ttu-id="b8875-277">Cette propriété est héritée de la [**\_ carte CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-277">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-278">**État**</span><span class="sxs-lookup"><span data-stu-id="b8875-278">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-281">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b8875-281">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-282">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b8875-282">Current status of the object.</span></span> <span data-ttu-id="b8875-283">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="b8875-283">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b8875-284">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="b8875-284">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b8875-285">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="b8875-285">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b8875-286">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="b8875-286">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b8875-287">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="b8875-287">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b8875-288">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8875-289">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8875-289">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b8875-290">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="b8875-290">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b8875-291">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="b8875-291">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8875-292">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="b8875-292">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8875-293">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="b8875-293">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b8875-294">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="b8875-294">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b8875-295">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="b8875-295">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b8875-296">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="b8875-296">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b8875-297">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="b8875-297">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b8875-298">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="b8875-298">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b8875-299">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="b8875-299">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b8875-300">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="b8875-300">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b8875-301">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="b8875-301">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8875-302">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b8875-302">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-305">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b8875-305">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-306">Identificateur unique de la carte de carte du système.</span><span class="sxs-lookup"><span data-stu-id="b8875-306">Unique identifier of the baseboard of the system.</span></span>

<span data-ttu-id="b8875-307">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-307">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="b8875-308">Exemple : « carte de base »</span><span class="sxs-lookup"><span data-stu-id="b8875-308">Example: "Base Board"</span></span>

</dd> <dt>

<span data-ttu-id="b8875-309">**Version**</span><span class="sxs-lookup"><span data-stu-id="b8875-309">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b8875-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-312">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8875-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8875-313">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="b8875-313">Version of the physical element.</span></span>

<span data-ttu-id="b8875-314">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-315">**Poids**</span><span class="sxs-lookup"><span data-stu-id="b8875-315">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-316">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="b8875-316">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-318">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="b8875-318">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-319">Poids du package physique en livres.</span><span class="sxs-lookup"><span data-stu-id="b8875-319">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="b8875-320">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-320">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8875-321">**Width**</span><span class="sxs-lookup"><span data-stu-id="b8875-321">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8875-322">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="b8875-322">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8875-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b8875-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8875-324">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="b8875-324">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b8875-325">Largeur du package physique en pouces.</span><span class="sxs-lookup"><span data-stu-id="b8875-325">Width of the physical package in inches.</span></span>

<span data-ttu-id="b8875-326">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-326">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8875-327">Notes</span><span class="sxs-lookup"><span data-stu-id="b8875-327">Remarks</span></span>

<span data-ttu-id="b8875-328">La **classe \_ Baseboard Win32** est dérivée de la [**\_ carte CIM**](cim-card.md) qui dérive de [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8875-328">The **Win32\_BaseBoard** class is derived from [**CIM\_Card**](cim-card.md) which derives from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b8875-329">Exemples</span><span class="sxs-lookup"><span data-stu-id="b8875-329">Examples</span></span>

<span data-ttu-id="b8875-330">L’exemple perl [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) retourne des informations sur la carte mère de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b8875-330">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="b8875-331">L’exemple PowerShell [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) retourne des informations sur la carte mère de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b8875-331">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) PowerShell sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="b8875-332">L’exemple VBScript suivant retourne également des informations sur la carte mère de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b8875-332">The following VBScript sample also returns information about the computer baseboard.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a><span data-ttu-id="b8875-333">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8875-333">Requirements</span></span>



| <span data-ttu-id="b8875-334">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8875-334">Requirement</span></span> | <span data-ttu-id="b8875-335">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8875-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8875-336">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8875-336">Minimum supported client</span></span><br/> | <span data-ttu-id="b8875-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8875-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8875-338">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8875-338">Minimum supported server</span></span><br/> | <span data-ttu-id="b8875-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8875-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8875-340">MOF</span><span class="sxs-lookup"><span data-stu-id="b8875-340">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8875-341"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8875-341"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8875-342">DLL</span><span class="sxs-lookup"><span data-stu-id="b8875-342">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8875-343"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8875-343"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8875-344">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8875-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8875-345">**\_Carte CIM**</span><span class="sxs-lookup"><span data-stu-id="b8875-345">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dt>

[<span data-ttu-id="b8875-346">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="b8875-346">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

