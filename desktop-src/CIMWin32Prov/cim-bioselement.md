---
description: La \_ classe CIM BIOSElement représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique.
ms.assetid: c203244a-51e0-4733-a0bc-cf9b7957f364
ms.tgt_platform: multiple
title: CIM_BIOSElement, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Caption
- CIM_BIOSElement.Description
- CIM_BIOSElement.InstallDate
- CIM_BIOSElement.Status
- CIM_BIOSElement.Name
- CIM_BIOSElement.BuildNumber
- CIM_BIOSElement.CodeSet
- CIM_BIOSElement.IdentificationCode
- CIM_BIOSElement.LanguageEdition
- CIM_BIOSElement.OtherTargetOS
- CIM_BIOSElement.SerialNumber
- CIM_BIOSElement.SoftwareElementID
- CIM_BIOSElement.SoftwareElementState
- CIM_BIOSElement.TargetOperatingSystem
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.Version
- CIM_BIOSElement.PrimaryBIOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21cd0d13d62f5cfa70f579110480b4c11c36b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033728"
---
# <a name="cim_bioselement-class-cimwin32-wmi-providers"></a><span data-ttu-id="67660-103">CIM_BIOSElement, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="67660-103">CIM_BIOSElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="67660-104">La classe **CIM \_ BIOSElement** représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique.</span><span class="sxs-lookup"><span data-stu-id="67660-104">The **CIM\_BIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67660-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="67660-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="67660-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="67660-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="67660-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="67660-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="67660-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="67660-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67660-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67660-109">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C562-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  string   BuildNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  uint16   TargetOperatingSystem;
  string   Manufacturer;
  string   Version;
  boolean  PrimaryBIOS;
};
```

## <a name="members"></a><span data-ttu-id="67660-110">Membres</span><span class="sxs-lookup"><span data-stu-id="67660-110">Members</span></span>

<span data-ttu-id="67660-111">La classe **CIM \_ BIOSElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="67660-111">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="67660-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67660-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67660-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67660-113">Properties</span></span>

<span data-ttu-id="67660-114">La classe **CIM \_ BIOSElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="67660-114">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67660-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="67660-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-118">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur les composants logiciels DMTF \| 002,4»)</span><span class="sxs-lookup"><span data-stu-id="67660-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="67660-119">Identificateur interne pour la compilation de cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="67660-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="67660-120">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="67660-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-124">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="67660-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="67660-125">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="67660-125">A short textual description of the object.</span></span>

<span data-ttu-id="67660-126">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-127">**Codes**</span><span class="sxs-lookup"><span data-stu-id="67660-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-130">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="67660-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="67660-131">Ensemble de codes utilisé par l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="67660-131">Code set used by the software element.</span></span>

<span data-ttu-id="67660-132">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-133">**Description**</span><span class="sxs-lookup"><span data-stu-id="67660-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-136">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="67660-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="67660-137">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="67660-137">A textual description of the object.</span></span>

<span data-ttu-id="67660-138">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="67660-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-142">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur les composants logiciels DMTF \| 002,7»)</span><span class="sxs-lookup"><span data-stu-id="67660-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="67660-143">Identificateur du fabricant de l’élément logiciel, souvent une unité de conservation ou un numéro de référence.</span><span class="sxs-lookup"><span data-stu-id="67660-143">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="67660-144">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="67660-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-146">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67660-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67660-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="67660-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="67660-149">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="67660-149">Indicates when the object was installed.</span></span> <span data-ttu-id="67660-150">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="67660-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="67660-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="67660-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-155">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur les composants logiciels DMTF \| 002,6»)</span><span class="sxs-lookup"><span data-stu-id="67660-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="67660-156">Édition de langue de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="67660-156">Language edition of the software element.</span></span> <span data-ttu-id="67660-157">Les codes de langue définis dans ISO 639 doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="67660-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="67660-158">Lorsque l’élément logiciel représente des versions multilingues ou internationales d’un produit, la chaîne « multilingue » doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="67660-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="67660-159">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-159">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-160">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="67660-160">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-163">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,2»)</span><span class="sxs-lookup"><span data-stu-id="67660-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="67660-164">Fabricant du BIOS.</span><span class="sxs-lookup"><span data-stu-id="67660-164">The manufacturer of the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="67660-165">**Nom**</span><span class="sxs-lookup"><span data-stu-id="67660-165">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-168">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="67660-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67660-169">Nom utilisé pour identifier cet élément logiciel</span><span class="sxs-lookup"><span data-stu-id="67660-169">The name used to identify this software element</span></span>

<span data-ttu-id="67660-170">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-170">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-171">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="67660-171">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-174">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="67660-174">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="67660-175">Fabricant et type de système d’exploitation pour un élément logiciel lorsque la propriété **TargetOperatingSystem** a la valeur 1 (« autre »).</span><span class="sxs-lookup"><span data-stu-id="67660-175">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="67660-176">Lorsque la propriété **TargetOperatingSystem** a la valeur 1, cette propriété doit avoir une valeur non null.</span><span class="sxs-lookup"><span data-stu-id="67660-176">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="67660-177">Pour toutes les autres valeurs **TargetOperatingSystem** , cette propriété a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="67660-177">For all other **TargetOperatingSystem** values, this property is null.</span></span>

<span data-ttu-id="67660-178">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-178">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-179">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="67660-179">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="67660-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67660-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-182">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,9»)</span><span class="sxs-lookup"><span data-stu-id="67660-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="67660-183">Si la **valeur est true**, il s’agit du BIOS principal du système informatique.</span><span class="sxs-lookup"><span data-stu-id="67660-183">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="67660-184">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="67660-184">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-187">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="67660-187">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="67660-188">Numéro de série de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="67660-188">Serial number of the software element.</span></span>

<span data-ttu-id="67660-189">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-189">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-190">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="67660-190">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-193">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="67660-193">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67660-194">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="67660-194">Identifier for the software element.</span></span> <span data-ttu-id="67660-195">Il est conçu pour être utilisé conjointement avec d’autres clés pour créer une représentation unique de ce [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-195">It is designed to be used in conjunction with other keys to create a unique representation of this [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="67660-196">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-196">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67660-197">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="67660-197">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67660-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67660-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-200">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67660-200">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67660-201">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="67660-201">State of a software element.</span></span>

<span data-ttu-id="67660-202">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-202">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="67660-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="67660-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="67660-204">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="67660-204">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="67660-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="67660-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="67660-206">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="67660-206">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="67660-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="67660-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="67660-208">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="67660-208">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="67660-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="67660-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67660-210">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="67660-210">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67660-211">**État**</span><span class="sxs-lookup"><span data-stu-id="67660-211">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-214">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="67660-214">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="67660-215">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="67660-215">String that indicates the current status of the object.</span></span> <span data-ttu-id="67660-216">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="67660-216">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="67660-217">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="67660-217">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="67660-218">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="67660-218">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="67660-219">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="67660-219">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="67660-220">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="67660-220">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="67660-221">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="67660-221">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="67660-222">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="67660-223">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="67660-223">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="67660-224">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="67660-224">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="67660-225">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="67660-225">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="67660-226">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="67660-226">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67660-227">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="67660-227">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="67660-228">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="67660-228">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="67660-229">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="67660-229">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="67660-230">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="67660-230">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="67660-231">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="67660-231">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="67660-232">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="67660-232">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="67660-233">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="67660-233">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="67660-234">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="67660-234">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="67660-235">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="67660-235">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67660-236">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="67660-236">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-237">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67660-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67660-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-239">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur le composant logiciel DMTF \| 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="67660-239">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="67660-240">Environnement du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="67660-240">Operating system environment.</span></span> <span data-ttu-id="67660-241">La valeur de cette propriété ne garantit pas l’exécution binaire, plus d’informations sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="67660-241">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="67660-242">La version du système d’exploitation doit être spécifiée à l’aide de la vérification de la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="67660-242">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="67660-243">Également nécessaire, est l’architecture sur laquelle le système d’exploitation s’exécute.</span><span class="sxs-lookup"><span data-stu-id="67660-243">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="67660-244">La combinaison de ces constructions permet au fournisseur d’identifier clairement le niveau de système d’exploitation requis pour un élément logiciel particulier.</span><span class="sxs-lookup"><span data-stu-id="67660-244">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="67660-245">Cette propriété est héritée de la [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-245">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67660-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="67660-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67660-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="67660-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="67660-248"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="67660-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="67660-249">Mac OS</span><span class="sxs-lookup"><span data-stu-id="67660-249">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="67660-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="67660-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67660-251">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="67660-251">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="67660-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="67660-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="67660-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="67660-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="67660-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="67660-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="67660-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="67660-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="67660-256">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="67660-256">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="67660-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="67660-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="67660-258">HP-UX</span><span class="sxs-lookup"><span data-stu-id="67660-258">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="67660-259"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="67660-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="67660-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="67660-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="67660-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="67660-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="67660-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="67660-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="67660-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="67660-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="67660-264">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="67660-264">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="67660-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="67660-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="67660-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="67660-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="67660-267">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="67660-267">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="67660-268"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="67660-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="67660-269">Windows 95</span><span class="sxs-lookup"><span data-stu-id="67660-269">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="67660-270"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="67660-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="67660-271">Windows 98</span><span class="sxs-lookup"><span data-stu-id="67660-271">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="67660-272"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="67660-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="67660-273">Windows NT</span><span class="sxs-lookup"><span data-stu-id="67660-273">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="67660-274"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="67660-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="67660-275">Windows CE</span><span class="sxs-lookup"><span data-stu-id="67660-275">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="67660-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="67660-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="67660-277">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="67660-277">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="67660-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="67660-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="67660-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="67660-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="67660-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="67660-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="67660-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="67660-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="67660-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="67660-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="67660-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="67660-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="67660-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="67660-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="67660-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="67660-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="67660-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="67660-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="67660-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="67660-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="67660-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="67660-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="67660-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="67660-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="67660-290">Une série</span><span class="sxs-lookup"><span data-stu-id="67660-290">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="67660-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="67660-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="67660-292">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="67660-292">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="67660-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="67660-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="67660-294">NT tandem</span><span class="sxs-lookup"><span data-stu-id="67660-294">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="67660-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="67660-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="67660-296">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="67660-296">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="67660-297"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="67660-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="67660-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="67660-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="67660-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="67660-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="67660-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="67660-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="67660-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="67660-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="67660-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="67660-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="67660-303">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="67660-303">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="67660-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="67660-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="67660-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="67660-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="67660-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="67660-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="67660-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="67660-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="67660-308">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="67660-308">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="67660-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="67660-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="67660-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="67660-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="67660-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="67660-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="67660-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="67660-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="67660-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="67660-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="67660-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="67660-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="67660-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="67660-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="67660-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="67660-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="67660-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="67660-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="67660-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="67660-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="67660-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="67660-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="67660-320">Palm OS</span><span class="sxs-lookup"><span data-stu-id="67660-320">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="67660-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="67660-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="67660-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="67660-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="67660-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="67660-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="67660-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="67660-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="67660-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="67660-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67660-326">**Version**</span><span class="sxs-lookup"><span data-stu-id="67660-326">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67660-327">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67660-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67660-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67660-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67660-329">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="67660-329">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="67660-330">Version du BIOS.</span><span class="sxs-lookup"><span data-stu-id="67660-330">The version of the BIOS.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67660-331">Notes</span><span class="sxs-lookup"><span data-stu-id="67660-331">Remarks</span></span>

<span data-ttu-id="67660-332">La classe **CIM \_ BIOSElement** est dérivée de [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="67660-332">The **CIM\_BIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="67660-333">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="67660-333">WMI does not implement this class.</span></span> <span data-ttu-id="67660-334">Pour plus d’informations sur les classes dérivées de **CIM \_ BIOSElement**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="67660-334">For more information about classes derived from **CIM\_BIOSElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="67660-335">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="67660-335">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="67660-336">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="67660-336">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="67660-337">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67660-337">Requirements</span></span>



| <span data-ttu-id="67660-338">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67660-338">Requirement</span></span> | <span data-ttu-id="67660-339">Valeur</span><span class="sxs-lookup"><span data-stu-id="67660-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67660-340">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67660-340">Minimum supported client</span></span><br/> | <span data-ttu-id="67660-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67660-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67660-342">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67660-342">Minimum supported server</span></span><br/> | <span data-ttu-id="67660-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67660-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67660-344">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="67660-344">Namespace</span></span><br/>                | <span data-ttu-id="67660-345">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="67660-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67660-346">MOF</span><span class="sxs-lookup"><span data-stu-id="67660-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67660-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67660-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67660-348">DLL</span><span class="sxs-lookup"><span data-stu-id="67660-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67660-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67660-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67660-350">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67660-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67660-351">**\_SOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="67660-351">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

