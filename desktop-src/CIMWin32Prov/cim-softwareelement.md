---
description: La \_ classe CIM SoftwareElement décompose un \_ objet SoftwareFeature CIM en un ensemble de parties gérables ou déployables individuellement pour une plateforme particulière.
ms.assetid: b2418735-b738-411a-a620-acc31662f824
ms.tgt_platform: multiple
title: CIM_SoftwareElement, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.Caption
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.Description
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.InstallDate
- CIM_SoftwareElement.LanguageEdition
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.Status
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fbe64ddfcf81a7410f5654db89c2924a8eabacc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110815"
---
# <a name="cim_softwareelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="d8ad4-103">CIM_SoftwareElement, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-103">CIM_SoftwareElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d8ad4-104">La classe **CIM \_ SoftwareElement** décompose un [**objet \_ SoftwareFeature CIM**](cim-softwarefeature.md) en un ensemble de parties gérables ou déployables individuellement pour une plateforme particulière.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-104">The **CIM\_SoftwareElement** class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="d8ad4-105">La plateforme d’un élément logiciel est identifiée de manière unique par son architecture matérielle sous-jacente et son système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-105">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

<span data-ttu-id="d8ad4-106">Par conséquent, pour comprendre les détails de la façon dont les fonctionnalités d’une fonctionnalité logicielle particulière sont fournies sur une plateforme particulière, les objets **CIM \_ SoftwareElement** référencés par les associations [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) sont organisés dans des ensembles disjoints basés sur la propriété **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="d8ad4-106">As such, to understand the details of how the functionality of a particular software feature is provided on a particular platform, the **CIM\_SoftwareElement** objects referenced by [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) associations are organized in disjoint sets based on the **TargetOperatingSystem** property.</span></span> <span data-ttu-id="d8ad4-107">Un objet **CIM \_ SoftwareElement** capture les détails de gestion d’une partie ou d’un composant dans l’un des quatre États caractérisés par la propriété **SoftwareElementState** .</span><span class="sxs-lookup"><span data-stu-id="d8ad4-107">A **CIM\_SoftwareElement** object captures the management details of a part or component in one of four states characterized by the **SoftwareElementState** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8ad4-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d8ad4-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d8ad4-110">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d8ad4-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ad4-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8ad4-112">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C561-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  string   LanguageEdition;
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="d8ad4-113">Membres</span><span class="sxs-lookup"><span data-stu-id="d8ad4-113">Members</span></span>

<span data-ttu-id="d8ad4-114">La classe **CIM \_ SoftwareElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8ad4-114">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="d8ad4-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8ad4-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8ad4-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8ad4-116">Properties</span></span>

<span data-ttu-id="d8ad4-117">La classe **CIM \_ SoftwareElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-117">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8ad4-118">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-118">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur les composants logiciels DMTF \| 002,4»)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-121">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-122">Identificateur interne pour la compilation de cet élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-122">Internal identifier for the compilation of this software element.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-126">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-127">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-127">Short textual description of the object.</span></span>

<span data-ttu-id="d8ad4-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-129">**Codes**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-129">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-132">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-133">Ensemble de codes utilisé par l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-133">Code set used by the software element.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-137">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-138">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-138">Textual description of the object.</span></span>

<span data-ttu-id="d8ad4-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-140">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-140">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-143">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur les composants logiciels DMTF \| 002,7»)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-143">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-144">Identificateur du fabricant de l’élément logiciel, souvent une unité de conservation ou un numéro de référence.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-144">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-146">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-149">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-149">Date and time the object was installed.</span></span> <span data-ttu-id="d8ad4-150">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-150">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d8ad4-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-155">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur les composants logiciels DMTF \| 002,6»)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-156">Édition de langue de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-156">Language edition of the software element.</span></span> <span data-ttu-id="d8ad4-157">Les codes de langue définis dans ISO 639 doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="d8ad4-158">Lorsque l’élément logiciel représente des versions multilingues ou internationales d’un produit, la chaîne « multilingue » doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-159">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-159">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-162">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-162">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-163">Fabricant de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-163">Manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-164">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-167">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-168">Nom utilisé pour identifier l’élément logiciel cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-168">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-169">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-169">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-172">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-173">Fabricant et type de système d’exploitation pour un élément logiciel lorsque la propriété **TargetOperatingSystem** a la valeur 1 (« autre »).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-173">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="d8ad4-174">Lorsque la propriété **TargetOperatingSystem** a la valeur 1, cette propriété doit avoir une valeur non null.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-174">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="d8ad4-175">Pour toutes les autres valeurs **TargetOperatingSystem** , cette propriété a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-175">For all other **TargetOperatingSystem** values, this property is null.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-176">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-176">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-179">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-179">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-180">Numéro de série de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-180">Serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-181">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-181">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-184">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-184">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-185">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-185">Identifier for the software element.</span></span> <span data-ttu-id="d8ad4-186">Il est conçu pour être utilisé conjointement avec d’autres clés pour créer une représentation unique de ce **\_ SoftwareElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-186">It is designed to be used in conjunction with other keys to create a unique representation of this **CIM\_SoftwareElement**.</span></span>

</dd> <dt>

<span data-ttu-id="d8ad4-187">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-187">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-188">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-190">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-190">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-191">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-191">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="d8ad4-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-193">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="d8ad4-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-195">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="d8ad4-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-197">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="d8ad4-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-199">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d8ad4-200">**État**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-200">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-203">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-204">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-204">Current status of the object.</span></span>

