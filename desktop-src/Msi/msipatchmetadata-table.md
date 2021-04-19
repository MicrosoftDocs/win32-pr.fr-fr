---
description: La table MsiPatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer le correctif et utilisé par ajout/suppression de programmes.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Table MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522447"
---
# <a name="msipatchmetadata-table"></a><span data-ttu-id="a9f24-103">Table MsiPatchMetadata</span><span class="sxs-lookup"><span data-stu-id="a9f24-103">MsiPatchMetadata Table</span></span>

<span data-ttu-id="a9f24-104">La table MsiPatchMetadata contient des informations sur un correctif Windows Installer requis pour supprimer le correctif et utilisé par **Ajout/suppression de programmes**.</span><span class="sxs-lookup"><span data-stu-id="a9f24-104">The MsiPatchMetadata Table contains information about a Windows Installer patch that is required to remove the patch and that is used by **Add/Remove Programs**.</span></span>

<span data-ttu-id="a9f24-105">Les correctifs installés sans ce tableau dans la base de données des correctifs (fichier. msp) ne peuvent pas être supprimés et des informations sont manquantes dans **Ajout/suppression de programmes**.</span><span class="sxs-lookup"><span data-stu-id="a9f24-105">Patches installed without this table present in the patch database (.msp file) cannot be removed, and are missing some information from **Add/Remove Programs**.</span></span> <span data-ttu-id="a9f24-106">La table doit se trouver dans la base de données du fichier correctif et non dans une transformation dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="a9f24-106">The table must be in the database of the patch file and not in a transform in the patch.</span></span>

<span data-ttu-id="a9f24-107">La table MsiPatchMetadata contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9f24-107">The MsiPatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="a9f24-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="a9f24-108">Column</span></span>   | <span data-ttu-id="a9f24-109">Type</span><span class="sxs-lookup"><span data-stu-id="a9f24-109">Type</span></span>                         | <span data-ttu-id="a9f24-110">Clé</span><span class="sxs-lookup"><span data-stu-id="a9f24-110">Key</span></span> | <span data-ttu-id="a9f24-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a9f24-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="a9f24-112">Company</span><span class="sxs-lookup"><span data-stu-id="a9f24-112">Company</span></span>  | [<span data-ttu-id="a9f24-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a9f24-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a9f24-114">O</span><span class="sxs-lookup"><span data-stu-id="a9f24-114">Y</span></span>   | <span data-ttu-id="a9f24-115">O</span><span class="sxs-lookup"><span data-stu-id="a9f24-115">Y</span></span>        |
| <span data-ttu-id="a9f24-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="a9f24-116">Property</span></span> | [<span data-ttu-id="a9f24-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a9f24-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="a9f24-118">O</span><span class="sxs-lookup"><span data-stu-id="a9f24-118">Y</span></span>   | <span data-ttu-id="a9f24-119">N</span><span class="sxs-lookup"><span data-stu-id="a9f24-119">N</span></span>        |
| <span data-ttu-id="a9f24-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9f24-120">Value</span></span>    | [<span data-ttu-id="a9f24-121">Text</span><span class="sxs-lookup"><span data-stu-id="a9f24-121">Text</span></span>](text.md)             | <span data-ttu-id="a9f24-122">N</span><span class="sxs-lookup"><span data-stu-id="a9f24-122">N</span></span>   | <span data-ttu-id="a9f24-123">N</span><span class="sxs-lookup"><span data-stu-id="a9f24-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a9f24-124">Colonnes</span><span class="sxs-lookup"><span data-stu-id="a9f24-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a9f24-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Entreprise</span><span class="sxs-lookup"><span data-stu-id="a9f24-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="a9f24-126">Nom de la société.</span><span class="sxs-lookup"><span data-stu-id="a9f24-126">The name of the company.</span></span> <span data-ttu-id="a9f24-127">Un champ vide (valeur null) indique que la ligne contient une des propriétés de métadonnées standard de l’Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a9f24-127">An empty field (a Null value) indicates that the row contains one of the standard metadata properties of the Windows Installer.</span></span> <span data-ttu-id="a9f24-128">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a9f24-128">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="a9f24-129">En ajoutant une ligne à la table et en entrant un nom de société dans ce champ, vous pouvez ajouter n’importe quelle société pour étendre le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a9f24-129">By adding a row to the table and entering a company name in this field, you can add any company to extend the property set.</span></span>

