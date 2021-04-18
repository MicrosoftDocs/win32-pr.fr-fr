---
description: La \_ classe de puces CIM représente le type de matériel de circuit intégré, y compris les ASIC, les processeurs, les puces de mémoire, et ainsi de suite.
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: Classe CIM_Chip
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483552"
---
# <a name="cim_chip-class"></a><span data-ttu-id="8f634-103">\_Classe de puce CIM</span><span class="sxs-lookup"><span data-stu-id="8f634-103">CIM\_Chip class</span></span>

<span data-ttu-id="8f634-104">La classe de **\_ puces CIM** représente le type de matériel de circuit intégré, y compris les ASIC, les processeurs, les puces de mémoire, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="8f634-104">The **CIM\_Chip** class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f634-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8f634-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8f634-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8f634-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8f634-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8f634-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8f634-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8f634-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f634-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f634-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
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
  uint16   FormFactor;
};
```

## <a name="members"></a><span data-ttu-id="8f634-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8f634-110">Members</span></span>

<span data-ttu-id="8f634-111">La classe de **\_ puce CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8f634-111">The **CIM\_Chip** class has these types of members:</span></span>

-   [<span data-ttu-id="8f634-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f634-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f634-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f634-113">Properties</span></span>

<span data-ttu-id="8f634-114">La classe de **\_ puce CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8f634-114">The **CIM\_Chip** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f634-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8f634-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="8f634-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8f634-119">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f634-119">A short textual description of the object.</span></span>

<span data-ttu-id="8f634-120">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f634-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-124">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f634-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-125">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="8f634-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8f634-126">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="8f634-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8f634-127">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-127">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="8f634-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-131">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8f634-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8f634-132">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f634-132">A textual description of the object.</span></span>

<span data-ttu-id="8f634-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-134">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="8f634-134">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f634-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f634-137">Facteur de forme d’implémentation pour la puce.</span><span class="sxs-lookup"><span data-stu-id="8f634-137">Implementation form factor for the chip.</span></span> <span data-ttu-id="8f634-138">Les valeurs suivantes peuvent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="8f634-138">The following values can be specified.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f634-139">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8f634-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8f634-140">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8f634-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="8f634-141">**SIP** (2)</span><span class="sxs-lookup"><span data-stu-id="8f634-141">**SIP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

<span data-ttu-id="8f634-142">**DIP** (3)</span><span class="sxs-lookup"><span data-stu-id="8f634-142">**DIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

<span data-ttu-id="8f634-143">**Code postal** (4)</span><span class="sxs-lookup"><span data-stu-id="8f634-143">**ZIP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

<span data-ttu-id="8f634-144">**SOJ** (5)</span><span class="sxs-lookup"><span data-stu-id="8f634-144">**SOJ** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="8f634-145">**Propriétaire** (6)</span><span class="sxs-lookup"><span data-stu-id="8f634-145">**Proprietary** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

<span data-ttu-id="8f634-146">**SIMM** (7)</span><span class="sxs-lookup"><span data-stu-id="8f634-146">**SIMM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

<span data-ttu-id="8f634-147">**DIMM** (8)</span><span class="sxs-lookup"><span data-stu-id="8f634-147">**DIMM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

<span data-ttu-id="8f634-148">**TSOP** (9)</span><span class="sxs-lookup"><span data-stu-id="8f634-148">**TSOP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

<span data-ttu-id="8f634-149">**PGA** (10)</span><span class="sxs-lookup"><span data-stu-id="8f634-149">**PGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

<span data-ttu-id="8f634-150">**RIMM** (11)</span><span class="sxs-lookup"><span data-stu-id="8f634-150">**RIMM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

<span data-ttu-id="8f634-151">**SODIMM** (12)</span><span class="sxs-lookup"><span data-stu-id="8f634-151">**SODIMM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

<span data-ttu-id="8f634-152">**SRIMM** (13)</span><span class="sxs-lookup"><span data-stu-id="8f634-152">**SRIMM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

<span data-ttu-id="8f634-153">**SMD** (14)</span><span class="sxs-lookup"><span data-stu-id="8f634-153">**SMD** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

<span data-ttu-id="8f634-154">**SSMP** (15)</span><span class="sxs-lookup"><span data-stu-id="8f634-154">**SSMP** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

<span data-ttu-id="8f634-155">**QFP** (16)</span><span class="sxs-lookup"><span data-stu-id="8f634-155">**QFP** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

<span data-ttu-id="8f634-156">**TQFP** (17)</span><span class="sxs-lookup"><span data-stu-id="8f634-156">**TQFP** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

<span data-ttu-id="8f634-157">**SOIC** (18)</span><span class="sxs-lookup"><span data-stu-id="8f634-157">**SOIC** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

<span data-ttu-id="8f634-158">**Carte LCC** (19)</span><span class="sxs-lookup"><span data-stu-id="8f634-158">**LCC** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

<span data-ttu-id="8f634-159">**PLCC** (20)</span><span class="sxs-lookup"><span data-stu-id="8f634-159">**PLCC** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

<span data-ttu-id="8f634-160">**BGA** (21)</span><span class="sxs-lookup"><span data-stu-id="8f634-160">**BGA** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

<span data-ttu-id="8f634-161">**FPBGA** (22)</span><span class="sxs-lookup"><span data-stu-id="8f634-161">**FPBGA** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

<span data-ttu-id="8f634-162">**LGA** (23)</span><span class="sxs-lookup"><span data-stu-id="8f634-162">**LGA** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

<span data-ttu-id="8f634-163">**FB-DIMM** (24)</span><span class="sxs-lookup"><span data-stu-id="8f634-163">**FB-DIMM** (24)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f634-164">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="8f634-164">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-165">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f634-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f634-167">Si la **valeur est true**, le package peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="8f634-167">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="8f634-168">Un package physique peut être échangé à chaud si l’élément peut être remplacé par un différent physiquement (mais équivalent), alors que le package qui le contient est activé.</span><span class="sxs-lookup"><span data-stu-id="8f634-168">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="8f634-169">Par exemple, un composant de ventilateur peut être conçu pour être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="8f634-169">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="8f634-170">Tous les composants pouvant être permutés à chaud sont intrinsèquement amovibles et remplaçables.</span><span class="sxs-lookup"><span data-stu-id="8f634-170">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="8f634-171">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-171">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f634-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-173">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f634-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-175">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="8f634-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8f634-176">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="8f634-176">Indicates when the object was installed.</span></span> <span data-ttu-id="8f634-177">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="8f634-177">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8f634-178">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-179">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="8f634-179">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-182">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f634-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-183">Nom de l’organisation responsable de la production de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="8f634-183">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="8f634-184">Pour plus d’informations, consultez la propriété **Vendor** du [**\_ produit CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-184">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="8f634-185">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-185">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-186">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="8f634-186">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-189">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f634-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-190">Nom par lequel l’élément physique est généralement connu.</span><span class="sxs-lookup"><span data-stu-id="8f634-190">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="8f634-191">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-191">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-192">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8f634-192">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-195">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8f634-195">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8f634-196">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="8f634-196">Label by which the object is known.</span></span> <span data-ttu-id="8f634-197">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="8f634-197">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8f634-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-199">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8f634-199">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f634-202">Données supplémentaires, au-delà des informations de balise d’actifs, qui peuvent être utilisées pour identifier un élément physique.</span><span class="sxs-lookup"><span data-stu-id="8f634-202">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="8f634-203">Par exemple, les données de code-barres sont associées à un élément, qui a également une balise de ressource.</span><span class="sxs-lookup"><span data-stu-id="8f634-203">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="8f634-204">Notez que si seules les données de code-barres sont disponibles et qu’elles sont uniques et peuvent être utilisées en tant que clé d’élément, cette propriété est null et les données de code-barres sont utilisées comme clé de classe dans la propriété de **balise** .</span><span class="sxs-lookup"><span data-stu-id="8f634-204">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="8f634-205">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-206">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="8f634-206">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-209">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f634-209">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-210">Numéro de référence attribué par l’organisation responsable de la production ou de la fabrication de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="8f634-210">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="8f634-211">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-211">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-212">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="8f634-212">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-213">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f634-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f634-215">Si la **valeur est true**, l’élément physique est sous tension.</span><span class="sxs-lookup"><span data-stu-id="8f634-215">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="8f634-216">Dans le cas contraire, elle est actuellement désactivée.</span><span class="sxs-lookup"><span data-stu-id="8f634-216">Otherwise, it is currently off.</span></span>

<span data-ttu-id="8f634-217">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-217">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-218">**Bande**</span><span class="sxs-lookup"><span data-stu-id="8f634-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f634-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f634-221">Si la **valeur est true**, cet élément est conçu pour être pris dans et hors du conteneur physique dans lequel il se trouve normalement, sans altérer la fonction de l’empaquetage global.</span><span class="sxs-lookup"><span data-stu-id="8f634-221">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="8f634-222">Un package est considéré comme amovible même si l’alimentation doit être désactivée pour effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="8f634-222">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="8f634-223">Si l’alimentation peut être activée et que le package a été supprimé, l’élément est alors amovible et peut être échangé à chaud.</span><span class="sxs-lookup"><span data-stu-id="8f634-223">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="8f634-224">Par exemple, une puce de processeur extensible est amovible.</span><span class="sxs-lookup"><span data-stu-id="8f634-224">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="8f634-225">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-225">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-226">**Remplaçables**</span><span class="sxs-lookup"><span data-stu-id="8f634-226">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-227">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8f634-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f634-229">Si la **valeur est true**, il est possible de remplacer l’élément par un élément différent physiquement.</span><span class="sxs-lookup"><span data-stu-id="8f634-229">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="8f634-230">Par exemple, certains systèmes informatiques autorisent la mise à niveau de la puce du processeur principal vers une évaluation de l’horloge plus élevée.</span><span class="sxs-lookup"><span data-stu-id="8f634-230">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="8f634-231">Dans ce cas, on dit que le processeur est remplaçable.</span><span class="sxs-lookup"><span data-stu-id="8f634-231">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="8f634-232">Tous les composants amovibles sont remplaçables par nature.</span><span class="sxs-lookup"><span data-stu-id="8f634-232">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="8f634-233">Cette propriété est héritée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-233">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-234">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="8f634-234">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-237">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f634-237">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-238">Numéro alloué par le fabricant utilisé pour identifier l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="8f634-238">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="8f634-239">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-240">**Référence (SKU)**</span><span class="sxs-lookup"><span data-stu-id="8f634-240">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-243">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f634-243">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-244">Numéro d’unité de conservation pour cet élément physique.</span><span class="sxs-lookup"><span data-stu-id="8f634-244">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="8f634-245">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-245">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-246">**État**</span><span class="sxs-lookup"><span data-stu-id="8f634-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-249">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8f634-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8f634-250">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f634-250">String that indicates the current status of the object.</span></span> <span data-ttu-id="8f634-251">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="8f634-251">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8f634-252">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="8f634-252">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8f634-253">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="8f634-253">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8f634-254">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="8f634-254">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8f634-255">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="8f634-255">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8f634-256">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="8f634-256">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8f634-257">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-257">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8f634-258">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f634-258">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8f634-259">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="8f634-259">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8f634-260">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="8f634-260">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8f634-261">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8f634-261">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f634-262">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="8f634-262">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8f634-263">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8f634-263">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8f634-264">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8f634-264">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8f634-265">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8f634-265">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8f634-266">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="8f634-266">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8f634-267">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="8f634-267">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8f634-268">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="8f634-268">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8f634-269">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="8f634-269">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8f634-270">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="8f634-270">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f634-271">**Tag**</span><span class="sxs-lookup"><span data-stu-id="8f634-271">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-274">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8f634-274">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-275">Identifie de façon unique l’élément physique et sert de clé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8f634-275">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="8f634-276">Cette propriété peut contenir des informations, telles que des données de numéro de série ou de balise d’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8f634-276">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="8f634-277">La clé de [**\_ PhysicalElement CIM**](cim-physicalelement.md) est placée très haut dans la hiérarchie d’objets pour identifier indépendamment le matériel ou l’entité, quel que soit l’emplacement physique des armoires, des adaptateurs, etc.</span><span class="sxs-lookup"><span data-stu-id="8f634-277">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="8f634-278">Par exemple, un composant amovible pouvant être échangé à chaud peut être extrait de son package conteneur (d’étendue) et être temporairement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="8f634-278">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="8f634-279">L’objet continue à exister et peut même être inséré dans un autre conteneur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8f634-279">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="8f634-280">La clé d’un élément physique est une chaîne arbitraire qui est définie indépendamment de l’emplacement ou de la hiérarchie orientée emplacement.</span><span class="sxs-lookup"><span data-stu-id="8f634-280">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="8f634-281">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f634-282">**Version**</span><span class="sxs-lookup"><span data-stu-id="8f634-282">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f634-283">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f634-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f634-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f634-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f634-285">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f634-285">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f634-286">Indique la version de l’élément physique.</span><span class="sxs-lookup"><span data-stu-id="8f634-286">Indicates the version of the physical element.</span></span>

<span data-ttu-id="8f634-287">Cette propriété est héritée de la [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f634-288">Notes</span><span class="sxs-lookup"><span data-stu-id="8f634-288">Remarks</span></span>

<span data-ttu-id="8f634-289">La classe de **\_ puce CIM** est dérivée de la [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-289">The **CIM\_Chip** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="8f634-290">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8f634-290">WMI does not implement this class.</span></span> <span data-ttu-id="8f634-291">Pour plus d’informations sur les classes dérivées de la **\_ puce CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8f634-291">For more information about classes derived from **CIM\_Chip**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8f634-292">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8f634-292">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8f634-293">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8f634-293">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f634-294">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f634-294">Requirements</span></span>



| <span data-ttu-id="8f634-295">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f634-295">Requirement</span></span> | <span data-ttu-id="8f634-296">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f634-296">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f634-297">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f634-297">Minimum supported client</span></span><br/> | <span data-ttu-id="8f634-298">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f634-298">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f634-299">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f634-299">Minimum supported server</span></span><br/> | <span data-ttu-id="8f634-300">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f634-300">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f634-301">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8f634-301">Namespace</span></span><br/>                | <span data-ttu-id="8f634-302">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8f634-302">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f634-303">MOF</span><span class="sxs-lookup"><span data-stu-id="8f634-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f634-304"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f634-304"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f634-305">DLL</span><span class="sxs-lookup"><span data-stu-id="8f634-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f634-306"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f634-306"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f634-307">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f634-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f634-308">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8f634-308">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

