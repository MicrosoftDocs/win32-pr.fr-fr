---
description: Les \_ sous-classes PHYSICALELEMENT CIM définissent tout composant d’un système qui a une identité physique distincte. Les instances de cette classe peuvent être définies en termes d’étiquettes qui peuvent être physiquement attachées à l’objet.
ms.assetid: 7ba6d1a9-f449-4ae2-a37c-517245bea39e
ms.tgt_platform: multiple
title: Classe CIM_PhysicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElement
- CIM_PhysicalElement.Caption
- CIM_PhysicalElement.Description
- CIM_PhysicalElement.InstallDate
- CIM_PhysicalElement.Name
- CIM_PhysicalElement.Status
- CIM_PhysicalElement.CreationClassName
- CIM_PhysicalElement.Manufacturer
- CIM_PhysicalElement.Model
- CIM_PhysicalElement.OtherIdentifyingInfo
- CIM_PhysicalElement.PartNumber
- CIM_PhysicalElement.PoweredOn
- CIM_PhysicalElement.SerialNumber
- CIM_PhysicalElement.SKU
- CIM_PhysicalElement.Tag
- CIM_PhysicalElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5afeda74789bc492aac3d37629b64385b8734f60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523119"
---
# <a name="cim_physicalelement-class"></a><span data-ttu-id="fedb2-104">\_Classe CIM PhysicalElement</span><span class="sxs-lookup"><span data-stu-id="fedb2-104">CIM\_PhysicalElement class</span></span>

<span data-ttu-id="fedb2-105">Les sous-classes **\_ PhysicalElement CIM** définissent tout composant d’un système qui a une identité physique distincte.</span><span class="sxs-lookup"><span data-stu-id="fedb2-105">The **CIM\_PhysicalElement** subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="fedb2-106">Les instances de cette classe peuvent être définies en termes d’étiquettes qui peuvent être physiquement attachées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="fedb2-106">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span> <span data-ttu-id="fedb2-107">Tous les processus, fichiers et périphériques logiques ne sont pas considérés comme des éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="fedb2-107">All processes, files, and logical devices are not considered to be physical elements.</span></span> <span data-ttu-id="fedb2-108">Par exemple, il n’est pas possible d’attacher une étiquette à un modem ; Il est uniquement possible d’attacher une étiquette à la carte qui implémente le modem.</span><span class="sxs-lookup"><span data-stu-id="fedb2-108">For example, it is not possible to attach a label to a modem; it is only possible to attach a label to the card that implements the modem.</span></span> <span data-ttu-id="fedb2-109">La même carte peut également implémenter une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="fedb2-109">The same card could also implement a LAN adapter.</span></span>

