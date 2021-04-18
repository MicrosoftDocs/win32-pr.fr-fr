---
description: La \_ classe CIM PhysicalLink représente le câblage des éléments physiques.
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: Classe CIM_PhysicalLink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524012"
---
# <a name="cim_physicallink-class"></a><span data-ttu-id="e041f-103">\_Classe CIM PhysicalLink</span><span class="sxs-lookup"><span data-stu-id="e041f-103">CIM\_PhysicalLink class</span></span>

<span data-ttu-id="e041f-104">La classe **CIM \_ PhysicalLink** représente le câblage des éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="e041f-104">The **CIM\_PhysicalLink** class represents the cabling of physical elements.</span></span> <span data-ttu-id="e041f-105">Par exemple, les câbles série ou Ethernet et les liaisons infrarouges sont des sous-classes (si des propriétés ou des associations supplémentaires sont définies) ou des instances de **\_ PhysicalLink CIM**.</span><span class="sxs-lookup"><span data-stu-id="e041f-105">For example, serial or Ethernet cables and infrared links would be subclasses (if additional properties or associations are defined) or instances of **CIM\_PhysicalLink**.</span></span> <span data-ttu-id="e041f-106">En règle générale, les nombreux câbles physiques d’un package physique ou d’un réseau ne sont pas modélisés.</span><span class="sxs-lookup"><span data-stu-id="e041f-106">Typically, the numerous physical cables within a physical package or network are not modeled.</span></span> <span data-ttu-id="e041f-107">Toutefois, lorsque les câbles ou les liens sont des composants critiques ou des ressources marquées de l’entreprise, les objets peuvent être instanciés à l’aide de cette classe ou de l’une de ses classes descendantes.</span><span class="sxs-lookup"><span data-stu-id="e041f-107">However, when the cables or links are critical components or tagged assets of the company, the objects can be instantiated using this class or one of its descendant classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e041f-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e041f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e041f-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e041f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e041f-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e041f-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e041f-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e041f-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e041f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e041f-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a><span data-ttu-id="e041f-113">Membres</span><span class="sxs-lookup"><span data-stu-id="e041f-113">Members</span></span>

<span data-ttu-id="e041f-114">La classe **CIM \_ PhysicalLink** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e041f-114">The **CIM\_PhysicalLink** class has these types of members:</span></span>

-   [<span data-ttu-id="e041f-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e041f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e041f-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e041f-116">Properties</span></span>

<span data-ttu-id="e041f-117">La classe **CIM \_ PhysicalLink** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e041f-117">The **CIM\_PhysicalLink** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e041f-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e041f-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="e041f-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e041f-122">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e041f-122">Short textual description of the object.</span></span>

<span data-ttu-id="e041f-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e041f-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-127">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e041f-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-128">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="e041f-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e041f-129">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="e041f-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e041f-130">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="e041f-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-134">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e041f-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e041f-135">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e041f-135">Textual description of the object.</span></span>

<span data-ttu-id="e041f-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e041f-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-138">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e041f-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="e041f-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e041f-141">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e041f-141">Date and time the object was installed.</span></span> <span data-ttu-id="e041f-142">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="e041f-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e041f-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-144">**Durée**</span><span class="sxs-lookup"><span data-stu-id="e041f-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-145">Type de données : **real64**</span><span class="sxs-lookup"><span data-stu-id="e041f-145">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-147">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pieds »)</span><span class="sxs-lookup"><span data-stu-id="e041f-147">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="e041f-148">Longueur actuelle du lien physique, en mètres.</span><span class="sxs-lookup"><span data-stu-id="e041f-148">Current length of the physical link, in feet.</span></span> <span data-ttu-id="e041f-149">Pour certaines connexions, en particulier les technologies sans fil, cette propriété peut ne pas être applicable et doit être laissée non initialisée.</span><span class="sxs-lookup"><span data-stu-id="e041f-149">For some connections, especially wireless technologies, this property might not be applicable and should be left uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="e041f-150">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="e041f-150">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-153">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e041f-153">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-154">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="e041f-154">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="e041f-155">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-155">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="e041f-156">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-156">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-157">**MaxLength**</span><span class="sxs-lookup"><span data-stu-id="e041f-157">**MaxLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-158">Type de données : **real64**</span><span class="sxs-lookup"><span data-stu-id="e041f-158">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-160">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« pieds »)</span><span class="sxs-lookup"><span data-stu-id="e041f-160">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="e041f-161">Longueur maximale du lien physique en pieds.</span><span class="sxs-lookup"><span data-stu-id="e041f-161">Maximum length of the physical link in feet.</span></span>

