---
description: La \_ classe de carte CIM représente un type de conteneur physique qui peut être branché dans une autre carte ou un autre tableau d’accueil, ou il s’agit d’une carte d’hébergement/carte mère dans un châssis.
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: Classe CIM_Card
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b10478e5d0e34020f64d8775e857d9fa6af94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516785"
---
# <a name="cim_card-class"></a><span data-ttu-id="97bea-103">\_Classe de carte CIM</span><span class="sxs-lookup"><span data-stu-id="97bea-103">CIM\_Card class</span></span>

<span data-ttu-id="97bea-104">La classe de **\_ carte CIM** représente un type de conteneur physique qui peut être branché dans une autre carte ou un autre tableau d’accueil, ou il s’agit d’une carte d’hébergement/carte mère dans un châssis.</span><span class="sxs-lookup"><span data-stu-id="97bea-104">The **CIM\_Card** class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="97bea-105">Cette classe comprend tout package capable de transporter des signaux et de fournir un point de montage pour les composants physiques, tels que les copeaux ou autres packages physiques, tels que les autres cartes.</span><span class="sxs-lookup"><span data-stu-id="97bea-105">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97bea-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="97bea-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="97bea-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="97bea-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="97bea-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="97bea-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="97bea-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="97bea-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="97bea-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97bea-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
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
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a><span data-ttu-id="97bea-111">Membres</span><span class="sxs-lookup"><span data-stu-id="97bea-111">Members</span></span>

<span data-ttu-id="97bea-112">La classe de la **\_ carte CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="97bea-112">The **CIM\_Card** class has these types of members:</span></span>

-   [<span data-ttu-id="97bea-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97bea-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="97bea-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97bea-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="97bea-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97bea-115">Methods</span></span>

<span data-ttu-id="97bea-116">La classe de **\_ carte CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="97bea-116">The **CIM\_Card** class has these methods.</span></span>



| <span data-ttu-id="97bea-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="97bea-117">Method</span></span>                                                        | <span data-ttu-id="97bea-118">Description</span><span class="sxs-lookup"><span data-stu-id="97bea-118">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97bea-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="97bea-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-card.md) | <span data-ttu-id="97bea-120">Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="97bea-120">Verifies whether the referenced physical element may be contained by or inserted into the physical package.</span></span> <span data-ttu-id="97bea-121">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="97bea-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="97bea-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="97bea-122">Properties</span></span>

<span data-ttu-id="97bea-123">La classe de la **\_ carte CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="97bea-123">The **CIM\_Card** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97bea-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="97bea-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-127">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="97bea-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-128">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="97bea-128">A short textual description of the object.</span></span>

<span data-ttu-id="97bea-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="97bea-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-133">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97bea-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-134">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="97bea-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="97bea-135">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="97bea-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="97bea-136">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-136">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-137">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="97bea-137">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-138">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="97bea-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-140">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="97bea-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-141">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="97bea-141">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="97bea-142">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-142">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-143">**Description**</span><span class="sxs-lookup"><span data-stu-id="97bea-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-146">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="97bea-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-147">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="97bea-147">A textual description of the object.</span></span>

<span data-ttu-id="97bea-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="97bea-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-150">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="97bea-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-152">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="97bea-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-153">Hauteur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="97bea-153">Height of the physical package, in inches.</span></span>

<span data-ttu-id="97bea-154">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-154">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-155">**Hébergement**</span><span class="sxs-lookup"><span data-stu-id="97bea-155">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-156">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97bea-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-158">Si la **valeur est true**, cette carte est une carte mère ou, plus génériquement, une carte de carte dans un châssis.</span><span class="sxs-lookup"><span data-stu-id="97bea-158">If **TRUE**, this card is a motherboard or, more generically, a baseboard in a chassis.</span></span>

</dd> <dt>