<span data-ttu-id="fedb2-110">Les éléments système gérés tangibles (généralement des éléments matériels) ont une manifeste physique.</span><span class="sxs-lookup"><span data-stu-id="fedb2-110">Tangible managed system elements (usually hardware items) have a physical manifestation.</span></span> <span data-ttu-id="fedb2-111">Un élément système managé n’est pas nécessairement un composant discret.</span><span class="sxs-lookup"><span data-stu-id="fedb2-111">A managed system element is not necessarily a discrete component.</span></span> <span data-ttu-id="fedb2-112">Par exemple, il est possible qu’une seule carte (un type d’élément physique) héberge plusieurs unités logiques.</span><span class="sxs-lookup"><span data-stu-id="fedb2-112">For example, it is possible for a single card (a type of physical element) to host more than one logical device.</span></span> <span data-ttu-id="fedb2-113">La carte est représentée par un seul élément physique associé à plusieurs unités logiques.</span><span class="sxs-lookup"><span data-stu-id="fedb2-113">The card would be represented by a single physical element associated with multiple logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fedb2-114">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="fedb2-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fedb2-115">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fedb2-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fedb2-116">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fedb2-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fedb2-117">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="fedb2-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fedb2-118">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fedb2-118">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B61-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElement : CIM_ManagedSystemElement
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
};
```

## <a name="members"></a><span data-ttu-id="fedb2-119">Membres</span><span class="sxs-lookup"><span data-stu-id="fedb2-119">Members</span></span>

<span data-ttu-id="fedb2-120">La classe **CIM \_ PhysicalElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fedb2-120">The **CIM\_PhysicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="fedb2-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fedb2-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fedb2-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fedb2-122">Properties</span></span>

<span data-ttu-id="fedb2-123">La classe **CIM \_ PhysicalElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fedb2-123">The **CIM\_PhysicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fedb2-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fedb2-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-127">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-128">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fedb2-128">A short textual description of the object.</span></span>

<span data-ttu-id="fedb2-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fedb2-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fedb2-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-133">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fedb2-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-134">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="fedb2-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fedb2-135">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="fedb2-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-136">**Description**</span><span class="sxs-lookup"><span data-stu-id="fedb2-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-139">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="fedb2-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-140">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fedb2-140">A textual description of the object.</span></span>

<span data-ttu-id="fedb2-141">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fedb2-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fedb2-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-143">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fedb2-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-145">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="fedb2-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-146">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="fedb2-146">Indicates when the object was installed.</span></span> <span data-ttu-id="fedb2-147">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="fedb2-147">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fedb2-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fedb2-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-149">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="fedb2-149">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-152">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fedb2-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-153">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="fedb2-153">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="fedb2-154">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="fedb2-154">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-155">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="fedb2-155">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-158">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fedb2-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-159">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="fedb2-159">Name by which the physical element is generally known.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-160">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fedb2-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-163">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fedb2-163">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-164">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="fedb2-164">Label by which the object is known.</span></span> <span data-ttu-id="fedb2-165">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="fedb2-165">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fedb2-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fedb2-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-167">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="fedb2-167">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-170">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="fedb2-170">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="fedb2-171">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="fedb2-171">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="fedb2-172">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="fedb2-172">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-173">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="fedb2-173">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-176">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fedb2-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-177">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="fedb2-177">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-178">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="fedb2-178">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-179">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fedb2-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-181">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="fedb2-181">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="fedb2-182">Dans le cas contraire, elle est actuellement désactivée.</span><span class="sxs-lookup"><span data-stu-id="fedb2-182">Otherwise, it is currently off.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="fedb2-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-186">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fedb2-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-187">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="fedb2-187">Manufacturer-allocated number used to identify the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-188">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="fedb2-188">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-191">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fedb2-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-192">Numéro d’unité de conservation pour cet élément physique.</span><span class="sxs-lookup"><span data-stu-id="fedb2-192">Stock-keeping unit number for this physical element.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-193">**État**</span><span class="sxs-lookup"><span data-stu-id="fedb2-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-196">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="fedb2-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-197">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fedb2-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="fedb2-198">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="fedb2-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fedb2-199">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="fedb2-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fedb2-200">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="fedb2-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fedb2-201">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="fedb2-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fedb2-202">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="fedb2-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fedb2-203">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="fedb2-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fedb2-204">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fedb2-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fedb2-205">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fedb2-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fedb2-206">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fedb2-207">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fedb2-208">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fedb2-209">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="fedb2-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fedb2-210">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fedb2-211">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fedb2-212">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fedb2-213">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fedb2-214">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fedb2-215">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fedb2-216">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fedb2-217">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="fedb2-217">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fedb2-218">**Tag**</span><span class="sxs-lookup"><span data-stu-id="fedb2-218">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-221">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fedb2-221">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-222">Identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="fedb2-222">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="fedb2-223">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="fedb2-223">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="fedb2-224">La clé de **\_ PhysicalElement CIM** est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="fedb2-224">The key for **CIM\_PhysicalElement** is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="fedb2-225">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="fedb2-225">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="fedb2-226">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="fedb2-226">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="fedb2-227">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="fedb2-227">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="fedb2-228">**Version**</span><span class="sxs-lookup"><span data-stu-id="fedb2-228">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fedb2-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fedb2-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fedb2-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fedb2-231">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="fedb2-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fedb2-232">Indique la version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="fedb2-232">Indicates the version of the physical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fedb2-233">Notes</span><span class="sxs-lookup"><span data-stu-id="fedb2-233">Remarks</span></span>

<span data-ttu-id="fedb2-234">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="fedb2-234">WMI does not implement this class.</span></span> <span data-ttu-id="fedb2-235">Pour les classes WMI dérivées de **CIM \_ PhysicalElement**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fedb2-235">For WMI classes derived from **CIM\_PhysicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fedb2-236">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="fedb2-236">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fedb2-237">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fedb2-237">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fedb2-238">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fedb2-238">Requirements</span></span>



| <span data-ttu-id="fedb2-239">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fedb2-239">Requirement</span></span> | <span data-ttu-id="fedb2-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="fedb2-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fedb2-241">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fedb2-241">Minimum supported client</span></span><br/> | <span data-ttu-id="fedb2-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fedb2-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fedb2-243">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fedb2-243">Minimum supported server</span></span><br/> | <span data-ttu-id="fedb2-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fedb2-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fedb2-245">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fedb2-245">Namespace</span></span><br/>                | <span data-ttu-id="fedb2-246">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="fedb2-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fedb2-247">MOF</span><span class="sxs-lookup"><span data-stu-id="fedb2-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fedb2-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fedb2-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fedb2-249">DLL</span><span class="sxs-lookup"><span data-stu-id="fedb2-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fedb2-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fedb2-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fedb2-251">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fedb2-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedb2-252">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="fedb2-252">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