</dd> <dt>

<span data-ttu-id="e041f-162">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="e041f-162">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e041f-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e041f-165">Type de média par le biais duquel les signaux de transmission sont transmis.</span><span class="sxs-lookup"><span data-stu-id="e041f-165">Type of media through which transmission signals pass.</span></span> <span data-ttu-id="e041f-166">Les supports réseau courants incluent le câble à paire torsadée, coaxial et fibre optique.</span><span class="sxs-lookup"><span data-stu-id="e041f-166">Common network media include twisted-pair, coaxial, and fiber-optic cable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e041f-167">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e041f-167">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e041f-168">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e041f-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

<span data-ttu-id="e041f-169">**Cat1** (2)</span><span class="sxs-lookup"><span data-stu-id="e041f-169">**Cat1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

<span data-ttu-id="e041f-170">**CAT2** (3)</span><span class="sxs-lookup"><span data-stu-id="e041f-170">**Cat2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

<span data-ttu-id="e041f-171">**Cat3** (4)</span><span class="sxs-lookup"><span data-stu-id="e041f-171">**Cat3** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

<span data-ttu-id="e041f-172">**Cat4** (5)</span><span class="sxs-lookup"><span data-stu-id="e041f-172">**Cat4** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

<span data-ttu-id="e041f-173">**CAT5** (6)</span><span class="sxs-lookup"><span data-stu-id="e041f-173">**Cat5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

<span data-ttu-id="e041f-174">**50-coaxial Ohm** (7)</span><span class="sxs-lookup"><span data-stu-id="e041f-174">**50-ohm Coaxial** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

<span data-ttu-id="e041f-175">**75-coaxial Ohm** (8)</span><span class="sxs-lookup"><span data-stu-id="e041f-175">**75-ohm Coaxial** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

<span data-ttu-id="e041f-176">**100-coaxial Ohm** (9)</span><span class="sxs-lookup"><span data-stu-id="e041f-176">**100-ohm Coaxial** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

<span data-ttu-id="e041f-177">**Fibre optique** (10)</span><span class="sxs-lookup"><span data-stu-id="e041f-177">**Fiber-optic** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

<span data-ttu-id="e041f-178">**UTP** (11)</span><span class="sxs-lookup"><span data-stu-id="e041f-178">**UTP** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

<span data-ttu-id="e041f-179">**STP** (12)</span><span class="sxs-lookup"><span data-stu-id="e041f-179">**STP** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

<span data-ttu-id="e041f-180">**Câble ruban** (13)</span><span class="sxs-lookup"><span data-stu-id="e041f-180">**Ribbon Cable** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

<span data-ttu-id="e041f-181">**Twinaxial** (14)</span><span class="sxs-lookup"><span data-stu-id="e041f-181">**Twinaxial** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

<span data-ttu-id="e041f-182">**9Um optique** (15)</span><span class="sxs-lookup"><span data-stu-id="e041f-182">**Optical 9um** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

<span data-ttu-id="e041f-183">**50Um optique** (16)</span><span class="sxs-lookup"><span data-stu-id="e041f-183">**Optical 50um** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

