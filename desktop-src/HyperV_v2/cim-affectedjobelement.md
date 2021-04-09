---
description: Représente une association entre un travail et les \_ objets propriété MANAGEDELEMENT CIM qui peuvent être affectés par son exécution.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: Classe CIM_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115099"
---
# <a name="cim_affectedjobelement-class"></a><span data-ttu-id="e09a2-103">\_Classe CIM AffectedJobElement</span><span class="sxs-lookup"><span data-stu-id="e09a2-103">CIM\_AffectedJobElement class</span></span>

<span data-ttu-id="e09a2-104">Représente une association entre un travail et les **objets \_ propriété ManagedElement CIM** qui peuvent être affectés par son exécution.</span><span class="sxs-lookup"><span data-stu-id="e09a2-104">Represents an association between a job and the **CIM\_ManagedElement** objects that may be affected by its execution.</span></span> <span data-ttu-id="e09a2-105">Il n’est pas possible que le travail décrive tous les éléments affectés.</span><span class="sxs-lookup"><span data-stu-id="e09a2-105">It may not be feasible for the job to describe all of the affected elements.</span></span> <span data-ttu-id="e09a2-106">L’objectif principal de cette association est de fournir des informations lorsqu’un travail requiert l’utilisation exclusive des éléments gérés affectés ou en décrivant les effets secondaires qui peuvent en résulter.</span><span class="sxs-lookup"><span data-stu-id="e09a2-106">The main purpose of this association is to provide information when a job requires exclusive use of the affected managed elements or when describing the side effects that may result.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09a2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e09a2-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="e09a2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e09a2-108">Members</span></span>

<span data-ttu-id="e09a2-109">La classe **CIM \_ AffectedJobElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e09a2-109">The **CIM\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="e09a2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e09a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e09a2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e09a2-111">Properties</span></span>

<span data-ttu-id="e09a2-112">La classe **CIM \_ AffectedJobElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e09a2-112">The **CIM\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e09a2-113">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="e09a2-113">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e09a2-114">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="e09a2-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e09a2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-116">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e09a2-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e09a2-117">Élément managé affecté par l’exécution du travail.</span><span class="sxs-lookup"><span data-stu-id="e09a2-117">The managed element affected by the execution of the job.</span></span>

</dd> <dt>

<span data-ttu-id="e09a2-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="e09a2-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e09a2-119">Type de données **: \_ travail CIM**</span><span class="sxs-lookup"><span data-stu-id="e09a2-119">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e09a2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-121">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e09a2-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e09a2-122">Travail qui affecte l’élément géré.</span><span class="sxs-lookup"><span data-stu-id="e09a2-122">The job that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="e09a2-123">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="e09a2-123">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e09a2-124">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e09a2-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e09a2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-126">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="e09a2-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="e09a2-127">Effet du travail sur l’élément géré.</span><span class="sxs-lookup"><span data-stu-id="e09a2-127">The effect the job has on the managed element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e09a2-128">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="e09a2-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e09a2-129">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="e09a2-129">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="e09a2-130">**Utilisation exclusive** (2)</span><span class="sxs-lookup"><span data-stu-id="e09a2-130">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="e09a2-131">**Impact sur les performances** (3)</span><span class="sxs-lookup"><span data-stu-id="e09a2-131">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="e09a2-132">**Intégrité de l’élément** (4)</span><span class="sxs-lookup"><span data-stu-id="e09a2-132">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="e09a2-133">**Créer** (5)</span><span class="sxs-lookup"><span data-stu-id="e09a2-133">**Create** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e09a2-134">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e09a2-134">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e09a2-135">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="e09a2-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e09a2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e09a2-137">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="e09a2-137">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="e09a2-138">Détails supplémentaires pour les valeurs « 1 » (autres) correspondantes dans le tableau **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="e09a2-138">Additional details for corresponding "1" (Other) values in the **ElementEffects** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e09a2-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e09a2-139">Requirements</span></span>



| <span data-ttu-id="e09a2-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e09a2-140">Requirement</span></span> | <span data-ttu-id="e09a2-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="e09a2-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09a2-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e09a2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e09a2-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e09a2-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e09a2-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e09a2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e09a2-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e09a2-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e09a2-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e09a2-146">Namespace</span></span><br/>                | <span data-ttu-id="e09a2-147">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e09a2-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e09a2-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e09a2-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e09a2-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e09a2-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e09a2-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e09a2-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e09a2-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e09a2-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

