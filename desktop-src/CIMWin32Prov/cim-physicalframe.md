---
description: La \_ classe PHYSICALFRAME CIM est une classe parente de racks, de châssis et d’autres boîtiers de frames tels qu’ils sont définis dans les classes d’extension.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: Classe CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111266"
---
# <a name="cim_physicalframe-class"></a><span data-ttu-id="d471d-103">\_Classe CIM PhysicalFrame</span><span class="sxs-lookup"><span data-stu-id="d471d-103">CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="d471d-104">La **classe \_ PhysicalFrame CIM** est une classe parente de racks, de châssis et d’autres boîtiers de frames tels qu’ils sont définis dans les classes d’extension.</span><span class="sxs-lookup"><span data-stu-id="d471d-104">The **CIM\_PhysicalFrame** class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="d471d-105">Les propriétés telles que **VisibleAlarm** et **AudibleAlarm**, ainsi que les données relatives aux violations de sécurité, sont incluses dans cette classe parente.</span><span class="sxs-lookup"><span data-stu-id="d471d-105">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d471d-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d471d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d471d-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d471d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d471d-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d471d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d471d-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d471d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d471d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d471d-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="d471d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d471d-111">Members</span></span>

<span data-ttu-id="d471d-112">La classe **CIM \_ PhysicalFrame** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d471d-112">The **CIM\_PhysicalFrame** class has these types of members:</span></span>