<span data-ttu-id="97bea-159">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="97bea-159">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-160">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97bea-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-162">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="97bea-162">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="97bea-163">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="97bea-163">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="97bea-164">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="97bea-164">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="97bea-165">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="97bea-165">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="97bea-166">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-166">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-167">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="97bea-167">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-168">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="97bea-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-170">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="97bea-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-171">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="97bea-171">Indicates when the object was installed.</span></span> <span data-ttu-id="97bea-172">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="97bea-172">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="97bea-173">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-174">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="97bea-174">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-177">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97bea-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-178">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="97bea-178">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="97bea-179">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-179">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="97bea-180">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-181">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="97bea-181">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-184">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97bea-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-185">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="97bea-185">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="97bea-186">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-186">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-187">**Nom**</span><span class="sxs-lookup"><span data-stu-id="97bea-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-190">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="97bea-190">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-191">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="97bea-191">Label by which the object is known.</span></span> <span data-ttu-id="97bea-192">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="97bea-192">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="97bea-193">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-194">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="97bea-194">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-197">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="97bea-197">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="97bea-198">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="97bea-198">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="97bea-199">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="97bea-199">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="97bea-200">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-201">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="97bea-201">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-204">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97bea-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-205">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="97bea-205">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="97bea-206">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-207">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="97bea-207">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-208">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97bea-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-210">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="97bea-210">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="97bea-211">Dans le cas contraire, elle est actuellement désactivée.</span><span class="sxs-lookup"><span data-stu-id="97bea-211">Otherwise, it is currently off.</span></span>

<span data-ttu-id="97bea-212">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-213">**Bande**</span><span class="sxs-lookup"><span data-stu-id="97bea-213">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-214">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97bea-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-216">Si la **valeur est true**, le package est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="97bea-216">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="97bea-217">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="97bea-217">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="97bea-218">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="97bea-218">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="97bea-219">Par exemple, une puce de processeur extensible est amovible.</span><span class="sxs-lookup"><span data-stu-id="97bea-219">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="97bea-220">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-220">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-221">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="97bea-221">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-222">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97bea-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-224">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="97bea-224">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="97bea-225">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="97bea-225">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="97bea-226">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="97bea-226">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="97bea-227">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="97bea-227">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="97bea-228">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-228">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-229">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="97bea-229">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-232">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ carte CIM**.**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="97bea-232">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-233">Chaîne de forme libre qui décrit la façon dont la carte est physiquement unique à partir d’autres cartes.</span><span class="sxs-lookup"><span data-stu-id="97bea-233">Free-form string that describes the ways in which the card is physically unique from other cards.</span></span> <span data-ttu-id="97bea-234">Cette propriété n’a de sens que lorsque la propriété booléenne correspondante, **SpecialRequirements**, a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="97bea-234">This property only has meaning when the corresponding Boolean property, **SpecialRequirements**, is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="97bea-235">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="97bea-235">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-236">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97bea-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-238">Si la **valeur est true**, pour fonctionner correctement, au moins une carte fille ou auxiliaire est requise.</span><span class="sxs-lookup"><span data-stu-id="97bea-238">If **TRUE**, to function properly, at least one daughterboard or auxiliary card is required.</span></span>

</dd> <dt>

<span data-ttu-id="97bea-239">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="97bea-239">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-242">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97bea-242">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-243">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="97bea-243">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="97bea-244">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-244">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-245">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="97bea-245">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-248">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97bea-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-249">Numéro d’unité de conservation pour cet élément physique.</span><span class="sxs-lookup"><span data-stu-id="97bea-249">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="97bea-250">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-250">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-251">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="97bea-251">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="97bea-254">Chaîne de forme libre qui décrit le positionnement de l’emplacement, l’utilisation typique, les restrictions, les espaces d’emplacement individuels ou d’autres informations pertinentes pour les emplacements sur une carte.</span><span class="sxs-lookup"><span data-stu-id="97bea-254">Free-form string that describes the slot positioning, typical usage, restrictions, individual slot spacings, or other pertinent information for the slots on a card.</span></span>

</dd> <dt>

<span data-ttu-id="97bea-255">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="97bea-255">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-256">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="97bea-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-258">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ carte CIM**.**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="97bea-258">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-259">Si la **valeur est true**, la carte est physiquement unique des autres cartes du même type et, par conséquent, nécessite un emplacement spécial.</span><span class="sxs-lookup"><span data-stu-id="97bea-259">If **TRUE**, the card is physically unique from other cards of the same type and, therefore, requires a special slot.</span></span> <span data-ttu-id="97bea-260">Par exemple, une carte à double largeur requiert deux emplacements.</span><span class="sxs-lookup"><span data-stu-id="97bea-260">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="97bea-261">Un autre exemple est lorsqu’une carte peut être utilisée pour la même fonction générale que les autres cartes, mais elle nécessite un emplacement spécial (très long, par exemple); en revanche, d’autres cartes peuvent être placées dans n’importe quel emplacement disponible.</span><span class="sxs-lookup"><span data-stu-id="97bea-261">Another example is when a certain card can be used for the same general function as other cards, but requires a special slot (extra long, for example); whereas, other cards can be placed in any available slot.</span></span> <span data-ttu-id="97bea-262">Si la **valeur est true**, la propriété **RequirementsDescription** correspondante doit spécifier la nature de l’unicité ou de l’objectif de la carte.</span><span class="sxs-lookup"><span data-stu-id="97bea-262">If **TRUE**, the corresponding **RequirementsDescription** property should specify the nature of the uniqueness or purpose of the card.</span></span>

