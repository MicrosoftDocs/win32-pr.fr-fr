---
description: La \_ classe CIM PhysicalPackage représente des éléments physiques qui contiennent ou hébergent d’autres composants. Il s’agit par exemple d’un boîtier en rack ou d’une carte adaptateur.
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: Classe CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1905467fd949e2c18d8be9e7a7bfff39ad8d1477
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514541"
---
# <a name="cim_physicalpackage-class"></a><span data-ttu-id="d0eda-104">\_Classe CIM PhysicalPackage</span><span class="sxs-lookup"><span data-stu-id="d0eda-104">CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="d0eda-105">La classe **CIM \_ PhysicalPackage** représente des éléments physiques qui contiennent ou hébergent d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="d0eda-105">The **CIM\_PhysicalPackage** class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="d0eda-106">Il s’agit par exemple d’un boîtier en rack ou d’une carte adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d0eda-106">Examples are a rack enclosure or an adapter card.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0eda-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d0eda-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d0eda-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d0eda-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d0eda-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d0eda-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d0eda-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d0eda-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0eda-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0eda-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
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
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="d0eda-112">Membres</span><span class="sxs-lookup"><span data-stu-id="d0eda-112">Members</span></span>

<span data-ttu-id="d0eda-113">La classe **CIM \_ PhysicalPackage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d0eda-113">The **CIM\_PhysicalPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="d0eda-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d0eda-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d0eda-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d0eda-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d0eda-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d0eda-116">Methods</span></span>

<span data-ttu-id="d0eda-117">La classe **CIM \_ PhysicalPackage** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d0eda-117">The **CIM\_PhysicalPackage** class has these methods.</span></span>



| <span data-ttu-id="d0eda-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="d0eda-118">Method</span></span>                                                                   | <span data-ttu-id="d0eda-119">Description</span><span class="sxs-lookup"><span data-stu-id="d0eda-119">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0eda-120">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="d0eda-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md) | <span data-ttu-id="d0eda-121">Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="d0eda-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="d0eda-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="d0eda-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d0eda-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d0eda-123">Properties</span></span>

<span data-ttu-id="d0eda-124">La classe **CIM \_ PhysicalPackage** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0eda-124">The **CIM\_PhysicalPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0eda-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d0eda-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-128">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-129">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d0eda-129">Short textual description of the object.</span></span>

<span data-ttu-id="d0eda-130">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d0eda-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-134">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d0eda-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-135">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d0eda-135">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d0eda-136">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="d0eda-136">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d0eda-137">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-138">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="d0eda-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-139">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d0eda-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-141">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-142">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d0eda-142">Depth of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-143">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0eda-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-146">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d0eda-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-147">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d0eda-147">Textual description of the object.</span></span>

<span data-ttu-id="d0eda-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-149">**Height**</span><span class="sxs-lookup"><span data-stu-id="d0eda-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-150">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d0eda-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-152">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-153">Hauteur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d0eda-153">Height of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-154">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="d0eda-154">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-155">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d0eda-155">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-157">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d0eda-157">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="d0eda-158">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="d0eda-158">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="d0eda-159">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d0eda-159">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="d0eda-160">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="d0eda-160">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d0eda-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-162">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d0eda-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-164">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d0eda-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-165">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d0eda-165">Date and time the object was installed.</span></span> <span data-ttu-id="d0eda-166">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="d0eda-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d0eda-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-168">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="d0eda-168">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-171">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d0eda-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-172">Nom de l’organisation qui a produit l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d0eda-172">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="d0eda-173">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-173">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="d0eda-174">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-175">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="d0eda-175">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-178">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d0eda-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-179">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="d0eda-179">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="d0eda-180">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-181">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d0eda-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-184">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d0eda-184">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-185">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d0eda-185">Label by which the object is known.</span></span> <span data-ttu-id="d0eda-186">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d0eda-186">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d0eda-187">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-188">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d0eda-188">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-191">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="d0eda-191">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="d0eda-192">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="d0eda-192">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="d0eda-193">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="d0eda-193">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="d0eda-194">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-195">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="d0eda-195">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-198">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d0eda-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-199">Numéro de référence attribué par l’organisation qui a produit ou fabriqué l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d0eda-199">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="d0eda-200">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-201">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="d0eda-201">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-202">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d0eda-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-204">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="d0eda-204">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="d0eda-205">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-206">**Bande**</span><span class="sxs-lookup"><span data-stu-id="d0eda-206">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-207">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d0eda-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-209">Si la **valeur est true**, le package est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="d0eda-209">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="d0eda-210">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="d0eda-210">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="d0eda-211">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d0eda-211">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="d0eda-212">Par exemple, une puce de processeur extensible est amovible.</span><span class="sxs-lookup"><span data-stu-id="d0eda-212">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-213">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="d0eda-213">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-214">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d0eda-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-216">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="d0eda-216">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="d0eda-217">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="d0eda-217">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="d0eda-218">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="d0eda-218">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="d0eda-219">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="d0eda-219">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d0eda-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-223">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d0eda-223">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-224">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d0eda-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="d0eda-225">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-226">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="d0eda-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-229">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d0eda-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-230">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d0eda-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="d0eda-231">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-232">**État**</span><span class="sxs-lookup"><span data-stu-id="d0eda-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-235">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d0eda-235">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-236">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d0eda-236">Current status of the object.</span></span>

