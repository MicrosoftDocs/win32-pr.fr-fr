---
description: Fait référence aux informations de compatibilité d’un ordinateur virtuel (en cas d’exécution sur un système informatique d’ordinateur virtuel) ou à un ordinateur hôte (lorsqu’il est exécuté sur un système d’ordinateur hôte).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Classe Msvm_CompatibilityVector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866413"
---
# <a name="msvm_compatibilityvector-class"></a><span data-ttu-id="1823b-103">MSVM \_ CompatibilityVector, classe</span><span class="sxs-lookup"><span data-stu-id="1823b-103">Msvm\_CompatibilityVector class</span></span>

<span data-ttu-id="1823b-104">Fait référence aux informations de compatibilité d’un ordinateur virtuel (en cas d’exécution sur un système informatique d’ordinateur virtuel) ou à un ordinateur hôte (lorsqu’il est exécuté sur un système d’ordinateur hôte).</span><span class="sxs-lookup"><span data-stu-id="1823b-104">References the compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span>

<span data-ttu-id="1823b-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1823b-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1823b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1823b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a><span data-ttu-id="1823b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1823b-107">Members</span></span>

<span data-ttu-id="1823b-108">La classe **MSVM \_ CompatibilityVector** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1823b-108">The **Msvm\_CompatibilityVector** class has these types of members:</span></span>