</dd> <dt>

<span data-ttu-id="a9f24-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété</span><span class="sxs-lookup"><span data-stu-id="a9f24-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="a9f24-131">Nom d’une propriété de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a9f24-131">The name of a metadata property.</span></span>

</dd> <dt>

<span data-ttu-id="a9f24-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="a9f24-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a9f24-133">Valeur de la propriété de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a9f24-133">The value of the metadata property.</span></span> <span data-ttu-id="a9f24-134">La valeur ne peut jamais être null ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="a9f24-134">This can never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9f24-135">Notes</span><span class="sxs-lookup"><span data-stu-id="a9f24-135">Remarks</span></span>

<span data-ttu-id="a9f24-136">Disponible dans Windows Installer 3,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a9f24-136">Available in Windows Installer 3.0 and later.</span></span>

<span data-ttu-id="a9f24-137">Les lignes de la table MsiPatchMetadata qui contiennent une valeur null dans le champ CompanyName font référence à l’une des propriétés de métadonnées de Windows Installer standard suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9f24-137">Rows in the MsiPatchMetadata Table that contain a Null value in the CompanyName field refer to one of the following standard Windows Installer metadata properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a9f24-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="a9f24-138">Property</span></span></th>
<th><span data-ttu-id="a9f24-139">Description</span><span class="sxs-lookup"><span data-stu-id="a9f24-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9f24-140">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="a9f24-140">AllowRemoval</span></span></td>
<td><span data-ttu-id="a9f24-141">Indique si le correctif est un correctif qui peut être <a href="uninstallable-patches.md">installé</a>.</span><span class="sxs-lookup"><span data-stu-id="a9f24-141">Indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="a9f24-142">Si le champ de valeur contient 0 (zéro), le correctif ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="a9f24-142">If the value field contains 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="a9f24-143">Si le champ de valeur contient un (1), le correctif est un correctif qui peut être désinstallé. cette propriété est inscrite et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9f24-143">If the value field contains one (1), the patch is an Uninstallable Patch.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9f24-144">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="a9f24-144">ManufacturerName</span></span></td>
<td><span data-ttu-id="a9f24-145">Nom du fabricant de l’application.</span><span class="sxs-lookup"><span data-stu-id="a9f24-145">Name of the manufacturer of the application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9f24-146">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="a9f24-146">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="a9f24-147">Indique que le correctif cible la version RTM du produit ou le correctif de mise à niveau majeur le plus récent.</span><span class="sxs-lookup"><span data-stu-id="a9f24-147">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="a9f24-148">Créez cette propriété facultative dans les correctifs de mise à niveau mineurs qui contiennent des informations de séquencement pour indiquer que le correctif supprime tous les correctifs jusqu’à la version RTM du produit, ou jusqu’au correctif de mise à niveau majeur le plus récent.</span><span class="sxs-lookup"><span data-stu-id="a9f24-148">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="a9f24-149">Cette propriété est disponible dans Windows Installer 3,1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a9f24-149">This property is available in Windows Installer 3.1 and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9f24-150">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="a9f24-150">TargetProductName</span></span></td>
<td><span data-ttu-id="a9f24-151">Nom de l’application ou de la suite d’applications cible.</span><span class="sxs-lookup"><span data-stu-id="a9f24-151">Name of the application or target application suite.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9f24-152">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="a9f24-152">MoreInfoURL</span></span></td>
<td><span data-ttu-id="a9f24-153">URL qui fournit des informations spécifiques à ce correctif.</span><span class="sxs-lookup"><span data-stu-id="a9f24-153">A URL that provides information specific to this patch.</span></span> <span data-ttu-id="a9f24-154">Cette propriété est enregistrée et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9f24-154">This property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="a9f24-155">À partir de Windows XP avec Service Pack 2 (SP2), cette valeur peut être le lien de support pour le correctif affiché dans <strong>Ajout/suppression de programmes</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9f24-155">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9f24-156">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="a9f24-156">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="a9f24-157">Heure de création du fichier. msp sous la forme mm-jj-aa HH : MM (mois-jour-année heure : minute).</span><span class="sxs-lookup"><span data-stu-id="a9f24-157">Creation time of the .msp file in the form of mm-dd-yy HH:MM (month-day-year hour:minute).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9f24-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9f24-158">DisplayName</span></span></td>
<td><span data-ttu-id="a9f24-159">Titre du correctif logiciel qui est OK pour un affichage public.</span><span class="sxs-lookup"><span data-stu-id="a9f24-159">A title for the patch that is okay for public display.</span></span> <span data-ttu-id="a9f24-160">Cette propriété est enregistrée et sa valeur peut être obtenue à l’aide de la fonction <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9f24-160">This property is registered, and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="a9f24-161">À partir de Windows XP avec SP2, cette valeur est le nom du correctif qui est affiché dans <strong>Ajout/suppression de programmes</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9f24-161">Beginning with Windows XP with SP2, this value is the name of the patch that is displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9f24-162">Description</span><span class="sxs-lookup"><span data-stu-id="a9f24-162">Description</span></span></td>
<td><span data-ttu-id="a9f24-163">Brève description du correctif.</span><span class="sxs-lookup"><span data-stu-id="a9f24-163">Brief description of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9f24-164">classification ;</span><span class="sxs-lookup"><span data-stu-id="a9f24-164">Classification</span></span></td>
<td><span data-ttu-id="a9f24-165">Valeur de chaîne qui contient la catégorie arbitraire des mises à jour telles que définies par l’auteur du correctif.</span><span class="sxs-lookup"><span data-stu-id="a9f24-165">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="a9f24-166">Par exemple, les auteurs de correctifs peuvent spécifier que chaque correctif soit classé comme un correctif, un correctif cumulatif de sécurité, une mise à jour critique, une mise à jour, un service pack ou un correctif cumulatif.</span><span class="sxs-lookup"><span data-stu-id="a9f24-166">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="a9f24-167">Cette propriété est requise.</span><span class="sxs-lookup"><span data-stu-id="a9f24-167">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9f24-168">OptimizeCA</span><span class="sxs-lookup"><span data-stu-id="a9f24-168">OptimizeCA</span></span></td>
<td><span data-ttu-id="a9f24-169">Indique si le Windows Installer doit ignorer les actions personnalisées lors de l’application du correctif.</span><span class="sxs-lookup"><span data-stu-id="a9f24-169">Indicates whether the Windows Installer should skip custom actions when applying the patch.</span></span> <span data-ttu-id="a9f24-170">Cela peut réduire le temps nécessaire pour appliquer le correctif.</span><span class="sxs-lookup"><span data-stu-id="a9f24-170">This can reduce the time required to apply the patch.</span></span> <span data-ttu-id="a9f24-171">La propriété OptimizeCA peut avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a9f24-171">The OptimizeCA property can have one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a9f24-172">0-ne pas ignorer les actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a9f24-172">0 - Do not skip any custom actions.</span></span></li>
<li><span data-ttu-id="a9f24-173">1-ignorer les actions personnalisées d’affectation de répertoire et de propriété.</span><span class="sxs-lookup"><span data-stu-id="a9f24-173">1 - Skip property and directory assignment custom actions.</span></span> <span data-ttu-id="a9f24-174">Le <a href="custom-action-type-35.md">type d’action personnalisé 35</a> et le type d' <a href="custom-action-type-51.md">action personnalisé 51</a> peuvent être des actions personnalisées de propriété et d’assignation de répertoire.</span><span class="sxs-lookup"><span data-stu-id="a9f24-174"><a href="custom-action-type-35.md">Custom Action Type 35</a> and <a href="custom-action-type-51.md">Custom Action Type 51</a> can be property and directory assignment custom actions.</span></span></li>
<li><span data-ttu-id="a9f24-175">2-ignorer les actions personnalisées immédiates qui ne se trouvent pas dans les assignations de propriété ou de répertoire.</span><span class="sxs-lookup"><span data-stu-id="a9f24-175">2 - Skip immediate custom actions that do not fall into the property or directory assignments.</span></span> <span data-ttu-id="a9f24-176">Les actions personnalisées immédiates n’incluent pas l’option msidbCustomActionTypeInScript dans la colonne type de la <a href="customaction-table.md">table CustomAction</a>.</span><span class="sxs-lookup"><span data-stu-id="a9f24-176">The immediate custom actions do not include msidbCustomActionTypeInScript option in the Type column of the <a href="customaction-table.md">CustomAction Table</a>.</span></span></li>
<li><span data-ttu-id="a9f24-177">4-ignorer les actions personnalisées qui s’exécutent dans le script.</span><span class="sxs-lookup"><span data-stu-id="a9f24-177">4 - Skip custom actions that run within the script.</span></span></li>
</ul>
<span data-ttu-id="a9f24-178">La valeur de OptimizeCA doit être la même pour tous les correctifs en cours d’installation ou aucune action personnalisée n’est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a9f24-178">The value of OptimizeCA must be the same for all patches that are being installed or no custom actions are skipped.</span></span> <span data-ttu-id="a9f24-179">Par exemple, si deux correctifs sont installés et que OptimizeCA est défini sur les valeurs 1 et 2, aucune action personnalisée n’est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a9f24-179">For example, if two patches are being installed, and OptimizeCA is set to the values 1 and 2 respectively, no custom actions are skipped.</span></span> <br/> <span data-ttu-id="a9f24-180">Les valeurs de OptimizeCA peuvent être combinées lors du traitement de plusieurs nouveaux correctifs.</span><span class="sxs-lookup"><span data-stu-id="a9f24-180">The values of OptimizeCA can be combined when processing multiple new patches.</span></span> <span data-ttu-id="a9f24-181">Si tous les correctifs ont 1 (un) inclus dans les valeurs, toutes les actions personnalisées d’affectation de répertoire et de propriété sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="a9f24-181">If all patches have a 1 (one) included in the values, then all property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="a9f24-182">Si un correctif a la valeur 3 (trois) pour la propriété et que l’un des correctifs a la valeur 1 (un) pour la propriété, les actions personnalisées d’affectation de répertoire et de propriété sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="a9f24-182">If one patch has the value 3 (three)for the property, and one patch has the value 1 (one) for the property, the property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="a9f24-183">Toutefois, les autres actions personnalisées immédiates s’exécutent, car tous les correctifs demandés ne sont pas ignorés.</span><span class="sxs-lookup"><span data-stu-id="a9f24-183">However, the other immediate custom actions run, because not all of the patches requested are skipped.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9f24-184">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="a9f24-184">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="a9f24-185">Si cette propriété a la valeur 1 (un) dans tous les correctifs à appliquer dans une transaction, une application du correctif est optimisée si possible.</span><span class="sxs-lookup"><span data-stu-id="a9f24-185">If this property is set to 1 (one) in all the patches to be applied in a transaction, an application of the patch is optimized if possible.</span></span> <span data-ttu-id="a9f24-186">Pour plus d’informations, consultez <a href="patch-optimization.md">optimisation des correctifs</a>.</span><span class="sxs-lookup"><span data-stu-id="a9f24-186">For more information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="a9f24-187">Disponible à partir de Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="a9f24-187">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a><span data-ttu-id="a9f24-188">Validation</span><span class="sxs-lookup"><span data-stu-id="a9f24-188">Validation</span></span>

<dl>

[<span data-ttu-id="a9f24-189">ICE03</span><span class="sxs-lookup"><span data-stu-id="a9f24-189">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a9f24-190">ICE06</span><span class="sxs-lookup"><span data-stu-id="a9f24-190">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="a9f24-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9f24-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f24-192">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="a9f24-192">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