-   [<span data-ttu-id="d471d-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d471d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="d471d-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d471d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d471d-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d471d-115">Methods</span></span>

<span data-ttu-id="d471d-116">La classe **CIM \_ PhysicalFrame** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d471d-116">The **CIM\_PhysicalFrame** class has these methods.</span></span>



| <span data-ttu-id="d471d-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="d471d-117">Method</span></span>                                                                 | <span data-ttu-id="d471d-118">Description</span><span class="sxs-lookup"><span data-stu-id="d471d-118">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d471d-119">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="d471d-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalframe.md) | <span data-ttu-id="d471d-120">Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="d471d-120">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="d471d-121">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="d471d-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d471d-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d471d-122">Properties</span></span>

<span data-ttu-id="d471d-123">La classe **CIM \_ PhysicalFrame** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d471d-123">The **CIM\_PhysicalFrame** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d471d-124">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="d471d-124">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-125">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d471d-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-127">Si la **valeur est true**, le cadre est équipé d’une alarme sonore.</span><span class="sxs-lookup"><span data-stu-id="d471d-127">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="d471d-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="d471d-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="d471d-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-132">Chaîne de forme libre qui fournit plus d’informations si la propriété **SecurityBreach** indique qu’une violation ou un autre événement lié à la sécurité s’est produit.</span><span class="sxs-lookup"><span data-stu-id="d471d-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d471d-133">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="d471d-133">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-136">Chaîne de forme libre qui contient des informations sur la façon dont les différents câbles sont connectés et regroupés pour le cadre.</span><span class="sxs-lookup"><span data-stu-id="d471d-136">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="d471d-137">Avec de nombreuses connexions réseau, liées au stockage et aux câbles d’alimentation, la gestion des câbles peut être un défi complexe et difficile.</span><span class="sxs-lookup"><span data-stu-id="d471d-137">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="d471d-138">Cette propriété de type chaîne contient des informations pour faciliter l’assembly et le service du frame.</span><span class="sxs-lookup"><span data-stu-id="d471d-138">This string property contains information to aid in assembly and service of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="d471d-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d471d-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-142">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d471d-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-143">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d471d-143">Short textual description of the object.</span></span>

<span data-ttu-id="d471d-144">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d471d-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-148">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d471d-148">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-149">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d471d-149">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d471d-150">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="d471d-150">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d471d-151">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-151">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-152">**Profondeur**</span><span class="sxs-lookup"><span data-stu-id="d471d-152">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-153">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d471d-153">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-155">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d471d-155">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-156">Profondeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d471d-156">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="d471d-157">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-157">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-158">**Description**</span><span class="sxs-lookup"><span data-stu-id="d471d-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-161">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d471d-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-162">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d471d-162">Textual description of the object.</span></span>

<span data-ttu-id="d471d-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-164">**Height**</span><span class="sxs-lookup"><span data-stu-id="d471d-164">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-165">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d471d-165">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-167">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d471d-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-168">Hauteur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d471d-168">Height of the physical package, in inches.</span></span>

<span data-ttu-id="d471d-169">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-169">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-170">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="d471d-170">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-171">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d471d-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-173">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d471d-173">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="d471d-174">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="d471d-174">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="d471d-175">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d471d-175">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="d471d-176">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="d471d-176">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="d471d-177">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-177">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-178">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d471d-178">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-179">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d471d-179">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-181">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d471d-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-182">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d471d-182">Date and time the object was installed.</span></span> <span data-ttu-id="d471d-183">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="d471d-183">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d471d-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-185">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="d471d-185">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-186">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d471d-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-188">Si la **valeur est true**, le frame est protégé par un verrou.</span><span class="sxs-lookup"><span data-stu-id="d471d-188">If **TRUE**, the frame is protected with a lock.</span></span>

</dd> <dt>

<span data-ttu-id="d471d-189">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="d471d-189">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-192">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d471d-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-193">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d471d-193">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="d471d-194">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-194">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="d471d-195">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-195">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-196">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="d471d-196">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-199">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d471d-199">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-200">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="d471d-200">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="d471d-201">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-202">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d471d-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-205">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d471d-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-206">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d471d-206">Label by which the object is known.</span></span> <span data-ttu-id="d471d-207">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d471d-207">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d471d-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-209">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d471d-209">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-212">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="d471d-212">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="d471d-213">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="d471d-213">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="d471d-214">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="d471d-214">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="d471d-215">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-216">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="d471d-216">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-219">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d471d-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-220">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d471d-220">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="d471d-221">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-222">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="d471d-222">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-223">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d471d-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-225">Si la **valeur est true**, l’élément physique est sous tension ; dans le cas contraire, elle est actuellement désactivée.</span><span class="sxs-lookup"><span data-stu-id="d471d-225">If **TRUE**, the physical element is powered on; otherwise, it is currently off.</span></span>

<span data-ttu-id="d471d-226">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-226">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-227">**Bande**</span><span class="sxs-lookup"><span data-stu-id="d471d-227">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-228">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d471d-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-230">Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="d471d-230">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="d471d-231">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="d471d-231">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="d471d-232">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="d471d-232">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="d471d-233">Par exemple, une puce de processeur extensible est amovible.</span><span class="sxs-lookup"><span data-stu-id="d471d-233">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="d471d-234">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-234">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-235">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="d471d-235">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-236">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d471d-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-238">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="d471d-238">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="d471d-239">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="d471d-239">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="d471d-240">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="d471d-240">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="d471d-241">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="d471d-241">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="d471d-242">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-242">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-243">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="d471d-243">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-244">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d471d-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-246">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Table globale du conteneur physique DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="d471d-246">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-247">Indique si une violation physique du frame a été tentée, mais a échoué ou a été tentée et réussie.</span><span class="sxs-lookup"><span data-stu-id="d471d-247">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d471d-248">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d471d-248">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d471d-249">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d471d-249">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="d471d-250">**Aucune violation** (3)</span><span class="sxs-lookup"><span data-stu-id="d471d-250">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="d471d-251">**Tentative de violation** (4)</span><span class="sxs-lookup"><span data-stu-id="d471d-251">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="d471d-252">**Violation réussie** (5)</span><span class="sxs-lookup"><span data-stu-id="d471d-252">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d471d-253">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d471d-253">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-254">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-256">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d471d-256">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-257">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d471d-257">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="d471d-258">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-258">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-259">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d471d-259">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-260">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d471d-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d471d-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-262">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="d471d-262">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-263">Chaînes de forme libre qui fournissent des explications détaillées sur les entrées dans le tableau **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="d471d-263">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="d471d-264">Chaque entrée de ce tableau est liée à l’entrée dans le tableau **ServicePhilosophy** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="d471d-264">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="d471d-265">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="d471d-265">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-266">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d471d-266">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d471d-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-268">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="d471d-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-269">Indique si le frame est pris en service à partir du haut, de l’avant, de l’arrière ou du côté ; et s’il a des bacs coulissants ou des côtés amovibles, et si le cadre est mobile (par exemple, des rouleaux).</span><span class="sxs-lookup"><span data-stu-id="d471d-269">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d471d-270">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d471d-270">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d471d-271">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d471d-271">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="d471d-272">**Service à partir du haut** (2)</span><span class="sxs-lookup"><span data-stu-id="d471d-272">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="d471d-273">**Service à l’avant** (3)</span><span class="sxs-lookup"><span data-stu-id="d471d-273">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="d471d-274">**Service à partir de l’arrière** (4)</span><span class="sxs-lookup"><span data-stu-id="d471d-274">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="d471d-275">**Service de la côte** (5)</span><span class="sxs-lookup"><span data-stu-id="d471d-275">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="d471d-276">**Plateaux coulissants** (6)</span><span class="sxs-lookup"><span data-stu-id="d471d-276">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="d471d-277">**Côtés amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="d471d-277">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="d471d-278">**Mobile** (8)</span><span class="sxs-lookup"><span data-stu-id="d471d-278">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d471d-279">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="d471d-279">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-282">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d471d-282">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-283">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d471d-283">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="d471d-284">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-284">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-285">**État**</span><span class="sxs-lookup"><span data-stu-id="d471d-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-288">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d471d-288">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-289">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d471d-289">Current status of the object.</span></span>

<span data-ttu-id="d471d-290">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d471d-291">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d471d-291">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d471d-292">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d471d-292">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d471d-293">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d471d-293">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d471d-294">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d471d-294">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d471d-295">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d471d-295">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d471d-296">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d471d-296">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d471d-297">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d471d-297">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d471d-298">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d471d-298">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d471d-299">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d471d-299">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d471d-300">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d471d-300">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d471d-301">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d471d-301">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d471d-302">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d471d-302">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d471d-303">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d471d-303">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d471d-304">**Tag**</span><span class="sxs-lookup"><span data-stu-id="d471d-304">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-307">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d471d-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-308">Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d471d-308">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="d471d-309">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="d471d-309">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="d471d-310">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel/l’entité, indépendamment de l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="d471d-310">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="d471d-311">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="d471d-311">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="d471d-312">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d471d-312">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="d471d-313">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="d471d-313">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="d471d-314">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-315">**Version**</span><span class="sxs-lookup"><span data-stu-id="d471d-315">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d471d-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-318">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d471d-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d471d-319">Chaîne qui indique la version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="d471d-319">String that indicates the version of the physical element.</span></span>

<span data-ttu-id="d471d-320">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-321">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="d471d-321">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-322">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d471d-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d471d-324">Si la **valeur est true**, l’équipement comprend une alarme visible.</span><span class="sxs-lookup"><span data-stu-id="d471d-324">If **TRUE**, the equipment includes a visible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="d471d-325">**Poids**</span><span class="sxs-lookup"><span data-stu-id="d471d-325">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-326">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d471d-326">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-328">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« livres »)</span><span class="sxs-lookup"><span data-stu-id="d471d-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-329">Poids du package physique, en livres.</span><span class="sxs-lookup"><span data-stu-id="d471d-329">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="d471d-330">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-330">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d471d-331">**Width**</span><span class="sxs-lookup"><span data-stu-id="d471d-331">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d471d-332">Type de données : **real32**</span><span class="sxs-lookup"><span data-stu-id="d471d-332">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d471d-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d471d-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d471d-334">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pouces »)</span><span class="sxs-lookup"><span data-stu-id="d471d-334">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d471d-335">Largeur du package physique, en pouces.</span><span class="sxs-lookup"><span data-stu-id="d471d-335">Width of the physical package, in inches.</span></span>

