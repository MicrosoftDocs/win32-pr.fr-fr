---
description: La table PatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer un correctif et utilisé par ajout/suppression de programmes.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Table PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536665"
---
# <a name="patchmetadata-table-patchwizdll"></a><span data-ttu-id="575b7-103">Table PatchMetadata (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="575b7-103">PatchMetadata Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="575b7-104">La table PatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer un correctif et utilisé par ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="575b7-104">The PatchMetadata Table contains information about a Windows Installer patch that is required to remove a patch and that is used by Add/Remove Programs.</span></span> <span data-ttu-id="575b7-105">Toutes les propriétés de la table PatchMetadata sont ajoutées à la [table MsiPatchMetadata](msipatchmetadata-table.md) du fichier. msp pour un correctif.</span><span class="sxs-lookup"><span data-stu-id="575b7-105">All the properties in the PatchMetadata Table are added to the [MsiPatchMetadata Table](msipatchmetadata-table.md) of the .msp file for a patch.</span></span>

<span data-ttu-id="575b7-106">La table PatchMetadata est requise dans les fichiers de propriétés de création de correctifs (fichiers. PCP) qui ont un MinimumRequiredMsiVersion égal à 300 dans le [tableau des propriétés](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="575b7-106">The PatchMetadata Table is required in patch creation properties files (.pcp files) that have a MinimumRequiredMsiVersion equal to 300 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="575b7-107">La table est facultative si MinimumRequiredMsiVersion n’est pas égal à 300.</span><span class="sxs-lookup"><span data-stu-id="575b7-107">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

<span data-ttu-id="575b7-108">La table PatchMetadata contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="575b7-108">The PatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="575b7-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="575b7-109">Column</span></span>   | <span data-ttu-id="575b7-110">Type</span><span class="sxs-lookup"><span data-stu-id="575b7-110">Type</span></span> | <span data-ttu-id="575b7-111">Clé</span><span class="sxs-lookup"><span data-stu-id="575b7-111">Key</span></span> | <span data-ttu-id="575b7-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="575b7-112">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="575b7-113">Company</span><span class="sxs-lookup"><span data-stu-id="575b7-113">Company</span></span>  | <span data-ttu-id="575b7-114">text</span><span class="sxs-lookup"><span data-stu-id="575b7-114">text</span></span> | <span data-ttu-id="575b7-115">O</span><span class="sxs-lookup"><span data-stu-id="575b7-115">Y</span></span>   | <span data-ttu-id="575b7-116">O</span><span class="sxs-lookup"><span data-stu-id="575b7-116">Y</span></span>        |
| <span data-ttu-id="575b7-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="575b7-117">Property</span></span> | <span data-ttu-id="575b7-118">text</span><span class="sxs-lookup"><span data-stu-id="575b7-118">text</span></span> | <span data-ttu-id="575b7-119">O</span><span class="sxs-lookup"><span data-stu-id="575b7-119">Y</span></span>   | <span data-ttu-id="575b7-120">N</span><span class="sxs-lookup"><span data-stu-id="575b7-120">N</span></span>        |
| <span data-ttu-id="575b7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="575b7-121">Value</span></span>    | <span data-ttu-id="575b7-122">text</span><span class="sxs-lookup"><span data-stu-id="575b7-122">text</span></span> |     | <span data-ttu-id="575b7-123">O</span><span class="sxs-lookup"><span data-stu-id="575b7-123">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="575b7-124">Colonnes</span><span class="sxs-lookup"><span data-stu-id="575b7-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="575b7-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Entreprise</span><span class="sxs-lookup"><span data-stu-id="575b7-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="575b7-126">Nom de la société.</span><span class="sxs-lookup"><span data-stu-id="575b7-126">The name of the company.</span></span> <span data-ttu-id="575b7-127">Un champ vide (valeur null) indique que cette ligne contient une des propriétés de métadonnées standard.</span><span class="sxs-lookup"><span data-stu-id="575b7-127">An empty field (a Null value) indicates that this row contains one of the standard metadata properties.</span></span> <span data-ttu-id="575b7-128">Une société peut étendre le jeu de propriétés en ajoutant une ligne à la table et en entrant un nom de société dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="575b7-128">A company can extend the property set by adding a row to the table, and entering a company name in this field.</span></span>

</dd> <dt>

<span data-ttu-id="575b7-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété</span><span class="sxs-lookup"><span data-stu-id="575b7-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="575b7-130">Nom d’une propriété de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="575b7-130">The name of a metadata property.</span></span> <span data-ttu-id="575b7-131">Les propriétés AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, description et classification sont requises dans la table PatchMetadata.</span><span class="sxs-lookup"><span data-stu-id="575b7-131">The AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description, and Classification properties are required in the PatchMetadata Table .</span></span> <span data-ttu-id="575b7-132">Ce champ doit contenir l’une des propriétés de métadonnées standard suivantes si le champ Company est vide (valeur null).</span><span class="sxs-lookup"><span data-stu-id="575b7-132">This field must contain one of the following standard metadata properties if the Company field is empty (a Null value).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="575b7-133">Propriété</span><span class="sxs-lookup"><span data-stu-id="575b7-133">Property</span></span></th>
<th><span data-ttu-id="575b7-134">Description</span><span class="sxs-lookup"><span data-stu-id="575b7-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="575b7-135">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="575b7-135">AllowRemoval</span></span></td>
<td><span data-ttu-id="575b7-136">Valeur entière qui indique si le correctif logiciel est un correctif pouvant être <a href="uninstallable-patches.md">installé</a>.</span><span class="sxs-lookup"><span data-stu-id="575b7-136">An integer value that indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="575b7-137">Si le champ de valeur contient un 0 (zéro), le correctif ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="575b7-137">If the Value field contains a 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="575b7-138">Si le champ valeur contient 1 (un), le correctif est un correctif qui peut être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="575b7-138">If the Value field contains 1 (one), the patch is an Uninstallable Patch.</span></span> <span data-ttu-id="575b7-139">Cette propriété est obligatoire. Cette propriété est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="575b7-139">This property is required.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="575b7-140">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="575b7-140">ManufacturerName</span></span></td>
<td><span data-ttu-id="575b7-141">Valeur de chaîne qui contient le nom du fabricant de l’application.</span><span class="sxs-lookup"><span data-stu-id="575b7-141">A string value that contains the name of the manufacturer of the application.</span></span> <span data-ttu-id="575b7-142">Cette propriété est requise.</span><span class="sxs-lookup"><span data-stu-id="575b7-142">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="575b7-143">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="575b7-143">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="575b7-144">Indique que le correctif cible la version RTM du produit ou le correctif de mise à niveau majeur le plus récent.</span><span class="sxs-lookup"><span data-stu-id="575b7-144">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="575b7-145">Créez cette propriété facultative dans les correctifs de mise à niveau mineurs qui contiennent des informations de séquencement pour indiquer que le correctif supprime tous les correctifs jusqu’à la version RTM du produit, ou jusqu’au correctif de mise à niveau majeur le plus récent.</span><span class="sxs-lookup"><span data-stu-id="575b7-145">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="575b7-146">Cette propriété est disponible à partir de Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="575b7-146">This property is available beginning with Windows Installer 3.1.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="575b7-147">Pour exiger que Windows Installer 3,1 soit installé pour appliquer le correctif, affectez à la propriété MinimumRequiredMsiVersion la valeur 310 dans la <a href="properties-table-patchwiz-dll-.md">table des propriétés</a> du fichier. PCP.</span><span class="sxs-lookup"><span data-stu-id="575b7-147">To require that Windows Installer 3.1 be installed to apply the patch, set the MinimumRequiredMsiVersion property to 310 in the <a href="properties-table-patchwiz-dll-.md">Properties Table</a> of the .pcp file.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="575b7-148">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="575b7-148">TargetProductName</span></span></td>
<td><span data-ttu-id="575b7-149">Valeur de chaîne qui contient le nom de l’application ou de la suite d’applications cible.</span><span class="sxs-lookup"><span data-stu-id="575b7-149">A string value that contains the name of the application or target application suite.</span></span> <span data-ttu-id="575b7-150">Cette propriété est requise.</span><span class="sxs-lookup"><span data-stu-id="575b7-150">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="575b7-151">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="575b7-151">MoreInfoURL</span></span></td>
<td><span data-ttu-id="575b7-152">Valeur de chaîne qui contient une URL pointant vers les informations de ce correctif.</span><span class="sxs-lookup"><span data-stu-id="575b7-152">A string value that contains a URL pointing to information for this patch.</span></span> <span data-ttu-id="575b7-153">Cette propriété requise est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="575b7-153">This required property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="575b7-154">À partir de Windows XP avec Service Pack 2 (SP2), cette valeur peut être le lien de support pour le correctif affiché dans Ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="575b7-154">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in Add/Remove Programs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="575b7-155">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="575b7-155">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="575b7-156">Valeur de chaîne qui contient l’heure de création du fichier. msp au format mm-jj-aa HH : MM (mois-jour-année heure : minute).</span><span class="sxs-lookup"><span data-stu-id="575b7-156">A string value that contains the creation time of the .msp file in the form mm-dd-yy HH:MM (month-day-year hour:minute).</span></span> <span data-ttu-id="575b7-157">Cette propriété est facultative.</span><span class="sxs-lookup"><span data-stu-id="575b7-157">This property is optional.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="575b7-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="575b7-158">DisplayName</span></span></td>
<td><span data-ttu-id="575b7-159">Valeur de chaîne qui contient le titre du correctif logiciel qui est adapté à un affichage public.</span><span class="sxs-lookup"><span data-stu-id="575b7-159">A string value that contains the title for the patch that is suitable for public display.</span></span> <span data-ttu-id="575b7-160">Cette propriété est requise.</span><span class="sxs-lookup"><span data-stu-id="575b7-160">This property is required.</span></span> <span data-ttu-id="575b7-161">Cette propriété est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="575b7-161">This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="575b7-162">À compter de Windows XP avec SP2, cette valeur correspond au nom du correctif affiché dans Ajout/suppression de programmes, à compter de Windows XP avec SP2.</span><span class="sxs-lookup"><span data-stu-id="575b7-162">Beginning with Windows XP with SP2, this value is the name of the patch displayed in Add/Remove Programs beginning with Windows XP with SP2.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="575b7-163">Description</span><span class="sxs-lookup"><span data-stu-id="575b7-163">Description</span></span></td>
<td><span data-ttu-id="575b7-164">Valeur de chaîne qui contient une brève description du correctif.</span><span class="sxs-lookup"><span data-stu-id="575b7-164">A string value that contains a brief description of the patch.</span></span> <span data-ttu-id="575b7-165">Cette propriété est requise.</span><span class="sxs-lookup"><span data-stu-id="575b7-165">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="575b7-166">classification ;</span><span class="sxs-lookup"><span data-stu-id="575b7-166">Classification</span></span></td>
<td><span data-ttu-id="575b7-167">Valeur de chaîne qui contient la catégorie arbitraire des mises à jour telles que définies par l’auteur du correctif.</span><span class="sxs-lookup"><span data-stu-id="575b7-167">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="575b7-168">Par exemple, les auteurs de correctifs peuvent spécifier que chaque correctif soit classé comme un correctif, un correctif cumulatif de sécurité, une mise à jour critique, une mise à jour, un service pack ou un correctif cumulatif.</span><span class="sxs-lookup"><span data-stu-id="575b7-168">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="575b7-169">Cette propriété est requise.</span><span class="sxs-lookup"><span data-stu-id="575b7-169">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="575b7-170">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="575b7-170">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="575b7-171">Si cette propriété a la valeur 1 (un) dans tous les correctifs à appliquer dans une transaction, l’application du correctif logiciel est optimisée si possible.</span><span class="sxs-lookup"><span data-stu-id="575b7-171">If this property is set to 1 (one) in all the patches to be applied in a transaction, the application of the patch is optimized if possible.</span></span> <span data-ttu-id="575b7-172">Pour plus d’informations, consultez <a href="patch-optimization.md">optimisation des correctifs</a>.</span><span class="sxs-lookup"><span data-stu-id="575b7-172">For information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="575b7-173">Disponible à partir de Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="575b7-173">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="575b7-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="575b7-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="575b7-175">Valeur de la propriété de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="575b7-175">Value of the metadata property.</span></span> <span data-ttu-id="575b7-176">La valeur ne peut jamais être null ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="575b7-176">This can never be Null or an empty string.</span></span> <span data-ttu-id="575b7-177">Cette valeur peut être localisée.</span><span class="sxs-lookup"><span data-stu-id="575b7-177">This value can be localized.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="575b7-178">Notes</span><span class="sxs-lookup"><span data-stu-id="575b7-178">Remarks</span></span>

<span data-ttu-id="575b7-179">Disponible à partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="575b7-179">Available beginning in Windows Installer 3.0.</span></span>

<span data-ttu-id="575b7-180">Toutes les propriétés créées dans la table PatchMetadata sont ajoutées à la table MsiPatchMetadata du fichier MSP.</span><span class="sxs-lookup"><span data-stu-id="575b7-180">All properties authored into the PatchMetadata Table are added to the MsiPatchMetadata table of the msp file.</span></span> <span data-ttu-id="575b7-181">Les propriétés AllowRemoval, MoreInfoURL et DisplayName sont inscrites et sont accessibles par le biais de [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="575b7-181">AllowRemoval, MoreInfoURL and DisplayName properties are registered and are accessible through the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

 

 