<span data-ttu-id="d0eda-237">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d0eda-238">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0eda-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d0eda-239">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d0eda-240">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0eda-241">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0eda-242">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d0eda-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d0eda-243">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d0eda-244">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d0eda-245">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d0eda-246">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d0eda-247">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d0eda-248">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d0eda-249">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d0eda-250">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0eda-251">**Tag**</span><span class="sxs-lookup"><span data-stu-id="d0eda-251">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-254">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d0eda-254">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-255">Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d0eda-255">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="d0eda-256">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="d0eda-256">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="d0eda-257">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="d0eda-257">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="d0eda-258">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d0eda-258">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="d0eda-259">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d0eda-259">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="d0eda-260">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="d0eda-260">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="d0eda-261">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-262">**Version**</span><span class="sxs-lookup"><span data-stu-id="d0eda-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0eda-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-265">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d0eda-265">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-266">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d0eda-266">Version of the physical element.</span></span>

<span data-ttu-id="d0eda-267">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-267">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-268">**Poids**</span><span class="sxs-lookup"><span data-stu-id="d0eda-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-269">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d0eda-269">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-271">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-271">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-272">Poids du package physique, en livres.</span><span class="sxs-lookup"><span data-stu-id="d0eda-272">Weight of the physical package, in pounds.</span></span>

</dd> <dt>

<span data-ttu-id="d0eda-273">**Width**</span><span class="sxs-lookup"><span data-stu-id="d0eda-273">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eda-274">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d0eda-274">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0eda-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eda-276">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d0eda-276">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d0eda-277">Largeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d0eda-277">Width of the physical package, in inches.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0eda-278">Notes</span><span class="sxs-lookup"><span data-stu-id="d0eda-278">Remarks</span></span>

<span data-ttu-id="d0eda-279">La classe **CIM \_ PhysicalPackage** est dérivée de [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-279">The **CIM\_PhysicalPackage** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="d0eda-280">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d0eda-280">WMI does not implement this class.</span></span> <span data-ttu-id="d0eda-281">Pour les classes WMI dérivées de **CIM \_ PhysicalPackage**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d0eda-281">For WMI classes that are derived from **CIM\_PhysicalPackage**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d0eda-282">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d0eda-282">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d0eda-283">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d0eda-283">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0eda-284">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0eda-284">Requirements</span></span>



| <span data-ttu-id="d0eda-285">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0eda-285">Requirement</span></span> | <span data-ttu-id="d0eda-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0eda-286">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0eda-287">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0eda-287">Minimum supported client</span></span><br/> | <span data-ttu-id="d0eda-288">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0eda-288">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0eda-289">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0eda-289">Minimum supported server</span></span><br/> | <span data-ttu-id="d0eda-290">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0eda-290">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0eda-291">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d0eda-291">Namespace</span></span><br/>                | <span data-ttu-id="d0eda-292">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d0eda-292">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0eda-293">MOF</span><span class="sxs-lookup"><span data-stu-id="d0eda-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0eda-294"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0eda-294"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0eda-295">DLL</span><span class="sxs-lookup"><span data-stu-id="d0eda-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0eda-296"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0eda-296"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0eda-297">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0eda-297">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0eda-298">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d0eda-298">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

