---
description: La table MsiPatchSequence contient toutes les informations requises par le programme d’installation pour déterminer la séquence d’application d’un correctif logiciel de petite mise à jour par rapport à tous les autres correctifs.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Table MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530769"
---
# <a name="msipatchsequence-table"></a><span data-ttu-id="7a261-103">Table MsiPatchSequence</span><span class="sxs-lookup"><span data-stu-id="7a261-103">MsiPatchSequence Table</span></span>

<span data-ttu-id="7a261-104">La table MsiPatchSequence contient toutes les informations requises par le programme d’installation pour déterminer la séquence d’application d’un correctif logiciel de [petite mise à jour](small-updates.md) par rapport à tous les autres correctifs.</span><span class="sxs-lookup"><span data-stu-id="7a261-104">The MsiPatchSequence table contains all the information the installer requires to determine the sequence of application of a [small update](small-updates.md) patch relative to all other patches.</span></span> <span data-ttu-id="7a261-105">La table doit se trouver dans la base de données du fichier correctif et non dans une transformation dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="7a261-105">The table must be in the database of the patch file and not in a transform in the patch.</span></span> <span data-ttu-id="7a261-106">Le programme d’installation ignore cette table lorsque vous appliquez un correctif de [mise à niveau majeure](major-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="7a261-106">The installer ignores this table when applying a [major upgrade](major-upgrades.md) patch.</span></span> <span data-ttu-id="7a261-107">Lors de l’application d’un correctif de [mise à niveau mineure](minor-upgrades.md) , le programme d’installation utilise uniquement cette table pour identifier les correctifs remplacés qui ne doivent pas être séquencés.</span><span class="sxs-lookup"><span data-stu-id="7a261-107">When applying a [minor upgrade](minor-upgrades.md) patch, the installer only uses this table to identify superseded patches that must not be sequenced.</span></span>

<span data-ttu-id="7a261-108">La **table MsiPatchSequence** contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a261-108">The **MsiPatchSequence table** has the following columns.</span></span>



| <span data-ttu-id="7a261-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="7a261-109">Column</span></span>      | <span data-ttu-id="7a261-110">Type</span><span class="sxs-lookup"><span data-stu-id="7a261-110">Type</span></span>                         | <span data-ttu-id="7a261-111">Clé</span><span class="sxs-lookup"><span data-stu-id="7a261-111">Key</span></span> | <span data-ttu-id="7a261-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="7a261-112">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="7a261-113">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="7a261-113">PatchFamily</span></span> | [<span data-ttu-id="7a261-114">Identificateur</span><span class="sxs-lookup"><span data-stu-id="7a261-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="7a261-115">O</span><span class="sxs-lookup"><span data-stu-id="7a261-115">Y</span></span>   | <span data-ttu-id="7a261-116">N</span><span class="sxs-lookup"><span data-stu-id="7a261-116">N</span></span>        |
| <span data-ttu-id="7a261-117">ProductCode</span><span class="sxs-lookup"><span data-stu-id="7a261-117">ProductCode</span></span> | [<span data-ttu-id="7a261-118">GUID</span><span class="sxs-lookup"><span data-stu-id="7a261-118">GUID</span></span>](guid.md)             | <span data-ttu-id="7a261-119">O</span><span class="sxs-lookup"><span data-stu-id="7a261-119">Y</span></span>   | <span data-ttu-id="7a261-120">O</span><span class="sxs-lookup"><span data-stu-id="7a261-120">Y</span></span>        |
| <span data-ttu-id="7a261-121">Séquence</span><span class="sxs-lookup"><span data-stu-id="7a261-121">Sequence</span></span>    | [<span data-ttu-id="7a261-122">Version</span><span class="sxs-lookup"><span data-stu-id="7a261-122">Version</span></span>](version.md)       | <span data-ttu-id="7a261-123">N</span><span class="sxs-lookup"><span data-stu-id="7a261-123">N</span></span>   | <span data-ttu-id="7a261-124">N</span><span class="sxs-lookup"><span data-stu-id="7a261-124">N</span></span>        |
| <span data-ttu-id="7a261-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="7a261-125">Attributes</span></span>  | [<span data-ttu-id="7a261-126">Integer</span><span class="sxs-lookup"><span data-stu-id="7a261-126">Integer</span></span>](integer.md)       | <span data-ttu-id="7a261-127">N</span><span class="sxs-lookup"><span data-stu-id="7a261-127">N</span></span>   | <span data-ttu-id="7a261-128">O</span><span class="sxs-lookup"><span data-stu-id="7a261-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7a261-129">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7a261-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7a261-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="7a261-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="7a261-131">Spécifie que le correctif est membre de la famille de correctifs nommée dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="7a261-131">Specifies that the patch is a member of the patch family named in this field.</span></span> <span data-ttu-id="7a261-132">Les correctifs de la même famille de correctifs qui ciblent la même version du produit sont triés selon les valeurs de la colonne séquence.</span><span class="sxs-lookup"><span data-stu-id="7a261-132">Patches in the same patch family that target the same product version are sorted by the values in the Sequence column.</span></span> <span data-ttu-id="7a261-133">Les correctifs au sein de la famille de correctifs sont appliqués au produit cible dans l’ordre de la plus grande séquence.</span><span class="sxs-lookup"><span data-stu-id="7a261-133">The patches within the patch family are applied to the target product in the order of increasing sequence.</span></span> <span data-ttu-id="7a261-134">Le PatchFamily est également utilisé pour déterminer les correctifs à remplacer.</span><span class="sxs-lookup"><span data-stu-id="7a261-134">The PatchFamily is also used to determine which patches are to be superseded.</span></span> <span data-ttu-id="7a261-135">Un correctif peut figurer dans plusieurs lignes et appartenir à plusieurs familles de correctifs s’il s’applique à plusieurs produits ou comprend plusieurs correctifs.</span><span class="sxs-lookup"><span data-stu-id="7a261-135">A patch may be listed in multiple rows and belong to multiple patch families if it applies to more than one product or includes multiple fixes.</span></span>

<span data-ttu-id="7a261-136">La Windows Installer n’interprète pas la valeur PatchFamily de quelque manière que ce soit par comparaison avec d’autres valeurs PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="7a261-136">The Windows Installer does not interpret the PatchFamily value in any way other than comparisons for equality against other PatchFamily values.</span></span> <span data-ttu-id="7a261-137">Une valeur PatchFamily doit être unique dans le ProductCode ciblé par l’ensemble de correctifs.</span><span class="sxs-lookup"><span data-stu-id="7a261-137">A PatchFamily value must be unique within the ProductCode targeted by the set of patches.</span></span> <span data-ttu-id="7a261-138">Dans les scénarios complexes de mise à jour corrective, l’identificateur PatchFamily peut avoir besoin d’être globalement unique.</span><span class="sxs-lookup"><span data-stu-id="7a261-138">In the complex patching scenarios the PatchFamily identifier may need to be globally unique.</span></span>

</dd> <dt>

<span data-ttu-id="7a261-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span><span class="sxs-lookup"><span data-stu-id="7a261-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span></span>
</dt> <dd>

<span data-ttu-id="7a261-140">Une valeur dans ce champ est facultative.</span><span class="sxs-lookup"><span data-stu-id="7a261-140">A value in this field is optional.</span></span> <span data-ttu-id="7a261-141">Si un GUID de [Code de produit](product-codes.md) est entré dans ce champ et que le correctif est appliqué au produit spécifié, le correctif est trié et appliqué en tant que membre du PatchFamily spécifié.</span><span class="sxs-lookup"><span data-stu-id="7a261-141">If a [product code](product-codes.md) GUID is entered in this field and the patch is being applied to the specified product, the patch is sorted and applied as a member of the specified PatchFamily.</span></span> <span data-ttu-id="7a261-142">Si un GUID de code de produit est entré dans ce champ et que le correctif n’est pas appliqué au produit spécifié par ProductCode, cette ligne est ignorée.</span><span class="sxs-lookup"><span data-stu-id="7a261-142">If a product code GUID is entered in this field and the patch is not being applied to the product specified by ProductCode, this row is ignored.</span></span> <span data-ttu-id="7a261-143">Si la valeur de ProductCode est NULL, le correctif est trié et appliqué en tant que membre de PatchFamily pour toutes les cibles du correctif, quel que soit le code du produit.</span><span class="sxs-lookup"><span data-stu-id="7a261-143">If the value in ProductCode is NULL, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

<span data-ttu-id="7a261-144">Un correctif peut avoir plusieurs lignes dans le même PatchFamily et une autre ProductCode pour chaque produit ciblé par le correctif.</span><span class="sxs-lookup"><span data-stu-id="7a261-144">A patch can have multiple rows in the same PatchFamily and a different ProductCode for each product targeted by the patch.</span></span> <span data-ttu-id="7a261-145">Une ligne pour le PatchFamily peut spécifier la valeur NULL pour ProductCode.</span><span class="sxs-lookup"><span data-stu-id="7a261-145">One row for the PatchFamily can specify NULL for ProductCode.</span></span> <span data-ttu-id="7a261-146">Si le produit cible correspond à une ligne avec une valeur ProductCode non NULL, le programme d’installation utilise la ligne correspondante et ignore la ligne avec la valeur ProductCode NULL.</span><span class="sxs-lookup"><span data-stu-id="7a261-146">If the target product matches a row with a non-NULL ProductCode, the installer uses the matching row and ignores the row with the NULL ProductCode.</span></span> <span data-ttu-id="7a261-147">Si aucun des codes de produit spécifiés ne correspond à la cible, le correctif est trié et appliqué en tant que membre de PatchFamily pour toutes les cibles du correctif, quel que soit le code du produit.</span><span class="sxs-lookup"><span data-stu-id="7a261-147">If none of the specified product codes match the target, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

</dd> <dt>

<span data-ttu-id="7a261-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="7a261-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="7a261-149">La valeur dans la colonne Sequence spécifie la séquence de ce correctif dans le PatchFamily spécifié.</span><span class="sxs-lookup"><span data-stu-id="7a261-149">The value in the Sequence column specifies the sequence of this patch within the specified PatchFamily.</span></span> <span data-ttu-id="7a261-150">La valeur de la séquence est exprimée au format des données de [version](version.md) .</span><span class="sxs-lookup"><span data-stu-id="7a261-150">The value in Sequence is expressed in the format of [Version](version.md) data.</span></span> <span data-ttu-id="7a261-151">La valeur contient entre 1 et 4 champs et chaque champ a une plage comprise entre 0 et 65535.</span><span class="sxs-lookup"><span data-stu-id="7a261-151">The value contains between 1 and 4 fields and each field has a range of 0 to 65535.</span></span> <span data-ttu-id="7a261-152">Les membres de PatchFamily sont triés et appliqués au produit cible dans l’ordre des valeurs de séquence de plus en plus nombreuses.</span><span class="sxs-lookup"><span data-stu-id="7a261-152">Members of PatchFamily are sorted and applied to the target product in the order of increasing Sequence values.</span></span> <span data-ttu-id="7a261-153">Par exemple, les six valeurs suivantes sont en constante évolution : 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.</span><span class="sxs-lookup"><span data-stu-id="7a261-153">For example, the following six values are increasing: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.</span></span>

</dd> <dt>

<span data-ttu-id="7a261-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="7a261-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="7a261-155">La présence de l’attribut **msidbPatchSequenceSupersedeEarlier** dans une ligne indique que le correctif de [mise à jour de petite taille](small-updates.md) remplace les mises à jour fournies par tous les correctifs ayant des valeurs de séquence moindres dans le même PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="7a261-155">The presence of the **msidbPatchSequenceSupersedeEarlier** attribute in a row indicates that the [small update](small-updates.md) patch supersedes the updates provided by all patches with lesser Sequence values in the same PatchFamily.</span></span> <span data-ttu-id="7a261-156">Ce correctif contient tous les correctifs fournis par les correctifs antérieurs dans le PatchFamily spécifié.</span><span class="sxs-lookup"><span data-stu-id="7a261-156">This patch contains all fixes provided by earlier patches in the specified PatchFamily.</span></span> <span data-ttu-id="7a261-157">Cet attribut ne signifie pas que ce correctif remplace les correctifs antérieurs dans tous les cas, car les correctifs précédents peuvent appartenir à plusieurs familles de correctifs.</span><span class="sxs-lookup"><span data-stu-id="7a261-157">This attribute does not mean that this patch supersedes the earlier patches in all cases because the earlier patches can belong to multiple patch families.</span></span>

<span data-ttu-id="7a261-158">Un correctif de [petite mise à jour](small-updates.md) ne peut pas remplacer une [mise à niveau mineure](minor-upgrades.md) ou une [mise à niveau majeure](major-upgrades.md) en tout cas, même si **msidbPatchSequenceSupersedeEarlier** est défini.</span><span class="sxs-lookup"><span data-stu-id="7a261-158">A [small update](small-updates.md) patch cannot supersede a [minor upgrade](minor-upgrades.md) or [major upgrade](major-upgrades.md) patch under any circumstances, even if the **msidbPatchSequenceSupersedeEarlier** is set.</span></span> 

| <span data-ttu-id="7a261-159">Nom</span><span class="sxs-lookup"><span data-stu-id="7a261-159">Name</span></span>                                   | <span data-ttu-id="7a261-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a261-160">Value</span></span> | <span data-ttu-id="7a261-161">Signification</span><span class="sxs-lookup"><span data-stu-id="7a261-161">Meaning</span></span>                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | <span data-ttu-id="7a261-162">0x00</span><span class="sxs-lookup"><span data-stu-id="7a261-162">0x00</span></span>  | <span data-ttu-id="7a261-163">Indique une valeur de séquencement simple.</span><span class="sxs-lookup"><span data-stu-id="7a261-163">Indicates a simple sequencing value.</span></span>                              |
| <span data-ttu-id="7a261-164">**msidbPatchSequenceSupersedeEarlier**</span><span class="sxs-lookup"><span data-stu-id="7a261-164">**msidbPatchSequenceSupersedeEarlier**</span></span> | <span data-ttu-id="7a261-165">0x01</span><span class="sxs-lookup"><span data-stu-id="7a261-165">0x01</span></span>  | <span data-ttu-id="7a261-166">Indique un correctif qui remplace les correctifs antérieurs dans cette famille.</span><span class="sxs-lookup"><span data-stu-id="7a261-166">Indicates a patch that supersedes earlier patches in this family.</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="7a261-167">Validation</span><span class="sxs-lookup"><span data-stu-id="7a261-167">Validation</span></span>

<dl>

[<span data-ttu-id="7a261-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="7a261-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7a261-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="7a261-169">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="7a261-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a261-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a261-171">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="7a261-171">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