-   [<span data-ttu-id="1823b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1823b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1823b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1823b-110">Properties</span></span>

<span data-ttu-id="1823b-111">La classe **MSVM \_ CompatibilityVector** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1823b-111">The **Msvm\_CompatibilityVector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1823b-112">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="1823b-112">**CompareOperation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1823b-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1823b-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1823b-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1823b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1823b-115">Identifie l’opération de comparaison qui retourne true si et seulement si deux vecteurs sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="1823b-115">Identifies the comparison operation that will return true if and only if two vectors are compatible.</span></span> <span data-ttu-id="1823b-116">Les données de la machine virtuelle se trouvent sur le côté gauche de la comparaison, et les données de l’hôte se trouvent sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="1823b-116">The VM's data is on the left hand side of the comparison, and the host's data is on the right hand side.</span></span>

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

<span data-ttu-id="1823b-117">**Égal** à (0)</span><span class="sxs-lookup"><span data-stu-id="1823b-117">**Equal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

<span data-ttu-id="1823b-118">Sur- **ensemble** (1)</span><span class="sxs-lookup"><span data-stu-id="1823b-118">**Superset** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

<span data-ttu-id="1823b-119">**Sous-ensemble** (2)</span><span class="sxs-lookup"><span data-stu-id="1823b-119">**Subset** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

<span data-ttu-id="1823b-120">**Disjoint** (3)</span><span class="sxs-lookup"><span data-stu-id="1823b-120">**Disjoint** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

<span data-ttu-id="1823b-121">**GreaterThan** (4)</span><span class="sxs-lookup"><span data-stu-id="1823b-121">**GreaterThan** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

<span data-ttu-id="1823b-122">**GreaterThanOrEqual** (5)</span><span class="sxs-lookup"><span data-stu-id="1823b-122">**GreaterThanOrEqual** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

<span data-ttu-id="1823b-123">**LessThan** (6)</span><span class="sxs-lookup"><span data-stu-id="1823b-123">**LessThan** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

<span data-ttu-id="1823b-124">**LessThanOrEqual** (7)</span><span class="sxs-lookup"><span data-stu-id="1823b-124">**LessThanOrEqual** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

<span data-ttu-id="1823b-125">**Multiple** (8)</span><span class="sxs-lookup"><span data-stu-id="1823b-125">**Multiple** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

<span data-ttu-id="1823b-126">**Divisible** (9)</span><span class="sxs-lookup"><span data-stu-id="1823b-126">**Divisible** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1823b-127">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="1823b-127">**CompatibilityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1823b-128">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1823b-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1823b-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1823b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1823b-130">Données d’attribut de compatibilité réelles utilisées pour la comparaison.</span><span class="sxs-lookup"><span data-stu-id="1823b-130">The actual compatibility attribute data that is used for comparison.</span></span>

</dd> <dt>

<span data-ttu-id="1823b-131">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="1823b-131">**VectorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1823b-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1823b-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1823b-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1823b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1823b-134">Identifie un vecteur de compatibilité qui représente un attribut spécifique.</span><span class="sxs-lookup"><span data-stu-id="1823b-134">Identifies a compatibility vector that represents a specific attribute.</span></span> <span data-ttu-id="1823b-135">Cette propriété est utilisée pour faire correspondre les vecteurs correspondants entre un hôte et une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1823b-135">This property is used to match corresponding vectors between a host and a VM.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1823b-136">Notes</span><span class="sxs-lookup"><span data-stu-id="1823b-136">Remarks</span></span>

<span data-ttu-id="1823b-137">La méthode [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) de la classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) retourne un tableau d’instances **MSVM \_ CompatibilityVector** pour l’hôte (si elle est exécutée sur l’hôte) ou une machine virtuelle (si elle est exécutée sur la machine virtuelle).</span><span class="sxs-lookup"><span data-stu-id="1823b-137">The [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class returns an array of **Msvm\_CompatibilityVector** instances for the host (if run on the host) or a VM (if run on the VM).</span></span> <span data-ttu-id="1823b-138">Chaque entrée **MSVM \_ CompatibilityVector** de la liste décrit un vecteur d’attribut de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="1823b-138">Each **Msvm\_CompatibilityVector** entry in the list describes a compatibility attribute vector.</span></span> <span data-ttu-id="1823b-139">Pour qu’une machine virtuelle soit compatible avec un hôte, tous ses attributs de compatibilité doivent être compatibles avec les attributs de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1823b-139">For a VM to be compatible with a host, all of its compatibility attributes must be compatible with the host s attributes.</span></span>

<span data-ttu-id="1823b-140">Chaque entrée **MSVM \_ CompatibilityVector** a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="1823b-140">Each **Msvm\_CompatibilityVector** entry has these properties:</span></span>

<dl> <dt>

<span data-ttu-id="1823b-141">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="1823b-141">**VectorId**</span></span>
</dt> <dd>

<span data-ttu-id="1823b-142">Identifie de façon unique le vecteur de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="1823b-142">Uniquely identifies the compatibility vector.</span></span> <span data-ttu-id="1823b-143">Il est utilisé pour faire correspondre les vecteurs à comparer entre un hôte et une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1823b-143">This is used to match the vectors to compare between a host and a VM.</span></span>

</dd> <dt>

<span data-ttu-id="1823b-144">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="1823b-144">**CompareOperation**</span></span>
</dt> <dd>

<span data-ttu-id="1823b-145">Identifie l’opération de comparaison qui détermine si les vecteurs sont compatibles.</span><span class="sxs-lookup"><span data-stu-id="1823b-145">Identifies the comparison operation that determines whether the vectors are compatible.</span></span>

</dd> <dt>

<span data-ttu-id="1823b-146">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="1823b-146">**CompatibilityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="1823b-147">Contient l’attribut de compatibilité réel ; Il s’agit effectivement de la charge utile d’attribut (par exemple, masque de fonctionnalité de processeur, taille de vidage de ligne de cache, etc.).</span><span class="sxs-lookup"><span data-stu-id="1823b-147">Contains the actual compatibility attribute; This is effectively the attribute payload (e.g. processor feature mask, cache line flush size, etc.)</span></span>

</dd> </dl>

<span data-ttu-id="1823b-148">L’ensemble des opérations définies pour **CompareOperation** implique simplement une comparaison d’entiers de base et une logique au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="1823b-148">The set of operations defined for **CompareOperation** just involve basic integer comparison and bitwise logic.</span></span> <span data-ttu-id="1823b-149">Cela permet au contenu réel de **CompatibilityInfo** de rester opaque.</span><span class="sxs-lookup"><span data-stu-id="1823b-149">This enables the actual contents of **CompatibilityInfo** to remain opaque.</span></span> <span data-ttu-id="1823b-150">L’ensemble d’opérations inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1823b-150">The set of operations include:</span></span>



| <span data-ttu-id="1823b-151">CompareOperation</span><span class="sxs-lookup"><span data-stu-id="1823b-151">CompareOperation</span></span> | <span data-ttu-id="1823b-152">Description</span><span class="sxs-lookup"><span data-stu-id="1823b-152">Description</span></span>                                      | <span data-ttu-id="1823b-153">Comparaison du pseudocode</span><span class="sxs-lookup"><span data-stu-id="1823b-153">Pseudocode Comparison</span></span>                |
|------------------|--------------------------------------------------|--------------------------------------|
| <span data-ttu-id="1823b-154">VmCcEqual</span><span class="sxs-lookup"><span data-stu-id="1823b-154">VmCcEqual</span></span>        | <span data-ttu-id="1823b-155">VmAttr doit être égal à HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-155">VmAttr must equal HostAttr</span></span>                       | <span data-ttu-id="1823b-156">If (VmAttr = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="1823b-156">If (VmAttr == HostAttr)</span></span>              |
| <span data-ttu-id="1823b-157">VmCcSuperSet</span><span class="sxs-lookup"><span data-stu-id="1823b-157">VmCcSuperSet</span></span>     | <span data-ttu-id="1823b-158">VmAttr doit être un sur-ensemble de HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-158">VmAttr must be a superset of HostAttr</span></span>            | <span data-ttu-id="1823b-159">If ((VmAttr & HostAttr) = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="1823b-159">If ((VmAttr & HostAttr) == HostAttr)</span></span> |
| <span data-ttu-id="1823b-160">VmCcSubSet</span><span class="sxs-lookup"><span data-stu-id="1823b-160">VmCcSubSet</span></span>       | <span data-ttu-id="1823b-161">VmAttr doit être un sous-ensemble de HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-161">VmAttr must be a subset of HostAttr</span></span>              | <span data-ttu-id="1823b-162">If ((VmAttr & HostAttr) = = VmAttr)</span><span class="sxs-lookup"><span data-stu-id="1823b-162">If ((VmAttr & HostAttr) == VmAttr)</span></span>   |
| <span data-ttu-id="1823b-163">VmCcDisjointSet</span><span class="sxs-lookup"><span data-stu-id="1823b-163">VmCcDisjointSet</span></span>  | <span data-ttu-id="1823b-164">VmAttr doit être un ensemble disjoint de HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-164">VmAttr must be a disjoint set from HostAttr</span></span>      | <span data-ttu-id="1823b-165">If ((VmAttr & HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="1823b-165">If ((VmAttr & HostAttr) == 0)</span></span>        |
| <span data-ttu-id="1823b-166">VmCcGreater</span><span class="sxs-lookup"><span data-stu-id="1823b-166">VmCcGreater</span></span>      | <span data-ttu-id="1823b-167">VmAttr doit être supérieur à HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-167">VmAttr must be greater than HostAttr</span></span>             | <span data-ttu-id="1823b-168">If (VmAttr > HostAttr)</span><span class="sxs-lookup"><span data-stu-id="1823b-168">If (VmAttr > HostAttr)</span></span>            |
| <span data-ttu-id="1823b-169">VmCcGreaterEqual</span><span class="sxs-lookup"><span data-stu-id="1823b-169">VmCcGreaterEqual</span></span> | <span data-ttu-id="1823b-170">VmAttr doit être supérieur ou égal à HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-170">VmAttr must be greater than or equal to HostAttr</span></span> | <span data-ttu-id="1823b-171">If (VmAttr >= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="1823b-171">If (VmAttr >= HostAttr)</span></span>           |
| <span data-ttu-id="1823b-172">VmCcLess</span><span class="sxs-lookup"><span data-stu-id="1823b-172">VmCcLess</span></span>         | <span data-ttu-id="1823b-173">VmAttr doit être inférieur à HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-173">VmAttr must be less than HostAttr</span></span>                | <span data-ttu-id="1823b-174">If (VmAttr < HostAttr)</span><span class="sxs-lookup"><span data-stu-id="1823b-174">If (VmAttr < HostAttr)</span></span>            |
| <span data-ttu-id="1823b-175">VmCcLessEqual</span><span class="sxs-lookup"><span data-stu-id="1823b-175">VmCcLessEqual</span></span>    | <span data-ttu-id="1823b-176">VmAttr doit être inférieur ou égal à HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-176">VmAttr must be less than or equal to HostAttr</span></span>    | <span data-ttu-id="1823b-177">If (VmAttr <= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="1823b-177">If (VmAttr <= HostAttr)</span></span>           |
| <span data-ttu-id="1823b-178">VmCcMultiple</span><span class="sxs-lookup"><span data-stu-id="1823b-178">VmCcMultiple</span></span>     | <span data-ttu-id="1823b-179">VmAttr doit être un multiple de HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-179">VmAttr must be a multiple of HostAttr</span></span>            | <span data-ttu-id="1823b-180">If ((VmAttr% HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="1823b-180">If ((VmAttr % HostAttr) == 0)</span></span>        |
| <span data-ttu-id="1823b-181">VmCcDivisor</span><span class="sxs-lookup"><span data-stu-id="1823b-181">VmCcDivisor</span></span>      | <span data-ttu-id="1823b-182">VmAttr doit être un diviseur de HostAttr</span><span class="sxs-lookup"><span data-stu-id="1823b-182">VmAttr must be a divisor of HostAttr</span></span>             | <span data-ttu-id="1823b-183">If ((HostAttr% VmAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="1823b-183">If ((HostAttr % VmAttr) == 0)</span></span>        |



 

<span data-ttu-id="1823b-184">SCVMM doit effectuer ces étapes pour déterminer si une machine virtuelle est compatible avec un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="1823b-184">SCVMM needs to do these steps to determine whether a VM is compatible with a host.</span></span>

<span data-ttu-id="1823b-185">**Pour déterminer si une machine virtuelle est compatible avec un ordinateur hôte**</span><span class="sxs-lookup"><span data-stu-id="1823b-185">**To determine whether a VM is compatible with a host**</span></span>

1.  <span data-ttu-id="1823b-186">Itérez au sein de tous les éléments **\_ CompatibilityVector MSVM** pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1823b-186">Iterate through all of the **Msvm\_CompatibilityVector** elements for the VM.</span></span>
2.  <span data-ttu-id="1823b-187">Pour chaque élément **MSVM \_ CompatibilityVector** , utilisez l’opération de compatibilité spécifiée dans **CompareOperation** pour comparer le vecteur de compatibilité matérielle des machines virtuelles avec le vecteur de compatibilité correspondant pour l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="1823b-187">For each **Msvm\_CompatibilityVector** element, use the compatibility operation specified in **CompareOperation** to compare the VM s hardware compatibility vector with the corresponding compatibility vector for the host.</span></span>
3.  <span data-ttu-id="1823b-188">Si tous les éléments **MSVM \_ CompatibilityVector** de la machine virtuelle sont jugés compatibles, la machine virtuelle est compatible avec l’hôte (du point de vue de la fonctionnalité de processeur).</span><span class="sxs-lookup"><span data-stu-id="1823b-188">If the all of the **Msvm\_CompatibilityVector** elements from the VM are deemed compatible, the VM is compatible with the host (from a processor feature perspective).</span></span>

## <a name="requirements"></a><span data-ttu-id="1823b-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1823b-189">Requirements</span></span>



| <span data-ttu-id="1823b-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1823b-190">Requirement</span></span> | <span data-ttu-id="1823b-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="1823b-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1823b-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1823b-192">Minimum supported client</span></span><br/> | <span data-ttu-id="1823b-193">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1823b-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1823b-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1823b-194">Minimum supported server</span></span><br/> | <span data-ttu-id="1823b-195">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1823b-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1823b-196">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1823b-196">Namespace</span></span><br/>                | <span data-ttu-id="1823b-197">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1823b-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1823b-198">MOF</span><span class="sxs-lookup"><span data-stu-id="1823b-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1823b-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1823b-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1823b-200">DLL</span><span class="sxs-lookup"><span data-stu-id="1823b-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1823b-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1823b-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1823b-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1823b-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1823b-203">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="1823b-203">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="1823b-204">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="1823b-204">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




