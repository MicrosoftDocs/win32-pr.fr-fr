---
description: La \_ classe CIM SoftwareElementVersionCheck représente un type d’élément logiciel qui doit exister dans l’environnement.
ms.assetid: a1c0f0d5-2586-499c-bd82-bbb107570d81
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck
- CIM_SoftwareElementVersionCheck.Caption
- CIM_SoftwareElementVersionCheck.CheckID
- CIM_SoftwareElementVersionCheck.CheckMode
- CIM_SoftwareElementVersionCheck.Description
- CIM_SoftwareElementVersionCheck.LowerSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Name
- CIM_SoftwareElementVersionCheck.SoftwareElementID
- CIM_SoftwareElementVersionCheck.SoftwareElementName
- CIM_SoftwareElementVersionCheck.SoftwareElementState
- CIM_SoftwareElementVersionCheck.SoftwareElementStateDesired
- CIM_SoftwareElementVersionCheck.TargetOperatingSystem
- CIM_SoftwareElementVersionCheck.TargetOperatingSystemDesired
- CIM_SoftwareElementVersionCheck.UpperSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb55a44a3aba9092567cdc91b668ba1b63e33174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200873"
---
# <a name="cim_softwareelementversioncheck-class"></a><span data-ttu-id="d6291-103">\_Classe CIM SoftwareElementVersionCheck</span><span class="sxs-lookup"><span data-stu-id="d6291-103">CIM\_SoftwareElementVersionCheck class</span></span>

<span data-ttu-id="d6291-104">La classe **CIM \_ SoftwareElementVersionCheck** représente un type d’élément logiciel qui doit exister dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="d6291-104">The **CIM\_SoftwareElementVersionCheck** class represents a type of software element that must exist in the environment.</span></span> <span data-ttu-id="d6291-105">Cette vérification peut être pour une plage de versions spécifique, minimale, maximale ou.</span><span class="sxs-lookup"><span data-stu-id="d6291-105">This check can be for a specific, minimum, maximum, or a range of versions.</span></span> <span data-ttu-id="d6291-106">Pour spécifier une version spécifique, les versions inférieure et supérieure doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="d6291-106">To specify a specific version, the lower and upper versions must be the same.</span></span> <span data-ttu-id="d6291-107">Pour spécifier une version minimale, spécifiez uniquement la version inférieure.</span><span class="sxs-lookup"><span data-stu-id="d6291-107">To specify a minimum version, specify only the lower version.</span></span> <span data-ttu-id="d6291-108">Pour spécifier une version maximale, spécifiez uniquement la version supérieure.</span><span class="sxs-lookup"><span data-stu-id="d6291-108">To specify a maximum version, specify only the upper version.</span></span> <span data-ttu-id="d6291-109">Pour spécifier une plage, les versions supérieure et inférieure doivent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d6291-109">To specify a range, both upper and lower versions must be specified.</span></span> <span data-ttu-id="d6291-110">Les détails des vérifications sont comparés aux détails correspondants trouvés dans un objet [**CIM \_ SoftwareElement**](cim-softwareelement.md) référencé par une association [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) pour l’objet [**\_ ComputerSystem CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="d6291-110">Details of the checks are compared with the corresponding details found in a [**CIM\_SoftwareElement**](cim-softwareelement.md) object referenced by a [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object.</span></span> <span data-ttu-id="d6291-111">Au moins un **\_ SoftwareElement CIM** doit satisfaire les détails de la condition pour que la vérification soit satisfaite.</span><span class="sxs-lookup"><span data-stu-id="d6291-111">At least one **CIM\_SoftwareElement** needs to satisfy the details of the condition for the check to be satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6291-112">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d6291-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d6291-113">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d6291-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d6291-114">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d6291-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d6291-115">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d6291-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6291-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6291-116">Syntax</span></span>

