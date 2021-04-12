---
description: La \_ classe CIM PhysicalComponent représente un composant de base ou de bas niveau au sein d’un package. Un élément physique qui n’est pas un lien, un connecteur ou un package est un descendant (ou membre) de cette classe.
ms.assetid: 079874cd-5717-4662-a192-0ced16270bbd
ms.tgt_platform: multiple
title: Classe CIM_PhysicalComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalComponent
- CIM_PhysicalComponent.Caption
- CIM_PhysicalComponent.Description
- CIM_PhysicalComponent.InstallDate
- CIM_PhysicalComponent.Name
- CIM_PhysicalComponent.Status
- CIM_PhysicalComponent.CreationClassName
- CIM_PhysicalComponent.Manufacturer
- CIM_PhysicalComponent.Model
- CIM_PhysicalComponent.OtherIdentifyingInfo
- CIM_PhysicalComponent.PartNumber
- CIM_PhysicalComponent.PoweredOn
- CIM_PhysicalComponent.SerialNumber
- CIM_PhysicalComponent.SKU
- CIM_PhysicalComponent.Tag
- CIM_PhysicalComponent.Version
- CIM_PhysicalComponent.HotSwappable
- CIM_PhysicalComponent.Removable
- CIM_PhysicalComponent.Replaceable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7e1db2c1d314b2d45816801643912dcf3b31bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483521"
---
# <a name="cim_physicalcomponent-class"></a><span data-ttu-id="078b7-104">\_Classe CIM PhysicalComponent</span><span class="sxs-lookup"><span data-stu-id="078b7-104">CIM\_PhysicalComponent class</span></span>