<span data-ttu-id="d471d-336">Cette propriété est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-336">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d471d-337">Notes</span><span class="sxs-lookup"><span data-stu-id="d471d-337">Remarks</span></span>

<span data-ttu-id="d471d-338">La classe **CIM \_ PhysicalFrame** est dérivée de [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-338">The **CIM\_PhysicalFrame** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="d471d-339">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d471d-339">WMI does not implement this class.</span></span> <span data-ttu-id="d471d-340">Pour les classes WMI dérivées de **CIM \_ PhysicalFrame**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d471d-340">For WMI classes derived from **CIM\_PhysicalFrame**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d471d-341">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d471d-341">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d471d-342">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d471d-342">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d471d-343">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d471d-343">Requirements</span></span>



| <span data-ttu-id="d471d-344">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d471d-344">Requirement</span></span> | <span data-ttu-id="d471d-345">Valeur</span><span class="sxs-lookup"><span data-stu-id="d471d-345">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d471d-346">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d471d-346">Minimum supported client</span></span><br/> | <span data-ttu-id="d471d-347">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d471d-347">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d471d-348">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d471d-348">Minimum supported server</span></span><br/> | <span data-ttu-id="d471d-349">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d471d-349">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d471d-350">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d471d-350">Namespace</span></span><br/>                | <span data-ttu-id="d471d-351">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d471d-351">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d471d-352">MOF</span><span class="sxs-lookup"><span data-stu-id="d471d-352">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d471d-353"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d471d-353"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d471d-354">DLL</span><span class="sxs-lookup"><span data-stu-id="d471d-354">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d471d-355"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d471d-355"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d471d-356">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d471d-356">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d471d-357">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="d471d-357">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