``` syntax
[UUID("{4D23FBD0-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareElementVersionCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  string  Description;
  string  LowerSoftwareElementVersion;
  string  Name;
  string  SoftwareElementID;
  string  SoftwareElementName;
  uint16  SoftwareElementState;
  uint16  SoftwareElementStateDesired;
  uint16  TargetOperatingSystem;
  uint16  TargetOperatingSystemDesired;
  string  UpperSoftwareElementVersion;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="d6291-117">Membres</span><span class="sxs-lookup"><span data-stu-id="d6291-117">Members</span></span>

<span data-ttu-id="d6291-118">La classe **CIM \_ SoftwareElementVersionCheck** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6291-118">The **CIM\_SoftwareElementVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="d6291-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6291-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="d6291-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6291-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d6291-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d6291-121">Methods</span></span>

<span data-ttu-id="d6291-122">La classe **CIM \_ SoftwareElementVersionCheck** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d6291-122">The **CIM\_SoftwareElementVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="d6291-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="d6291-123">Method</span></span>                                                                   | <span data-ttu-id="d6291-124">Description</span><span class="sxs-lookup"><span data-stu-id="d6291-124">Description</span></span>                                                   |
|:-------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="d6291-125">**Appeler**</span><span class="sxs-lookup"><span data-stu-id="d6291-125">**Invoke**</span></span>](invoke-method-in-class-cim-softwareelementversioncheck.md) | <span data-ttu-id="d6291-126">Effectue une action particulière.</span><span class="sxs-lookup"><span data-stu-id="d6291-126">Takes a particular action.</span></span> <span data-ttu-id="d6291-127">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="d6291-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d6291-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6291-128">Properties</span></span>

<span data-ttu-id="d6291-129">La classe **CIM \_ SoftwareElementVersionCheck** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6291-129">The **CIM\_SoftwareElementVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6291-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d6291-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-133">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d6291-133">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d6291-134">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d6291-134">Short textual description of the object.</span></span>

<span data-ttu-id="d6291-135">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-135">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6291-136">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="d6291-136">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-139">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d6291-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d6291-140">Identificateur utilisé conjointement avec d’autres clés pour identifier de manière unique la vérification.</span><span class="sxs-lookup"><span data-stu-id="d6291-140">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="d6291-141">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-141">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6291-142">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="d6291-142">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d6291-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6291-145">Si la **valeur est true**, la condition est supposée exister dans l’environnement (par exemple, si un fichier se trouve sur un système, la méthode [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) doit retourner la **valeur true**).</span><span class="sxs-lookup"><span data-stu-id="d6291-145">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="d6291-146">Si la **valeur est false**, la condition ne doit pas exister (par exemple, si un fichier n’est pas sur un système, la méthode **Invoke** doit retourner **false**).</span><span class="sxs-lookup"><span data-stu-id="d6291-146">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="d6291-147">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-147">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6291-148">**Description**</span><span class="sxs-lookup"><span data-stu-id="d6291-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d6291-151">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d6291-151">Description of the object.</span></span>

<span data-ttu-id="d6291-152">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6291-153">**LowerSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="d6291-153">**LowerSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-156">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="d6291-156">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="d6291-157">Version minimale des éléments logiciels en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="d6291-157">Minimum version of a software elements being checked.</span></span>

</dd> <dt>

<span data-ttu-id="d6291-158">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d6291-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-161">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d6291-161">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d6291-162">Nom utilisé pour identifier l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d6291-162">Name used to identify the software element.</span></span>

<span data-ttu-id="d6291-163">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-163">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6291-164">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="d6291-164">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-167">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d6291-167">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d6291-168">Identificateur de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d6291-168">Identifier for the software element.</span></span>

<span data-ttu-id="d6291-169">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-169">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6291-170">**SoftwareElementName**</span><span class="sxs-lookup"><span data-stu-id="d6291-170">**SoftwareElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-173">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="d6291-173">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="d6291-174">Nom de l’élément logiciel en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="d6291-174">Name of the software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="d6291-175">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="d6291-175">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-176">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6291-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-178">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d6291-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d6291-179">État d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d6291-179">State of a software element.</span></span>

<span data-ttu-id="d6291-180">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-180">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="d6291-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="d6291-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-182">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d6291-182">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="d6291-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="d6291-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-184">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d6291-184">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="d6291-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="d6291-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-186">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d6291-186">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="d6291-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="d6291-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-188">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="d6291-188">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d6291-189">**SoftwareElementStateDesired**</span><span class="sxs-lookup"><span data-stu-id="d6291-189">**SoftwareElementStateDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6291-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-192">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**")</span><span class="sxs-lookup"><span data-stu-id="d6291-192">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**")</span></span>
</dt> </dl>

<span data-ttu-id="d6291-193">État de l’élément logiciel en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="d6291-193">State of the software element being checked.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="d6291-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Déployable** (0)</span><span class="sxs-lookup"><span data-stu-id="d6291-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-195">Décrit les détails nécessaires à la réussite de la distribution et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État installable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d6291-195">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="d6291-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installation** (1)</span><span class="sxs-lookup"><span data-stu-id="d6291-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-197">Décrit les détails nécessaires à l’installation réussie et les détails (conditions et actions) nécessaires à la création d’un élément logiciel dans l’État exécutable (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d6291-197">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="d6291-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Exécutable** (2)</span><span class="sxs-lookup"><span data-stu-id="d6291-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-199">Décrit les détails nécessaires pour une exécution réussie et les détails (conditions et actions) requis pour créer un élément logiciel dans l’État en cours d’exécution (autrement dit, l’état suivant).</span><span class="sxs-lookup"><span data-stu-id="d6291-199">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="d6291-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En cours d’exécution** (3)</span><span class="sxs-lookup"><span data-stu-id="d6291-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-201">Décrit les détails nécessaires à l’analyse et à l’utilisation d’un élément de début.</span><span class="sxs-lookup"><span data-stu-id="d6291-201">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d6291-202">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="d6291-202">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-203">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6291-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-205">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informations sur les composants logiciels DMTF \| 002,5»)</span><span class="sxs-lookup"><span data-stu-id="d6291-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="d6291-206">Système d’exploitation cible de l’élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="d6291-206">Target operating system of the software element.</span></span>

<span data-ttu-id="d6291-207">Cette propriété est héritée de la [**\_ vérification CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="d6291-207">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6291-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d6291-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d6291-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d6291-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="d6291-210"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="d6291-210"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-211">Mac OS</span><span class="sxs-lookup"><span data-stu-id="d6291-211">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="d6291-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="d6291-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-213">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="d6291-213">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="d6291-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="d6291-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="d6291-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="d6291-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="d6291-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="d6291-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="d6291-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="d6291-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-218">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="d6291-218">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="d6291-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="d6291-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-220">HP-UX</span><span class="sxs-lookup"><span data-stu-id="d6291-220">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="d6291-221"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="d6291-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="d6291-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="d6291-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="d6291-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="d6291-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="d6291-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="d6291-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="d6291-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="d6291-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-226">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="d6291-226">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="d6291-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="d6291-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="d6291-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="d6291-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-229">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="d6291-229">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="d6291-230"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="d6291-230"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-231">Windows 95</span><span class="sxs-lookup"><span data-stu-id="d6291-231">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="d6291-232"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="d6291-232"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-233">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d6291-233">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="d6291-234"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="d6291-234"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-235">Windows NT</span><span class="sxs-lookup"><span data-stu-id="d6291-235">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="d6291-236"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="d6291-236"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-237">Windows CE</span><span class="sxs-lookup"><span data-stu-id="d6291-237">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="d6291-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="d6291-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-239">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="d6291-239">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="d6291-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="d6291-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="d6291-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="d6291-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="d6291-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="d6291-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="d6291-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="d6291-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="d6291-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="d6291-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="d6291-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="d6291-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="d6291-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="d6291-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="d6291-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="d6291-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="d6291-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="d6291-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="d6291-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="d6291-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="d6291-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="d6291-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="d6291-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="d6291-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-252">Une série</span><span class="sxs-lookup"><span data-stu-id="d6291-252">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="d6291-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="d6291-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-254">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="d6291-254">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="d6291-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="d6291-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-256">NT tandem</span><span class="sxs-lookup"><span data-stu-id="d6291-256">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="d6291-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="d6291-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-258">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="d6291-258">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="d6291-259"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="d6291-259"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="d6291-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="d6291-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="d6291-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="d6291-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="d6291-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="d6291-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="d6291-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="d6291-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="d6291-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="d6291-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-265">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="d6291-265">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="d6291-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="d6291-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="d6291-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="d6291-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="d6291-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="d6291-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="d6291-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="d6291-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-270">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="d6291-270">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="d6291-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="d6291-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="d6291-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="d6291-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="d6291-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="d6291-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="d6291-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="d6291-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="d6291-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="d6291-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="d6291-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="d6291-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="d6291-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="d6291-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="d6291-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="d6291-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="d6291-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="d6291-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="d6291-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="d6291-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="d6291-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="d6291-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-282">Palm OS</span><span class="sxs-lookup"><span data-stu-id="d6291-282">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="d6291-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="d6291-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="d6291-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="d6291-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="d6291-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="d6291-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="d6291-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="d6291-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="d6291-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="d6291-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d6291-288">**TargetOperatingSystemDesired**</span><span class="sxs-lookup"><span data-stu-id="d6291-288">**TargetOperatingSystemDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-289">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6291-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-291">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**")</span><span class="sxs-lookup"><span data-stu-id="d6291-291">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**")</span></span>
</dt> </dl>

<span data-ttu-id="d6291-292">Système d’exploitation cible de l’élément logiciel en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="d6291-292">Target operating system of the software element being checked.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d6291-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d6291-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d6291-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d6291-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="d6291-295"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="d6291-295"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-296">Mac OS</span><span class="sxs-lookup"><span data-stu-id="d6291-296">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="d6291-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="d6291-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-298">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="d6291-298">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="d6291-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="d6291-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="d6291-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="d6291-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="d6291-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="d6291-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="d6291-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="d6291-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-303">Ouvrir des machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="d6291-303">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="d6291-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="d6291-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-305">HP-UX</span><span class="sxs-lookup"><span data-stu-id="d6291-305">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="d6291-306"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="d6291-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="d6291-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="d6291-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="d6291-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="d6291-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="d6291-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="d6291-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="d6291-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="d6291-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-311">Machine virtuelle Microsoft pour Java</span><span class="sxs-lookup"><span data-stu-id="d6291-311">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="d6291-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="d6291-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="d6291-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="d6291-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-314">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="d6291-314">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="d6291-315"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="d6291-315"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-316">Windows 95</span><span class="sxs-lookup"><span data-stu-id="d6291-316">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="d6291-317"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="d6291-317"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-318">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d6291-318">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="d6291-319"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="d6291-319"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-320">Windows NT</span><span class="sxs-lookup"><span data-stu-id="d6291-320">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="d6291-321"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="d6291-321"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-322">Windows CE</span><span class="sxs-lookup"><span data-stu-id="d6291-322">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="d6291-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="d6291-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-324">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="d6291-324">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="d6291-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="d6291-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="d6291-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="d6291-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="d6291-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="d6291-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="d6291-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="d6291-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="d6291-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="d6291-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="d6291-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="d6291-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="d6291-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="d6291-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="d6291-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="d6291-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="d6291-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="d6291-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="d6291-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="d6291-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="d6291-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="d6291-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="d6291-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="d6291-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-337">Une série</span><span class="sxs-lookup"><span data-stu-id="d6291-337">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="d6291-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="d6291-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-339">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="d6291-339">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="d6291-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="d6291-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-341">NT tandem</span><span class="sxs-lookup"><span data-stu-id="d6291-341">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="d6291-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="d6291-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-343">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="d6291-343">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="d6291-344"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="d6291-344"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="d6291-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="d6291-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="d6291-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="d6291-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="d6291-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="d6291-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="d6291-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="d6291-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="d6291-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="d6291-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-350">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="d6291-350">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="d6291-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="d6291-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="d6291-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="d6291-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="d6291-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="d6291-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="d6291-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="d6291-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-355">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="d6291-355">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="d6291-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="d6291-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="d6291-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="d6291-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="d6291-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="d6291-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="d6291-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="d6291-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="d6291-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="d6291-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="d6291-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="d6291-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="d6291-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="d6291-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="d6291-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="d6291-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="d6291-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="d6291-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="d6291-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="d6291-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="d6291-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="d6291-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="d6291-367">Palm OS</span><span class="sxs-lookup"><span data-stu-id="d6291-367">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="d6291-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="d6291-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="d6291-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="d6291-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="d6291-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="d6291-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="d6291-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="d6291-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="d6291-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="d6291-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d6291-373">**UpperSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="d6291-373">**UpperSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-376">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="d6291-376">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="d6291-377">Version maximale d’un élément logiciel en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="d6291-377">Maximum version of a software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="d6291-378">**Version**</span><span class="sxs-lookup"><span data-stu-id="d6291-378">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6291-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d6291-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6291-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d6291-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6291-381">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="d6291-381">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="d6291-382">Version de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d6291-382">Version of the operation.</span></span>

<span data-ttu-id="d6291-383">La version de l’opération doit se présenter sous l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6291-383">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="d6291-384"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="d6291-384"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="d6291-385"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="d6291-385"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="d6291-386">Cette propriété est héritée de la classe de [**\_ vérification CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="d6291-386">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6291-387">Notes</span><span class="sxs-lookup"><span data-stu-id="d6291-387">Remarks</span></span>

<span data-ttu-id="d6291-388">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d6291-388">WMI does not implement this class.</span></span>

<span data-ttu-id="d6291-389">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d6291-389">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d6291-390">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d6291-390">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6291-391">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6291-391">Requirements</span></span>



| <span data-ttu-id="d6291-392">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6291-392">Requirement</span></span> | <span data-ttu-id="d6291-393">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6291-393">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6291-394">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6291-394">Minimum supported client</span></span><br/> | <span data-ttu-id="d6291-395">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6291-395">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6291-396">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6291-396">Minimum supported server</span></span><br/> | <span data-ttu-id="d6291-397">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6291-397">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6291-398">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d6291-398">Namespace</span></span><br/>                | <span data-ttu-id="d6291-399">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d6291-399">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6291-400">MOF</span><span class="sxs-lookup"><span data-stu-id="d6291-400">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6291-401"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6291-401"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6291-402">DLL</span><span class="sxs-lookup"><span data-stu-id="d6291-402">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6291-403"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6291-403"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6291-404">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6291-404">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6291-405">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="d6291-405">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

