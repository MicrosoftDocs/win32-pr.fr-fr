---
description: Représente une association entre un service et un élément managé qui peut être affecté par son exécution.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Classe CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514452"
---
# <a name="cim_serviceaffectselement-class"></a><span data-ttu-id="90f33-103">\_Classe CIM ServiceAffectsElement</span><span class="sxs-lookup"><span data-stu-id="90f33-103">CIM\_ServiceAffectsElement class</span></span>

<span data-ttu-id="90f33-104">Représente une association entre un service et un élément managé qui peut être affecté par son exécution.</span><span class="sxs-lookup"><span data-stu-id="90f33-104">Represents an association between a service and a managed element that might be affected by its execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="90f33-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90f33-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="90f33-106">Membres</span><span class="sxs-lookup"><span data-stu-id="90f33-106">Members</span></span>

<span data-ttu-id="90f33-107">La classe **CIM \_ ServiceAffectsElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="90f33-107">The **CIM\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="90f33-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90f33-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90f33-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90f33-109">Properties</span></span>

<span data-ttu-id="90f33-110">La classe **CIM \_ ServiceAffectsElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="90f33-110">The **CIM\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90f33-111">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="90f33-111">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f33-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="90f33-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="90f33-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90f33-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90f33-114">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90f33-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90f33-115">Élément managé affecté par le service.</span><span class="sxs-lookup"><span data-stu-id="90f33-115">The managed element that is affected by the service.</span></span>

</dd> <dt>

<span data-ttu-id="90f33-116">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="90f33-116">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f33-117">Type de données **: \_ service CIM**</span><span class="sxs-lookup"><span data-stu-id="90f33-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="90f33-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90f33-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90f33-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90f33-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90f33-120">Service qui affecte l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="90f33-120">The service that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="90f33-121">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="90f33-121">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f33-122">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90f33-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="90f33-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90f33-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90f33-124">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="90f33-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="90f33-125">Effet sur l’élément managé.</span><span class="sxs-lookup"><span data-stu-id="90f33-125">The effect on the managed element.</span></span> <span data-ttu-id="90f33-126">Ce tableau correspond au tableau **OtherElementEffectsDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="90f33-126">This array corresponds to the **OtherElementEffectsDescriptions** array.</span></span>

<span data-ttu-id="90f33-127">\- Utilisation exclusive (2) : aucun autre service ne peut avoir cette association avec l’élément.</span><span class="sxs-lookup"><span data-stu-id="90f33-127">\- Exclusive Use (2): No other Service may have this association to the element.</span></span>

<span data-ttu-id="90f33-128">\- Impact sur les performances (3) : déconseillé en faveur de « consomme », « améliore les performances » ou « dégrade les performances ».</span><span class="sxs-lookup"><span data-stu-id="90f33-128">\- Performance Impact (3): Deprecated in favor of "Consumes", "Enhances Performance", or "Degrades Performance".</span></span> <span data-ttu-id="90f33-129">L’exécution du service peut améliorer ou dégrader les performances de l’élément.</span><span class="sxs-lookup"><span data-stu-id="90f33-129">Execution of the Service may enhance or degrade the performance of the element.</span></span> <span data-ttu-id="90f33-130">Cela peut être un effet secondaire de l’exécution ou comme une conséquence prévue des méthodes fournies par le service.</span><span class="sxs-lookup"><span data-stu-id="90f33-130">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="90f33-131">\- Intégrité de l’élément (4) : déconseillé en faveur de « consomme », « améliore l’intégrité » ou « dégrade l’intégrité ».</span><span class="sxs-lookup"><span data-stu-id="90f33-131">\- Element Integrity (4): Deprecated in favor of "Consumes", "Enhances Integrity", or "Degrades Integrity".</span></span> <span data-ttu-id="90f33-132">L’exécution du service peut améliorer ou dégrader l’intégrité de l’élément.</span><span class="sxs-lookup"><span data-stu-id="90f33-132">Execution of the Service may enhance or degrade the integrity of the element.</span></span> <span data-ttu-id="90f33-133">Cela peut être un effet secondaire de l’exécution ou comme une conséquence prévue des méthodes fournies par le service.</span><span class="sxs-lookup"><span data-stu-id="90f33-133">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="90f33-134">\- Gère (5) : le service gère l’élément.</span><span class="sxs-lookup"><span data-stu-id="90f33-134">\- Manages (5): The Service manages the element.</span></span>

<span data-ttu-id="90f33-135">\- Consomme (6) : l’exécution du service consomme une partie ou la totalité de l’élément associé à la suite de l’exécution du service.</span><span class="sxs-lookup"><span data-stu-id="90f33-135">\- Consumes (6): Execution of the Service consumes some or all of the associated element as a consequence of running the Service.</span></span> <span data-ttu-id="90f33-136">Par exemple, le service peut consommer des cycles de processeur, ce qui peut affecter les performances ou le stockage qui peut affecter à la fois les performances et l’intégrité.</span><span class="sxs-lookup"><span data-stu-id="90f33-136">For example, the Service may consume CPU cycles, which may affect performance, or Storage which may affect both performance and integrity.</span></span> <span data-ttu-id="90f33-137">(Par exemple, le manque de stockage gratuit peut nuire à l’intégrité en réduisant la possibilité d’enregistrer l’État.</span><span class="sxs-lookup"><span data-stu-id="90f33-137">(For instance, the lack of free storage can degrade integrity by reducing the ability to save state.</span></span> <span data-ttu-id="90f33-138">) « Consomme » peut être utilisé seul ou conjointement avec d’autres valeurs, en particulier « diminue les performances » et « dégrade l’intégrité ».</span><span class="sxs-lookup"><span data-stu-id="90f33-138">) "Consumes" may be used alone or in conjunction with other values, in particular, "Degrades Performance" and "Degrades Integrity".</span></span>

