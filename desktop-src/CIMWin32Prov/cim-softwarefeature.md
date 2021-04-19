---
description: La \_ classe CIM SoftwareFeature représente une fonction ou une fonctionnalité particulière d’un produit ou d’un système d’application.
ms.assetid: 7beeb32c-d285-44f7-adeb-3b661d8ab037
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeature
- CIM_SoftwareFeature.Caption
- CIM_SoftwareFeature.Description
- CIM_SoftwareFeature.IdentifyingNumber
- CIM_SoftwareFeature.InstallDate
- CIM_SoftwareFeature.Name
- CIM_SoftwareFeature.ProductName
- CIM_SoftwareFeature.Status
- CIM_SoftwareFeature.Vendor
- CIM_SoftwareFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3959f7b99170cf1470d3688a101e4858f70e9a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512877"
---
# <a name="cim_softwarefeature-class"></a><span data-ttu-id="32f56-103">\_Classe CIM SoftwareFeature</span><span class="sxs-lookup"><span data-stu-id="32f56-103">CIM\_SoftwareFeature class</span></span>

<span data-ttu-id="32f56-104">La classe **CIM \_ SoftwareFeature** représente une fonction ou une fonctionnalité particulière d’un produit ou d’un système d’application.</span><span class="sxs-lookup"><span data-stu-id="32f56-104">The **CIM\_SoftwareFeature** class represents a particular function or capability of a product or application system.</span></span> <span data-ttu-id="32f56-105">Cette classe reflète un niveau de granularité significatif pour l’utilisateur d’un produit plutôt que les unités qui reflètent la manière dont le produit est créé ou empaqueté (capturé à l’aide d’une classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) ).</span><span class="sxs-lookup"><span data-stu-id="32f56-105">This class reflects a level of granularity that is meaningful to a user of a product rather than the units that reflect how the product is built or packaged (captured using a [**CIM\_SoftwareElement**](cim-softwareelement.md) class).</span></span> <span data-ttu-id="32f56-106">Lorsqu’une fonctionnalité logicielle peut exister sur plusieurs plateformes ou systèmes d’exploitation, la fonctionnalité logicielle est un ensemble d’éléments logiciels pour les différentes plateformes.</span><span class="sxs-lookup"><span data-stu-id="32f56-106">When a software feature can exist on multiple platforms or operating systems, the software feature is a collection of the software elements for the different platforms.</span></span> <span data-ttu-id="32f56-107">Dans ce cas, les utilisateurs du modèle sont généralement intéressés par une sous-collection des éléments logiciels requis pour une plate-forme particulière.</span><span class="sxs-lookup"><span data-stu-id="32f56-107">In which case, the users of the model will be typically interested in a sub-collection of the software elements required for a particular platform.</span></span> <span data-ttu-id="32f56-108">Étant donné que les fonctionnalités sont fournies par le biais de produits, les fonctionnalités logicielles sont toujours définies dans le contexte d’une classe de [**\_ produit CIM**](cim-product.md) à l’aide de l’Association [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) .</span><span class="sxs-lookup"><span data-stu-id="32f56-108">Because features are delivered through products, software features are always defined in the context of a [**CIM\_Product**](cim-product.md) class using the [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association.</span></span> <span data-ttu-id="32f56-109">Éventuellement, les fonctionnalités logicielles d’un ou de plusieurs produits peuvent être organisées en systèmes d’applications à l’aide de l’Association [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="32f56-109">Optionally, software features from one or more products can be organized into application systems using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32f56-110">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="32f56-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="32f56-111">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="32f56-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="32f56-112">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="32f56-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="32f56-113">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="32f56-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f56-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32f56-114">Syntax</span></span>

``` syntax
[UUID("{E527D7F2-E3D4-11d2-8601-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_SoftwareFeature : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="32f56-115">Membres</span><span class="sxs-lookup"><span data-stu-id="32f56-115">Members</span></span>

<span data-ttu-id="32f56-116">La classe **CIM \_ SoftwareFeature** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="32f56-116">The **CIM\_SoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="32f56-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="32f56-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32f56-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="32f56-118">Properties</span></span>

<span data-ttu-id="32f56-119">La classe **CIM \_ SoftwareFeature** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="32f56-119">The **CIM\_SoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32f56-120">**Caption**</span><span class="sxs-lookup"><span data-stu-id="32f56-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-123">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="32f56-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-124">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32f56-124">Short textual description of the object.</span></span>

<span data-ttu-id="32f56-125">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32f56-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f56-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="32f56-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-129">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="32f56-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-130">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32f56-130">Textual description of the object.</span></span>

<span data-ttu-id="32f56-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32f56-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f56-132">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="32f56-132">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-135">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="32f56-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-136">Identification du produit, telle qu’un numéro de série sur un logiciel ou un numéro gravé sur une puce matérielle.</span><span class="sxs-lookup"><span data-stu-id="32f56-136">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="32f56-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="32f56-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-138">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="32f56-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="32f56-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-141">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32f56-141">Date and time the object was installed.</span></span> <span data-ttu-id="32f56-142">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="32f56-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="32f56-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32f56-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f56-144">**Nom**</span><span class="sxs-lookup"><span data-stu-id="32f56-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-147">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="32f56-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="32f56-148">Étiquette par laquelle l’objet est connu en dehors du système de traitement des données.</span><span class="sxs-lookup"><span data-stu-id="32f56-148">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="32f56-149">L’étiquette est un nom lisible par l’utilisateur qui identifie de façon unique l’élément dans le contexte de l’espace de noms de l’élément.</span><span class="sxs-lookup"><span data-stu-id="32f56-149">The label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="32f56-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32f56-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32f56-151">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="32f56-151">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-154">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="32f56-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-155">Nom de produit couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="32f56-155">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="32f56-156">**État**</span><span class="sxs-lookup"><span data-stu-id="32f56-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-159">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="32f56-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-160">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="32f56-160">Current status of the object.</span></span>

<span data-ttu-id="32f56-161">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="32f56-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="32f56-162">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32f56-162">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="32f56-163">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="32f56-163">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="32f56-164">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="32f56-164">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="32f56-165">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="32f56-165">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="32f56-166">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="32f56-166">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="32f56-167">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="32f56-167">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="32f56-168">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="32f56-168">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="32f56-169">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="32f56-169">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="32f56-170">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="32f56-170">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="32f56-171">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="32f56-171">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="32f56-172">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="32f56-172">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="32f56-173">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="32f56-173">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="32f56-174">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="32f56-174">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="32f56-175">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="32f56-175">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-178">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Vendor**»), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« DMTF \| ComponentID \| 001,1 »)</span><span class="sxs-lookup"><span data-stu-id="32f56-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-179">Nom du fournisseur du produit, qui correspond à la propriété **Vendor** dans l’objet Product de la norme d’échange de solution DMTF.</span><span class="sxs-lookup"><span data-stu-id="32f56-179">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> <dt>

<span data-ttu-id="32f56-180">**Version**</span><span class="sxs-lookup"><span data-stu-id="32f56-180">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f56-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="32f56-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f56-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="32f56-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f56-183">Qualificateurs : [**propagate**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ produit CIM**](cim-product.md).**Version**"), [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="32f56-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="32f56-184">Les informations de version du produit, qui correspondent à la propriété **version** dans l’objet Product de la norme d’échange de solutions DMTF.</span><span class="sxs-lookup"><span data-stu-id="32f56-184">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32f56-185">Notes</span><span class="sxs-lookup"><span data-stu-id="32f56-185">Remarks</span></span>

<span data-ttu-id="32f56-186">La classe **CIM \_ SoftwareFeature** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="32f56-186">The **CIM\_SoftwareFeature** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="32f56-187">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="32f56-187">WMI does not implement this class.</span></span> <span data-ttu-id="32f56-188">Pour les classes WMI dérivées de **CIM \_ SoftwareFeature**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="32f56-188">For WMI classes derived from **CIM\_SoftwareFeature**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="32f56-189">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="32f56-189">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="32f56-190">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="32f56-190">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="32f56-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32f56-191">Requirements</span></span>



| <span data-ttu-id="32f56-192">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32f56-192">Requirement</span></span> | <span data-ttu-id="32f56-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="32f56-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32f56-194">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32f56-194">Minimum supported client</span></span><br/> | <span data-ttu-id="32f56-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32f56-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32f56-196">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32f56-196">Minimum supported server</span></span><br/> | <span data-ttu-id="32f56-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32f56-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32f56-198">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="32f56-198">Namespace</span></span><br/>                | <span data-ttu-id="32f56-199">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="32f56-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32f56-200">MOF</span><span class="sxs-lookup"><span data-stu-id="32f56-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32f56-201"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32f56-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32f56-202">DLL</span><span class="sxs-lookup"><span data-stu-id="32f56-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f56-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f56-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f56-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32f56-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f56-205">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="32f56-205">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