<span data-ttu-id="078b7-105">La classe **CIM \_ PhysicalComponent** représente un composant de base ou de bas niveau au sein d’un package.</span><span class="sxs-lookup"><span data-stu-id="078b7-105">The **CIM\_PhysicalComponent** class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="078b7-106">Un élément physique qui n’est pas un lien, un connecteur ou un package est un descendant (ou membre) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="078b7-106">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span> <span data-ttu-id="078b7-107">Par exemple, le circuit microprogrammé UART sur une carte modem interne est une sous-classe (si des propriétés ou des associations supplémentaires sont définies) ou une instance de **\_ PhysicalComponent CIM**.</span><span class="sxs-lookup"><span data-stu-id="078b7-107">For example, the UART chipset on an internal modem card would be a subclass (if additional properties or associations are defined) or an instance of **CIM\_PhysicalComponent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="078b7-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="078b7-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="078b7-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="078b7-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="078b7-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="078b7-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="078b7-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="078b7-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="078b7-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="078b7-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B78-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalComponent : CIM_PhysicalElement
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
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
};
```

## <a name="members"></a><span data-ttu-id="078b7-113">Membres</span><span class="sxs-lookup"><span data-stu-id="078b7-113">Members</span></span>

<span data-ttu-id="078b7-114">La classe **CIM \_ PhysicalComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="078b7-114">The **CIM\_PhysicalComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="078b7-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="078b7-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="078b7-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="078b7-116">Properties</span></span>

<span data-ttu-id="078b7-117">La classe **CIM \_ PhysicalComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="078b7-117">The **CIM\_PhysicalComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="078b7-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="078b7-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="078b7-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="078b7-122">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="078b7-122">A short textual description of the object.</span></span>

<span data-ttu-id="078b7-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="078b7-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-127">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="078b7-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-128">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="078b7-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="078b7-129">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="078b7-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="078b7-130">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="078b7-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-134">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="078b7-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="078b7-135">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="078b7-135">A textual description of the object.</span></span>

<span data-ttu-id="078b7-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-137">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="078b7-137">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-138">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="078b7-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078b7-140">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="078b7-140">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="078b7-141">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="078b7-141">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="078b7-142">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="078b7-142">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="078b7-143">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="078b7-143">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="078b7-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="078b7-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-145">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="078b7-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-147">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="078b7-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="078b7-148">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="078b7-148">Indicates when the object was installed.</span></span> <span data-ttu-id="078b7-149">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="078b7-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="078b7-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-151">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="078b7-151">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-154">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="078b7-154">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-155">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="078b7-155">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="078b7-156">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-156">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="078b7-157">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-157">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-158">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="078b7-158">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-161">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="078b7-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-162">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="078b7-162">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="078b7-163">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-163">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-164">**Nom**</span><span class="sxs-lookup"><span data-stu-id="078b7-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-167">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="078b7-167">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="078b7-168">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="078b7-168">Label by which the object is known.</span></span> <span data-ttu-id="078b7-169">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="078b7-169">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="078b7-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-171">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="078b7-171">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078b7-174">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="078b7-174">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="078b7-175">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="078b7-175">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="078b7-176">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="078b7-176">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="078b7-177">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-177">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-178">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="078b7-178">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-181">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="078b7-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-182">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="078b7-182">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="078b7-183">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-183">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-184">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="078b7-184">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-185">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="078b7-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078b7-187">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="078b7-187">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="078b7-188">Dans le cas contraire, elle est actuellement désactivée.</span><span class="sxs-lookup"><span data-stu-id="078b7-188">Otherwise, it is currently off.</span></span>

<span data-ttu-id="078b7-189">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-189">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-190">**Bande**</span><span class="sxs-lookup"><span data-stu-id="078b7-190">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-191">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="078b7-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078b7-193">Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="078b7-193">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="078b7-194">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="078b7-194">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="078b7-195">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="078b7-195">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="078b7-196">Par exemple, une puce de processeur extensible est amovible.</span><span class="sxs-lookup"><span data-stu-id="078b7-196">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="078b7-197">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="078b7-197">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-198">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="078b7-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078b7-200">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="078b7-200">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="078b7-201">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="078b7-201">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="078b7-202">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="078b7-202">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="078b7-203">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="078b7-203">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="078b7-204">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="078b7-204">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-207">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="078b7-207">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-208">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="078b7-208">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="078b7-209">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-209">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-210">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="078b7-210">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-213">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="078b7-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-214">Numéro d’unité de conservation pour cet élément physique.</span><span class="sxs-lookup"><span data-stu-id="078b7-214">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="078b7-215">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-216">**État**</span><span class="sxs-lookup"><span data-stu-id="078b7-216">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-219">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="078b7-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="078b7-220">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="078b7-220">String that indicates the current status of the object.</span></span> <span data-ttu-id="078b7-221">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="078b7-221">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="078b7-222">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="078b7-222">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="078b7-223">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="078b7-223">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="078b7-224">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="078b7-224">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="078b7-225">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="078b7-225">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="078b7-226">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="078b7-226">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="078b7-227">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="078b7-228">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="078b7-228">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="078b7-229">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="078b7-229">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="078b7-230">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="078b7-230">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="078b7-231">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="078b7-231">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="078b7-232">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="078b7-232">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="078b7-233">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="078b7-233">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="078b7-234">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="078b7-234">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="078b7-235">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="078b7-235">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="078b7-236">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="078b7-236">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="078b7-237">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="078b7-237">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="078b7-238">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="078b7-238">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="078b7-239">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="078b7-239">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="078b7-240">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="078b7-240">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="078b7-241">**Tag**</span><span class="sxs-lookup"><span data-stu-id="078b7-241">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-244">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="078b7-244">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-245">Identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="078b7-245">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="078b7-246">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="078b7-246">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="078b7-247">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="078b7-247">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="078b7-248">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="078b7-248">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="078b7-249">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="078b7-249">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="078b7-250">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="078b7-250">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="078b7-251">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-251">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="078b7-252">**Version**</span><span class="sxs-lookup"><span data-stu-id="078b7-252">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078b7-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="078b7-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078b7-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="078b7-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078b7-255">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="078b7-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="078b7-256">Indique la version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="078b7-256">Indicates the version of the physical element.</span></span>

<span data-ttu-id="078b7-257">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="078b7-258">Notes</span><span class="sxs-lookup"><span data-stu-id="078b7-258">Remarks</span></span>

<span data-ttu-id="078b7-259">La classe **CIM \_ PhysicalComponent** est dérivée de [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-259">The **CIM\_PhysicalComponent** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="078b7-260">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="078b7-260">WMI does not implement this class.</span></span> <span data-ttu-id="078b7-261">Pour les classes WMI dérivées de **CIM \_ PhysicalComponent**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="078b7-261">For WMI classes derived from **CIM\_PhysicalComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="078b7-262">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="078b7-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="078b7-263">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="078b7-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="078b7-264">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="078b7-264">Requirements</span></span>



| <span data-ttu-id="078b7-265">Condition requise</span><span class="sxs-lookup"><span data-stu-id="078b7-265">Requirement</span></span> | <span data-ttu-id="078b7-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="078b7-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="078b7-267">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="078b7-267">Minimum supported client</span></span><br/> | <span data-ttu-id="078b7-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="078b7-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="078b7-269">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="078b7-269">Minimum supported server</span></span><br/> | <span data-ttu-id="078b7-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="078b7-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="078b7-271">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="078b7-271">Namespace</span></span><br/>                | <span data-ttu-id="078b7-272">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="078b7-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="078b7-273">MOF</span><span class="sxs-lookup"><span data-stu-id="078b7-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="078b7-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="078b7-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="078b7-275">DLL</span><span class="sxs-lookup"><span data-stu-id="078b7-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="078b7-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="078b7-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="078b7-277">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="078b7-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078b7-278">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="078b7-278">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