<span data-ttu-id="90f33-139">Les « Manage » et non « consomment » doivent être utilisés pour refléter les services d’allocation qui peuvent être fournis par un service.</span><span class="sxs-lookup"><span data-stu-id="90f33-139">"Manages" and not "Consumes" should be used to reflect allocation services that may be provided by a Service.</span></span>

<span data-ttu-id="90f33-140">\- Améliore l’intégrité (7) : le service peut améliorer l’intégrité de l’élément associé.</span><span class="sxs-lookup"><span data-stu-id="90f33-140">\- Enhances Integrity (7): The Service may enhance integrity of the associated element.</span></span>

<span data-ttu-id="90f33-141">\- Dégradation de l’intégrité (8) : le service peut nuire à l’intégrité de l’élément associé.</span><span class="sxs-lookup"><span data-stu-id="90f33-141">\- Degrades Integrity (8): The Service may degrade integrity of the associated element.</span></span>

<span data-ttu-id="90f33-142">\- Améliore les performances (9) : le service peut améliorer les performances de l’élément associé.</span><span class="sxs-lookup"><span data-stu-id="90f33-142">\- Enhances Performance (9): The Service may enhance performance of the associated element.</span></span>

<span data-ttu-id="90f33-143">\- Diminue les performances (10) : le service peut dégrader les performances de l’élément associé.</span><span class="sxs-lookup"><span data-stu-id="90f33-143">\- Degrades Performance (10): The Service may degrade performance of the associated element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="90f33-144">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="90f33-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="90f33-145">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="90f33-145">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="90f33-146">**Utilisation exclusive** (2)</span><span class="sxs-lookup"><span data-stu-id="90f33-146">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="90f33-147">**Impact sur les performances** (3)</span><span class="sxs-lookup"><span data-stu-id="90f33-147">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="90f33-148">**Intégrité de l’élément** (4)</span><span class="sxs-lookup"><span data-stu-id="90f33-148">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

<span data-ttu-id="90f33-149">**Gère** (5)</span><span class="sxs-lookup"><span data-stu-id="90f33-149">**Manages** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

<span data-ttu-id="90f33-150">**Consomme** (6)</span><span class="sxs-lookup"><span data-stu-id="90f33-150">**Consumes** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

<span data-ttu-id="90f33-151">**Améliore l’intégrité** (7)</span><span class="sxs-lookup"><span data-stu-id="90f33-151">**Enhances Integrity** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

<span data-ttu-id="90f33-152">**Dégradation de l’intégrité** (8)</span><span class="sxs-lookup"><span data-stu-id="90f33-152">**Degrades Integrity** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

<span data-ttu-id="90f33-153">**Améliore les performances** (9)</span><span class="sxs-lookup"><span data-stu-id="90f33-153">**Enhances Performance** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

<span data-ttu-id="90f33-154">**Dégrader les performances** (10)</span><span class="sxs-lookup"><span data-stu-id="90f33-154">**Degrades Performance** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="90f33-155">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="90f33-155">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="90f33-156">**Fournisseur réservé** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="90f33-156">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="90f33-157">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="90f33-157">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f33-158">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="90f33-158">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="90f33-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90f33-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90f33-160">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="90f33-160">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="90f33-161">Chaque élément du tableau fournit des informations supplémentaires pour l’élément correspondant dans le tableau **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="90f33-161">Each item in the array provides additional information for the corresponding item in the **ElementEffects** array.</span></span> <span data-ttu-id="90f33-162">Une description est requise pour tout élément du tableau **ElementEffects** ayant la valeur **other** (« 1 »).</span><span class="sxs-lookup"><span data-stu-id="90f33-162">A description is required for any item in the **ElementEffects** array that is set to **Other** ("1").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90f33-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90f33-163">Requirements</span></span>



| <span data-ttu-id="90f33-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90f33-164">Requirement</span></span> | <span data-ttu-id="90f33-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="90f33-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90f33-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90f33-166">Minimum supported client</span></span><br/> | <span data-ttu-id="90f33-167">Windows 8</span><span class="sxs-lookup"><span data-stu-id="90f33-167">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="90f33-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90f33-168">Minimum supported server</span></span><br/> | <span data-ttu-id="90f33-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90f33-169">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="90f33-170">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90f33-170">Namespace</span></span><br/>                | <span data-ttu-id="90f33-171">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="90f33-171">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="90f33-172">MOF</span><span class="sxs-lookup"><span data-stu-id="90f33-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90f33-173"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90f33-173"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90f33-174">DLL</span><span class="sxs-lookup"><span data-stu-id="90f33-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90f33-175"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90f33-175"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

