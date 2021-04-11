---
description: La \_ classe CIM PhysicalMedia représente les types de documentation et les supports de stockage, tels que les bandes, les CD-ROM, etc.
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: Classe CIM_PhysicalMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211268"
---
# <a name="cim_physicalmedia-class"></a><span data-ttu-id="09980-103">\_Classe CIM PhysicalMedia</span><span class="sxs-lookup"><span data-stu-id="09980-103">CIM\_PhysicalMedia class</span></span>

<span data-ttu-id="09980-104">La classe **CIM \_ PhysicalMedia** représente les types de documentation et les supports de stockage, tels que les bandes, les CD-ROM, etc.</span><span class="sxs-lookup"><span data-stu-id="09980-104">The **CIM\_PhysicalMedia** class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span> <span data-ttu-id="09980-105">Cette classe est généralement utilisée pour rechercher et gérer des médias amovibles (par opposition aux médias scellés avec l’appareil d’accès aux médias en tant que package unique, tels que les disques durs).</span><span class="sxs-lookup"><span data-stu-id="09980-105">This class is typically used to locate and manage removable media (versus media sealed with the media access device as a single package, such as hard disks).</span></span> <span data-ttu-id="09980-106">Toutefois, le support scellé peut également être modélisé à l’aide de cette classe lorsque le média est associé au package physique à l’aide de la relation [**\_ PackagedComponent CIM**](cim-packagedcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="09980-106">Sealed media, however, can also be modeled using this class when the media is associated with the physical package using the [**CIM\_PackagedComponent**](cim-packagedcomponent.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09980-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="09980-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="09980-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="09980-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="09980-109">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="09980-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="09980-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="09980-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="09980-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09980-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
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
  boolean  WriteProtectOn;
};
```

## <a name="members"></a><span data-ttu-id="09980-112">Membres</span><span class="sxs-lookup"><span data-stu-id="09980-112">Members</span></span>

<span data-ttu-id="09980-113">La classe **CIM \_ PhysicalMedia** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="09980-113">The **CIM\_PhysicalMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="09980-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="09980-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09980-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="09980-115">Properties</span></span>

<span data-ttu-id="09980-116">La classe **CIM \_ PhysicalMedia** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="09980-116">The **CIM\_PhysicalMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09980-117">**Capacité**</span><span class="sxs-lookup"><span data-stu-id="09980-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-118">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09980-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09980-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-120">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="09980-120">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="09980-121">Nombre d’octets pouvant être lus ou écrits dans un média.</span><span class="sxs-lookup"><span data-stu-id="09980-121">Number of bytes that can be read from, or written to, a media.</span></span> <span data-ttu-id="09980-122">Cette propriété ne s’applique pas à la copie matérielle (documentation) ou au support de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="09980-122">This property is not applicable to hard copy (documentation) or cleaner media.</span></span> <span data-ttu-id="09980-123">La compression des données ne doit pas être prise en supposer, car elle augmente la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="09980-123">Data compression should not be assumed, as it would increase the value in this property.</span></span> <span data-ttu-id="09980-124">Pour les bandes, il est supposé qu’aucune marque de fichier ou zone d’espace vide n’est enregistrée sur le support.</span><span class="sxs-lookup"><span data-stu-id="09980-124">For tapes, it should be assumed that no file marks or blank space areas are recorded on the media.</span></span>

<span data-ttu-id="09980-125">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="09980-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="09980-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="09980-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="09980-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="09980-130">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="09980-130">Short textual description of the object.</span></span>

<span data-ttu-id="09980-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-132">**CleanerMedia**</span><span class="sxs-lookup"><span data-stu-id="09980-132">**CleanerMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="09980-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09980-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09980-135">Si la **valeur est true**, le support physique est utilisé à des fins de nettoyage, et non un stockage de données.</span><span class="sxs-lookup"><span data-stu-id="09980-135">If **TRUE**, the physical media is used for cleaning purposes, not data storage.</span></span>

</dd> <dt>

<span data-ttu-id="09980-136">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09980-136">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-139">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="09980-139">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="09980-140">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="09980-140">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="09980-141">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="09980-141">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="09980-142">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-142">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-143">**Description**</span><span class="sxs-lookup"><span data-stu-id="09980-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-146">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="09980-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="09980-147">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="09980-147">Textual description of the object.</span></span>

<span data-ttu-id="09980-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="09980-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-150">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="09980-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09980-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09980-152">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="09980-152">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="09980-153">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="09980-153">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="09980-154">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="09980-154">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="09980-155">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="09980-155">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="09980-156">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="09980-156">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="09980-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-158">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09980-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09980-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-160">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="09980-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="09980-161">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="09980-161">Date and time the object was installed.</span></span> <span data-ttu-id="09980-162">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="09980-162">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="09980-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-164">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="09980-164">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-167">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="09980-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="09980-168">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="09980-168">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="09980-169">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="09980-169">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="09980-170">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-170">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-171">**MediaDescription**</span><span class="sxs-lookup"><span data-stu-id="09980-171">**MediaDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-174">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaType**»)</span><span class="sxs-lookup"><span data-stu-id="09980-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="09980-175">Détails supplémentaires relatifs à l’énumération **MediaType** .</span><span class="sxs-lookup"><span data-stu-id="09980-175">Additional detail related to the **MediaType** enumeration.</span></span> <span data-ttu-id="09980-176">Par exemple, si la valeur 3 (« cartouche QIC ») est spécifiée, cette propriété indique si la bande est d’une largeur de 1/4 pouces, d’une version préformatée, d’une compatibilité Travan, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="09980-176">For example, if value 3 ("QIC Cartridge") is specified, this property would indicate whether the tape is wide or 1/4 inch, pre-formatted, Travan compatible, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="09980-177">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="09980-177">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-178">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09980-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09980-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-180">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaDescription**»)</span><span class="sxs-lookup"><span data-stu-id="09980-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="09980-181">Type de support physique.</span><span class="sxs-lookup"><span data-stu-id="09980-181">Type of physical media.</span></span> <span data-ttu-id="09980-182">La propriété **MediaDescription** fournit une définition plus explicite du type de média.</span><span class="sxs-lookup"><span data-stu-id="09980-182">The **MediaDescription** property provides more explicit definition of the media type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="09980-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="09980-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="09980-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="09980-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span data-ttu-id="09980-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Cartouche de bande** (2)</span><span class="sxs-lookup"><span data-stu-id="09980-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Tape Cartridge** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span data-ttu-id="09980-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**Cartouche QIC** (3)</span><span class="sxs-lookup"><span data-stu-id="09980-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC Cartridge** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span data-ttu-id="09980-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**Cartouche ait** (4)</span><span class="sxs-lookup"><span data-stu-id="09980-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT Cartridge** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span data-ttu-id="09980-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**Cartouche DTF** (5)</span><span class="sxs-lookup"><span data-stu-id="09980-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF Cartridge** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span data-ttu-id="09980-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**Cartouche dat** (6)</span><span class="sxs-lookup"><span data-stu-id="09980-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT Cartridge** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="09980-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**cartouche de bande 8mm** (7)</span><span class="sxs-lookup"><span data-stu-id="09980-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8mm Tape Cartridge** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="09980-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**cartouche de bande 19MM** (8)</span><span class="sxs-lookup"><span data-stu-id="09980-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19mm Tape Cartridge** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span data-ttu-id="09980-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**Cartouche DLT** (9)</span><span class="sxs-lookup"><span data-stu-id="09980-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT Cartridge** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span data-ttu-id="09980-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Cartouche de bande magnétique demi-pouces** (10)</span><span class="sxs-lookup"><span data-stu-id="09980-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Half-Inch Magnetic Tape Cartridge** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span data-ttu-id="09980-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Disque de cartouche** (11)</span><span class="sxs-lookup"><span data-stu-id="09980-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Cartridge Disk** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span data-ttu-id="09980-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**Disque Jaz** (12)</span><span class="sxs-lookup"><span data-stu-id="09980-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span data-ttu-id="09980-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**Disque zip** (13)</span><span class="sxs-lookup"><span data-stu-id="09980-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP Disk** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span data-ttu-id="09980-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**Disque Syquest** (14)</span><span class="sxs-lookup"><span data-stu-id="09980-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span data-ttu-id="09980-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Disque amovible Winchester** (15)</span><span class="sxs-lookup"><span data-stu-id="09980-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester Removable Disk** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="09980-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="09980-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="09980-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="09980-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="09980-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="09980-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="09980-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD inscriptible** (19)</span><span class="sxs-lookup"><span data-stu-id="09980-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span data-ttu-id="09980-203"><span id="WORM"></span><span id="worm"></span>**Ver** (20)</span><span class="sxs-lookup"><span data-stu-id="09980-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span data-ttu-id="09980-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magnéto-optique** (21)</span><span class="sxs-lookup"><span data-stu-id="09980-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="09980-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="09980-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span data-ttu-id="09980-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23)</span><span class="sxs-lookup"><span data-stu-id="09980-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD+RW** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="09980-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="09980-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="09980-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="09980-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="09980-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-vidéo** (26)</span><span class="sxs-lookup"><span data-stu-id="09980-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="09980-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="09980-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span data-ttu-id="09980-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Disquette/disquette** (28)</span><span class="sxs-lookup"><span data-stu-id="09980-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/Diskette** (28)</span></span>


</dt> <dd>

<span data-ttu-id="09980-212">Disquette</span><span class="sxs-lookup"><span data-stu-id="09980-212">Floppy disk</span></span>

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span data-ttu-id="09980-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Disque dur** (29)</span><span class="sxs-lookup"><span data-stu-id="09980-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Hard Disk** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span data-ttu-id="09980-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Carte mémoire** (30)</span><span class="sxs-lookup"><span data-stu-id="09980-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Memory Card** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span data-ttu-id="09980-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Copie matérielle** (31)</span><span class="sxs-lookup"><span data-stu-id="09980-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Hard Copy** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span data-ttu-id="09980-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Disque Clik** (32)</span><span class="sxs-lookup"><span data-stu-id="09980-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik Disk** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="09980-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="09980-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="09980-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span><span class="sxs-lookup"><span data-stu-id="09980-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="09980-219"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="09980-219"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="09980-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD enregistrable** (36)</span><span class="sxs-lookup"><span data-stu-id="09980-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="09980-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="09980-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="09980-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)</span><span class="sxs-lookup"><span data-stu-id="09980-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="09980-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="09980-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="09980-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="09980-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="09980-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="09980-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="09980-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="09980-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span data-ttu-id="09980-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magnéto-optique réinscriptible** (43)</span><span class="sxs-lookup"><span data-stu-id="09980-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-Optical Rewriteable** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span data-ttu-id="09980-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Écriture unique magnéto-optique** (44)</span><span class="sxs-lookup"><span data-stu-id="09980-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-Optical Write Once** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span data-ttu-id="09980-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magnéto-optique réinscriptible (LIMDOW)** (45)</span><span class="sxs-lookup"><span data-stu-id="09980-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical Rewriteable (LIMDOW)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span data-ttu-id="09980-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Modification de la phase écriture une seule fois** (46)</span><span class="sxs-lookup"><span data-stu-id="09980-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Change Write Once** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span data-ttu-id="09980-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Modification de la phase réinscriptible** (47)</span><span class="sxs-lookup"><span data-stu-id="09980-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Phase Change Rewriteable** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span data-ttu-id="09980-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Changement de phase double réécriture** (48)</span><span class="sxs-lookup"><span data-stu-id="09980-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phase Change Dual Rewriteable** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span data-ttu-id="09980-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Écriture unique ablation** (49)</span><span class="sxs-lookup"><span data-stu-id="09980-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write Once** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span data-ttu-id="09980-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Enregistrement de champ proche** (50)</span><span class="sxs-lookup"><span data-stu-id="09980-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near Field Recording** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span data-ttu-id="09980-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQIC** (51)</span><span class="sxs-lookup"><span data-stu-id="09980-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span data-ttu-id="09980-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span><span class="sxs-lookup"><span data-stu-id="09980-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span data-ttu-id="09980-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**particule métal 8mm** (53)</span><span class="sxs-lookup"><span data-stu-id="09980-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm Metal Particle** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span data-ttu-id="09980-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**évaporation Metal avancé 8mm** (54)</span><span class="sxs-lookup"><span data-stu-id="09980-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal Evaporate** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span data-ttu-id="09980-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span><span class="sxs-lookup"><span data-stu-id="09980-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span data-ttu-id="09980-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span><span class="sxs-lookup"><span data-stu-id="09980-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span data-ttu-id="09980-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**Accélération LTO** (57)</span><span class="sxs-lookup"><span data-stu-id="09980-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span data-ttu-id="09980-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 piste bande** (58)</span><span class="sxs-lookup"><span data-stu-id="09980-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Track Tape** (58)</span></span>


</dt> <dd>

<span data-ttu-id="09980-243">9-bande de suivi</span><span class="sxs-lookup"><span data-stu-id="09980-243">9-track tape</span></span>

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span data-ttu-id="09980-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**bande à 18 pistes** (59)</span><span class="sxs-lookup"><span data-stu-id="09980-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Track Tape** (59)</span></span>


</dt> <dd>

<span data-ttu-id="09980-245">bande 18-Track</span><span class="sxs-lookup"><span data-stu-id="09980-245">18-track tape</span></span>

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span data-ttu-id="09980-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**bande de piste 36** (60)</span><span class="sxs-lookup"><span data-stu-id="09980-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 Track Tape** (60)</span></span>


</dt> <dd>

<span data-ttu-id="09980-247">36-bande de suivi</span><span class="sxs-lookup"><span data-stu-id="09980-247">36-track tape</span></span>

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span data-ttu-id="09980-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span><span class="sxs-lookup"><span data-stu-id="09980-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span data-ttu-id="09980-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Pack d’Magstar** (62)</span><span class="sxs-lookup"><span data-stu-id="09980-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span data-ttu-id="09980-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**Bande D2** (63)</span><span class="sxs-lookup"><span data-stu-id="09980-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 Tape** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span data-ttu-id="09980-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Bande-heure d’été petite** (64)</span><span class="sxs-lookup"><span data-stu-id="09980-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape - DST Small** (64)</span></span>


</dt> <dd>

<span data-ttu-id="09980-252">Bande DST petite</span><span class="sxs-lookup"><span data-stu-id="09980-252">Tape   DST small</span></span>

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span data-ttu-id="09980-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Bande-DST moyen** (65)</span><span class="sxs-lookup"><span data-stu-id="09980-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Tape - DST Medium** (65)</span></span>


</dt> <dd>

<span data-ttu-id="09980-254">Bande d’heure d’été moyenne</span><span class="sxs-lookup"><span data-stu-id="09980-254">Tape   DST medium</span></span>

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span data-ttu-id="09980-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Bande-DST grande** (66)</span><span class="sxs-lookup"><span data-stu-id="09980-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape - DST Large** (66)</span></span>


</dt> <dd>

<span data-ttu-id="09980-256">Bande d’heure d’été importante</span><span class="sxs-lookup"><span data-stu-id="09980-256">Tape   DST large</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="09980-257">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="09980-257">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-260">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="09980-260">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="09980-261">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="09980-261">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="09980-262">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-263">**Nom**</span><span class="sxs-lookup"><span data-stu-id="09980-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-266">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="09980-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="09980-267">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="09980-267">Label by which the object is known.</span></span> <span data-ttu-id="09980-268">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="09980-268">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="09980-269">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-269">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-270">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="09980-270">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09980-273">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="09980-273">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="09980-274">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="09980-274">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="09980-275">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="09980-275">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="09980-276">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-276">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-277">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="09980-277">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-280">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="09980-280">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="09980-281">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="09980-281">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="09980-282">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-283">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="09980-283">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-284">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="09980-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09980-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09980-286">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="09980-286">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="09980-287">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-288">**Bande**</span><span class="sxs-lookup"><span data-stu-id="09980-288">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-289">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="09980-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09980-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09980-291">Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="09980-291">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="09980-292">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="09980-292">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="09980-293">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="09980-293">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="09980-294">Par exemple, une puce de processeur pouvant être dégradée est amovible.</span><span class="sxs-lookup"><span data-stu-id="09980-294">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="09980-295">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="09980-295">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-296">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="09980-296">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-297">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="09980-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09980-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09980-299">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="09980-299">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="09980-300">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="09980-300">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="09980-301">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="09980-301">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="09980-302">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="09980-302">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="09980-303">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="09980-303">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-304">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="09980-304">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-307">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="09980-307">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="09980-308">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="09980-308">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="09980-309">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-309">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-310">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="09980-310">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-311">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-313">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="09980-313">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="09980-314">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="09980-314">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="09980-315">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-315">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-316">**État**</span><span class="sxs-lookup"><span data-stu-id="09980-316">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-319">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="09980-319">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="09980-320">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="09980-320">Current status of the object.</span></span>

<span data-ttu-id="09980-321">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="09980-322">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="09980-322">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="09980-323">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="09980-323">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="09980-324">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="09980-324">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="09980-325">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="09980-325">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="09980-326">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="09980-326">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="09980-327">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="09980-327">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="09980-328">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="09980-328">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="09980-329">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="09980-329">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="09980-330">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="09980-330">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="09980-331">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="09980-331">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="09980-332">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="09980-332">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="09980-333">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="09980-333">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="09980-334">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="09980-334">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="09980-335">**Tag**</span><span class="sxs-lookup"><span data-stu-id="09980-335">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-338">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="09980-338">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="09980-339">Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="09980-339">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="09980-340">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="09980-340">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="09980-341">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="09980-341">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="09980-342">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="09980-342">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="09980-343">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="09980-343">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="09980-344">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="09980-344">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="09980-345">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-345">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-346">**Version**</span><span class="sxs-lookup"><span data-stu-id="09980-346">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="09980-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09980-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09980-349">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="09980-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="09980-350">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="09980-350">Version of the physical element.</span></span>

<span data-ttu-id="09980-351">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="09980-351">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="09980-352">**WriteProtectOn**</span><span class="sxs-lookup"><span data-stu-id="09980-352">**WriteProtectOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09980-353">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="09980-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09980-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="09980-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09980-355">Si la **valeur est true**, le média est actuellement protégé en écriture par un mécanisme physique, tel qu’un onglet protéger sur une disquette.</span><span class="sxs-lookup"><span data-stu-id="09980-355">If **TRUE**, the media is currently write-protected by a physical mechanism, such as a protect tab on a floppy disk.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09980-356">Notes</span><span class="sxs-lookup"><span data-stu-id="09980-356">Remarks</span></span>

<span data-ttu-id="09980-357">La classe **CIM \_ PhysicalMedia** est dérivée de [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="09980-357">The **CIM\_PhysicalMedia** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="09980-358">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="09980-358">WMI does not implement this class.</span></span>

<span data-ttu-id="09980-359">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="09980-359">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="09980-360">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="09980-360">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="09980-361">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09980-361">Requirements</span></span>



| <span data-ttu-id="09980-362">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09980-362">Requirement</span></span> | <span data-ttu-id="09980-363">Valeur</span><span class="sxs-lookup"><span data-stu-id="09980-363">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09980-364">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09980-364">Minimum supported client</span></span><br/> | <span data-ttu-id="09980-365">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09980-365">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09980-366">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09980-366">Minimum supported server</span></span><br/> | <span data-ttu-id="09980-367">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09980-367">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09980-368">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="09980-368">Namespace</span></span><br/>                | <span data-ttu-id="09980-369">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="09980-369">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="09980-370">MOF</span><span class="sxs-lookup"><span data-stu-id="09980-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09980-371"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09980-371"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="09980-372">DLL</span><span class="sxs-lookup"><span data-stu-id="09980-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09980-373"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09980-373"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09980-374">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09980-374">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09980-375">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="09980-375">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