<span data-ttu-id="d8ad4-205">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d8ad4-206">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8ad4-206">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d8ad4-207">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-207">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d8ad4-208">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-208">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d8ad4-209">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-209">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8ad4-210">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-210">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d8ad4-211">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-211">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d8ad4-212">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-212">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d8ad4-213">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-213">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d8ad4-214">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-214">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d8ad4-215">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-215">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d8ad4-216">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-216">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d8ad4-217">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-217">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d8ad4-218">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-218">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8ad4-219">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-219">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-220">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-222">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations sur le composant logiciel DMTF \| 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-222">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-223">Environnement du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-223">Operating system environment.</span></span> <span data-ttu-id="d8ad4-224">La valeur de cette propriété ne garantit pas l’exécution binaire, plus d’informations sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-224">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="d8ad4-225">La version du système d’exploitation doit être spécifiée à l’aide de la vérification de la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-225">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="d8ad4-226">Également nécessaire, est l’architecture sur laquelle le système d’exploitation s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-226">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="d8ad4-227">La combinaison de ces constructions permet au fournisseur d’identifier clairement le niveau de système d’exploitation requis pour un élément logiciel particulier.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-227">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8ad4-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d8ad4-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="d8ad4-230"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-231">Mac OS</span><span class="sxs-lookup"><span data-stu-id="d8ad4-231">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="d8ad4-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-233">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="d8ad4-233">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="d8ad4-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="d8ad4-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="d8ad4-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="d8ad4-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-238">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="d8ad4-238">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="d8ad4-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-240">HP-UX</span><span class="sxs-lookup"><span data-stu-id="d8ad4-240">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="d8ad4-241"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="d8ad4-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="d8ad4-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="d8ad4-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="d8ad4-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-246">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="d8ad4-246">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="d8ad4-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="d8ad4-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-249">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="d8ad4-249">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="d8ad4-250"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-251">Windows 95</span><span class="sxs-lookup"><span data-stu-id="d8ad4-251">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="d8ad4-252"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-253">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d8ad4-253">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="d8ad4-254"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-255">Windows NT</span><span class="sxs-lookup"><span data-stu-id="d8ad4-255">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="d8ad4-256"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-257">Windows CE</span><span class="sxs-lookup"><span data-stu-id="d8ad4-257">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="d8ad4-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-259">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="d8ad4-259">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="d8ad4-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="d8ad4-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="d8ad4-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="d8ad4-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="d8ad4-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="d8ad4-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="d8ad4-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="d8ad4-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="d8ad4-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="d8ad4-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="d8ad4-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="d8ad4-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-272">Une série</span><span class="sxs-lookup"><span data-stu-id="d8ad4-272">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="d8ad4-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-274">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="d8ad4-274">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="d8ad4-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-276">NT tandem</span><span class="sxs-lookup"><span data-stu-id="d8ad4-276">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="d8ad4-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-278">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="d8ad4-278">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="d8ad4-279"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="d8ad4-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="d8ad4-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="d8ad4-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="d8ad4-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="d8ad4-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-285">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="d8ad4-285">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="d8ad4-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="d8ad4-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="d8ad4-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="d8ad4-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-290">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="d8ad4-290">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="d8ad4-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="d8ad4-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="d8ad4-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="d8ad4-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="d8ad4-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="d8ad4-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="d8ad4-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="d8ad4-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="d8ad4-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="d8ad4-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="d8ad4-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="d8ad4-302">Palm OS</span><span class="sxs-lookup"><span data-stu-id="d8ad4-302">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="d8ad4-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="d8ad4-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="d8ad4-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="d8ad4-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="d8ad4-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="d8ad4-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8ad4-308">**Version**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-308">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8ad4-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8ad4-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8ad4-311">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="d8ad4-311">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="d8ad4-312">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-312">Version of the operation.</span></span>

<span data-ttu-id="d8ad4-313">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8ad4-313">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="d8ad4-314"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="d8ad4-314"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="d8ad4-315"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="d8ad4-315"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8ad4-316">Notes</span><span class="sxs-lookup"><span data-stu-id="d8ad4-316">Remarks</span></span>

<span data-ttu-id="d8ad4-317">La classe **CIM \_ SoftwareElement** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-317">The **CIM\_SoftwareElement** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="d8ad4-318">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-318">WMI does not implement this class.</span></span> <span data-ttu-id="d8ad4-319">Pour les classes WMI dérivées de **CIM \_ SoftwareElement**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d8ad4-319">For WMI classes derived from **CIM\_SoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d8ad4-320">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-320">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d8ad4-321">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d8ad4-321">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ad4-322">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8ad4-322">Requirements</span></span>



| <span data-ttu-id="d8ad4-323">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8ad4-323">Requirement</span></span> | <span data-ttu-id="d8ad4-324">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8ad4-324">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ad4-325">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8ad4-325">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ad4-326">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8ad4-326">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8ad4-327">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8ad4-327">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ad4-328">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8ad4-328">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8ad4-329">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8ad4-329">Namespace</span></span><br/>                | <span data-ttu-id="d8ad4-330">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d8ad4-330">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8ad4-331">MOF</span><span class="sxs-lookup"><span data-stu-id="d8ad4-331">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8ad4-332"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad4-332"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8ad4-333">DLL</span><span class="sxs-lookup"><span data-stu-id="d8ad4-333">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8ad4-334"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad4-334"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ad4-335">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8ad4-335">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ad4-336">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d8ad4-336">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