<span data-ttu-id="e041f-184">**MU de la messagerie optique 62,5** (17)</span><span class="sxs-lookup"><span data-stu-id="e041f-184">**Optical 62.5um** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e041f-185">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="e041f-185">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-188">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e041f-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-189">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="e041f-189">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="e041f-190">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-190">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-191">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e041f-191">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-194">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e041f-194">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e041f-195">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="e041f-195">Label by which the object is known.</span></span> <span data-ttu-id="e041f-196">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="e041f-196">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e041f-197">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-198">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e041f-198">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e041f-201">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="e041f-201">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="e041f-202">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="e041f-202">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="e041f-203">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="e041f-203">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="e041f-204">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-204">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-205">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="e041f-205">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-208">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e041f-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-209">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="e041f-209">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="e041f-210">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-210">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-211">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="e041f-211">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-212">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e041f-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e041f-214">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="e041f-214">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="e041f-215">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-216">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e041f-216">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-219">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e041f-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-220">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="e041f-220">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="e041f-221">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-222">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="e041f-222">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-225">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e041f-225">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-226">Numéro d’unité de stock pour l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="e041f-226">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="e041f-227">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-228">**État**</span><span class="sxs-lookup"><span data-stu-id="e041f-228">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-231">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e041f-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e041f-232">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e041f-232">Current status of the object.</span></span>

<span data-ttu-id="e041f-233">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-233">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e041f-234">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e041f-234">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e041f-235">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="e041f-235">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e041f-236">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="e041f-236">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e041f-237">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e041f-237">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e041f-238">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="e041f-238">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e041f-239">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e041f-239">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e041f-240">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e041f-240">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e041f-241">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e041f-241">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e041f-242">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="e041f-242">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e041f-243">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="e041f-243">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e041f-244">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="e041f-244">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e041f-245">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="e041f-245">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e041f-246">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="e041f-246">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e041f-247">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e041f-247">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-250">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e041f-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-251">Chaîne arbitraire qui identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="e041f-251">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="e041f-252">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="e041f-252">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="e041f-253">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="e041f-253">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="e041f-254">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="e041f-254">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="e041f-255">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e041f-255">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="e041f-256">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="e041f-256">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="e041f-257">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-258">**Version**</span><span class="sxs-lookup"><span data-stu-id="e041f-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-259">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e041f-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e041f-261">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e041f-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e041f-262">Version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="e041f-262">Version of the physical element.</span></span>

<span data-ttu-id="e041f-263">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e041f-264">**Fil**</span><span class="sxs-lookup"><span data-stu-id="e041f-264">**Wired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e041f-265">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e041f-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e041f-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e041f-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e041f-267">Si la **valeur est true**, le lien physique est un câble.</span><span class="sxs-lookup"><span data-stu-id="e041f-267">If **TRUE**, the physical link is a cable.</span></span> <span data-ttu-id="e041f-268">Dans le cas contraire, il s’agit d’une connexion sans fil.</span><span class="sxs-lookup"><span data-stu-id="e041f-268">Otherwise, it is a wireless connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e041f-269">Notes</span><span class="sxs-lookup"><span data-stu-id="e041f-269">Remarks</span></span>

<span data-ttu-id="e041f-270">La classe **CIM \_ PhysicalLink** est dérivée de [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-270">The **CIM\_PhysicalLink** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="e041f-271">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="e041f-271">WMI does not implement this class.</span></span>

<span data-ttu-id="e041f-272">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e041f-272">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e041f-273">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e041f-273">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e041f-274">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e041f-274">Requirements</span></span>



| <span data-ttu-id="e041f-275">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e041f-275">Requirement</span></span> | <span data-ttu-id="e041f-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="e041f-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e041f-277">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e041f-277">Minimum supported client</span></span><br/> | <span data-ttu-id="e041f-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e041f-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e041f-279">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e041f-279">Minimum supported server</span></span><br/> | <span data-ttu-id="e041f-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e041f-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e041f-281">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e041f-281">Namespace</span></span><br/>                | <span data-ttu-id="e041f-282">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e041f-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e041f-283">MOF</span><span class="sxs-lookup"><span data-stu-id="e041f-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e041f-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e041f-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e041f-285">DLL</span><span class="sxs-lookup"><span data-stu-id="e041f-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e041f-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e041f-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e041f-287">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e041f-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e041f-288">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e041f-288">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