</dd> <dt>

<span data-ttu-id="97bea-263">**État**</span><span class="sxs-lookup"><span data-stu-id="97bea-263">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-266">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="97bea-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-267">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="97bea-267">String that indicates the current status of the object.</span></span> <span data-ttu-id="97bea-268">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="97bea-268">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="97bea-269">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="97bea-269">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="97bea-270">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="97bea-270">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="97bea-271">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="97bea-271">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="97bea-272">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="97bea-272">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="97bea-273">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="97bea-273">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="97bea-274">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-274">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="97bea-275">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="97bea-275">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="97bea-276">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="97bea-276">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="97bea-277">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="97bea-277">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="97bea-278">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="97bea-278">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="97bea-279">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="97bea-279">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="97bea-280">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="97bea-280">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="97bea-281">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="97bea-281">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="97bea-282">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="97bea-282">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="97bea-283">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="97bea-283">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="97bea-284">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="97bea-284">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="97bea-285">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="97bea-285">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="97bea-286">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="97bea-286">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="97bea-287">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="97bea-287">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="97bea-288">**Tag**</span><span class="sxs-lookup"><span data-stu-id="97bea-288">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-291">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="97bea-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-292">Identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="97bea-292">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="97bea-293">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="97bea-293">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="97bea-294">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="97bea-294">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="97bea-295">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="97bea-295">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="97bea-296">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="97bea-296">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="97bea-297">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="97bea-297">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="97bea-298">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-299">**Version**</span><span class="sxs-lookup"><span data-stu-id="97bea-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="97bea-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-302">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="97bea-302">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="97bea-303">Indique la version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="97bea-303">Indicates the version of the physical element.</span></span>

<span data-ttu-id="97bea-304">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-304">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-305">**Poids**</span><span class="sxs-lookup"><span data-stu-id="97bea-305">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-306">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="97bea-306">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-308">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="97bea-308">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-309">Poids du package physique, en livres.</span><span class="sxs-lookup"><span data-stu-id="97bea-309">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="97bea-310">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-310">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="97bea-311">**Width**</span><span class="sxs-lookup"><span data-stu-id="97bea-311">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97bea-312">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="97bea-312">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="97bea-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="97bea-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97bea-314">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="97bea-314">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="97bea-315">Largeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="97bea-315">Width of the physical package, in inches.</span></span>

<span data-ttu-id="97bea-316">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-316">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97bea-317">Notes</span><span class="sxs-lookup"><span data-stu-id="97bea-317">Remarks</span></span>

<span data-ttu-id="97bea-318">La classe de la **\_ carte CIM** est dérivée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-318">The **CIM\_Card** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="97bea-319">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="97bea-319">WMI does not implement this class.</span></span> <span data-ttu-id="97bea-320">Pour plus d’informations sur les classes dérivées de la **\_ carte CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="97bea-320">For more information about classes derived from **CIM\_Card**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="97bea-321">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="97bea-321">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="97bea-322">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="97bea-322">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="97bea-323">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97bea-323">Requirements</span></span>



| <span data-ttu-id="97bea-324">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97bea-324">Requirement</span></span> | <span data-ttu-id="97bea-325">Valeur</span><span class="sxs-lookup"><span data-stu-id="97bea-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97bea-326">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97bea-326">Minimum supported client</span></span><br/> | <span data-ttu-id="97bea-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97bea-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97bea-328">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97bea-328">Minimum supported server</span></span><br/> | <span data-ttu-id="97bea-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97bea-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97bea-330">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97bea-330">Namespace</span></span><br/>                | <span data-ttu-id="97bea-331">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="97bea-331">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97bea-332">MOF</span><span class="sxs-lookup"><span data-stu-id="97bea-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97bea-333"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97bea-333"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97bea-334">DLL</span><span class="sxs-lookup"><span data-stu-id="97bea-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97bea-335"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97bea-335"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97bea-336">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97bea-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bea-337">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="97bea-337">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

