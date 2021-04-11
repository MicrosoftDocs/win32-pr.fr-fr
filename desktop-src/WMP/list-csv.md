---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player Online stores, list.csv
- magasins en ligne, list.csv
- tapez 1 magasins en ligne, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101237"
---
# <a name="listcsv"></a><span data-ttu-id="c6540-107">list.csv</span><span class="sxs-lookup"><span data-stu-id="c6540-107">list.csv</span></span>

<span data-ttu-id="c6540-108">Ce fichier contient une entrée pour chacune des listes contenues dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="c6540-108">This file contains an entry for each of the lists the catalog contains.</span></span> <span data-ttu-id="c6540-109">Les listes peuvent être des listes de pistes, d’albums, d’artistes, de genres, de sous-genres ou de flux radio. ou ils peuvent être des listes d’autres listes.</span><span class="sxs-lookup"><span data-stu-id="c6540-109">Lists can be lists of tracks, albums, artists, genres, subgenres, or radio feeds; or they can be lists of other lists.</span></span> <span data-ttu-id="c6540-110">Chaque entrée de liste est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c6540-110">Each list entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="c6540-111">Les champs doivent apparaître dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="c6540-111">Fields must appear in the order listed.</span></span>

<span data-ttu-id="c6540-112">La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="c6540-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="c6540-113">Elle ne fait pas référence au type de données du contenu.</span><span class="sxs-lookup"><span data-stu-id="c6540-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="c6540-114">Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.</span><span class="sxs-lookup"><span data-stu-id="c6540-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6540-115">Champ</span><span class="sxs-lookup"><span data-stu-id="c6540-115">Field</span></span></th>
<th><span data-ttu-id="c6540-116">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c6540-116">Required</span></span></th>
<th><span data-ttu-id="c6540-117">Format</span><span class="sxs-lookup"><span data-stu-id="c6540-117">Format</span></span></th>
<th><span data-ttu-id="c6540-118">Description</span><span class="sxs-lookup"><span data-stu-id="c6540-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6540-119">ListID</span><span class="sxs-lookup"><span data-stu-id="c6540-119">ListID</span></span></td>
<td><span data-ttu-id="c6540-120">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-120">Yes</span></span></td>
<td><span data-ttu-id="c6540-121">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c6540-121">Non-negative integer.</span></span></td>
<td><span data-ttu-id="c6540-122">Identificateur de liste, unique dans list.csv.</span><span class="sxs-lookup"><span data-stu-id="c6540-122">List identifier, unique within list.csv.</span></span> <span data-ttu-id="c6540-123">Doit être non négatif et inférieur à 2 ^ 32. <strong>Affichage d’un nœud de liste dans un contrôle Tree View :</strong> Si la valeur de ListID est 0, 1, 2, 3, 4, 5, 6 ou 7, la liste apparaît comme un nœud personnalisé sous le nœud de niveau supérieur de votre magasin en ligne dans le contrôle d’arborescence du lecteur.</span><span class="sxs-lookup"><span data-stu-id="c6540-123">Must be non-negative and less than 2^32.<strong>Displaying a list node in tree view control:</strong> If the ListID is 0, 1, 2, 3, 4, 5, 6, or 7, the list will appear as a custom node under your online store's top-level node in the Player's tree view control.</span></span> <span data-ttu-id="c6540-124">Les nœuds personnalisés apparaissent avant les nœuds standard sous le nœud de niveau supérieur du magasin en ligne et sont positionnés par ListID dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="c6540-124">Custom nodes appear before the standard nodes under the online store's top-level node, and they are positioned in ascending order by ListID.</span></span> <span data-ttu-id="c6540-125">Par exemple, s’il existe trois nœuds personnalisés, avec ListId de 1, 3 et 5, ils sont affichés en premier, deuxième et troisième sous le nœud de niveau supérieur de la boutique en ligne.</span><span class="sxs-lookup"><span data-stu-id="c6540-125">For example, if there are three custom nodes, with ListIDs of 1, 3, and 5, they will be displayed first, second, and third under the online store's top level node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6540-126">ListTitle</span><span class="sxs-lookup"><span data-stu-id="c6540-126">ListTitle</span></span></td>
<td><span data-ttu-id="c6540-127">Non</span><span class="sxs-lookup"><span data-stu-id="c6540-127">No</span></span></td>
<td><span data-ttu-id="c6540-128">Chaîne Unicode. Exemple : 10 premiers résultats</span><span class="sxs-lookup"><span data-stu-id="c6540-128">Unicode string.Example: Top Ten Hits</span></span><br/></td>
<td><span data-ttu-id="c6540-129">Titre de la liste.</span><span class="sxs-lookup"><span data-stu-id="c6540-129">List title.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6540-130">ListSubtitle</span><span class="sxs-lookup"><span data-stu-id="c6540-130">ListSubtitle</span></span></td>
<td><span data-ttu-id="c6540-131">Non</span><span class="sxs-lookup"><span data-stu-id="c6540-131">No</span></span></td>
<td><span data-ttu-id="c6540-132">chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="c6540-132">Unicode string</span></span></td>
<td><span data-ttu-id="c6540-133">Autre titre de liste, affiché sur la deuxième ligne de l’affichage en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="c6540-133">List alternate title, displayed in the second line of the Tile view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6540-134">ListDescription</span><span class="sxs-lookup"><span data-stu-id="c6540-134">ListDescription</span></span></td>
<td><span data-ttu-id="c6540-135">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-135">Yes</span></span></td>
<td><span data-ttu-id="c6540-136">chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="c6540-136">Unicode string</span></span></td>
<td><span data-ttu-id="c6540-137">Afficher le texte convivial de liste (affiché dans les pages de propriétés).</span><span class="sxs-lookup"><span data-stu-id="c6540-137">List friendly display text (displayed in property pages).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6540-138">Linked_ItemType</span><span class="sxs-lookup"><span data-stu-id="c6540-138">Linked_ItemType</span></span></td>
<td><span data-ttu-id="c6540-139">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-139">Yes</span></span></td>
<td><span data-ttu-id="c6540-140">Chaîne Unicode. Format : [T | P | A | L | G | S | R</span><span class="sxs-lookup"><span data-stu-id="c6540-140">Unicode string.Format: [T|P|A|L|G|S|R]</span></span><br/> <span data-ttu-id="c6540-141">Exemple : T</span><span class="sxs-lookup"><span data-stu-id="c6540-141">Example: T</span></span><br/></td>
<td><span data-ttu-id="c6540-142">Indique le type des éléments liés.</span><span class="sxs-lookup"><span data-stu-id="c6540-142">Indicates the type of the linked items.</span></span>
<ul>
<li><span data-ttu-id="c6540-143">T = Track</span><span class="sxs-lookup"><span data-stu-id="c6540-143">T= Track</span></span></li>
<li><span data-ttu-id="c6540-144">P = l’intervenant</span><span class="sxs-lookup"><span data-stu-id="c6540-144">P = Performer</span></span></li>
<li><span data-ttu-id="c6540-145">A = album</span><span class="sxs-lookup"><span data-stu-id="c6540-145">A = Album</span></span></li>
<li><span data-ttu-id="c6540-146">L = liste</span><span class="sxs-lookup"><span data-stu-id="c6540-146">L = List</span></span></li>
<li><span data-ttu-id="c6540-147">G = genre</span><span class="sxs-lookup"><span data-stu-id="c6540-147">G = Genre</span></span></li>
<li><span data-ttu-id="c6540-148">S = sous-genre</span><span class="sxs-lookup"><span data-stu-id="c6540-148">S = Subgenre</span></span></li>
<li><span data-ttu-id="c6540-149">R = radio</span><span class="sxs-lookup"><span data-stu-id="c6540-149">R = Radio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6540-150">ListPrice</span><span class="sxs-lookup"><span data-stu-id="c6540-150">ListPrice</span></span></td>
<td><span data-ttu-id="c6540-151">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-151">Yes</span></span></td>
<td><span data-ttu-id="c6540-152">Chaîne Unicode. Exemple : $9,99</span><span class="sxs-lookup"><span data-stu-id="c6540-152">Unicode string.Example: $9.99</span></span><br/></td>
<td><span data-ttu-id="c6540-153">Prix de la liste.</span><span class="sxs-lookup"><span data-stu-id="c6540-153">Price of the list.</span></span> <span data-ttu-id="c6540-154">Le symbole monétaire doit être inclus. Une valeur zéro signifie que la liste est libre.</span><span class="sxs-lookup"><span data-stu-id="c6540-154">The currency symbol should be included.A zero means the list is free.</span></span> <span data-ttu-id="c6540-155">Aucune valeur signifie que le prix est inconnu.</span><span class="sxs-lookup"><span data-stu-id="c6540-155">No value means the price is unknown.</span></span> <span data-ttu-id="c6540-156">Un trait d’Union signifie que la liste ne peut pas être achetée.</span><span class="sxs-lookup"><span data-stu-id="c6540-156">A hyphen means the list cannot be purchased.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6540-157">Popularité</span><span class="sxs-lookup"><span data-stu-id="c6540-157">Popularity</span></span></td>
<td><span data-ttu-id="c6540-158">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-158">Yes</span></span></td>
<td><span data-ttu-id="c6540-159">Valeur entière ou décimale. Exemple : 1259,3</span><span class="sxs-lookup"><span data-stu-id="c6540-159">Integer or decimal value.Example: 1259.3</span></span><br/></td>
<td><span data-ttu-id="c6540-160">Indique le classement de la popularité lorsque cette liste apparaît dans d’autres listes.</span><span class="sxs-lookup"><span data-stu-id="c6540-160">Indicates the popularity ranking when this list appears in other lists.</span></span> <span data-ttu-id="c6540-161">Peut être zéro s’il n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="c6540-161">Can be zero if not applicable..</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6540-162">IsRecentlyAdded</span><span class="sxs-lookup"><span data-stu-id="c6540-162">IsRecentlyAdded</span></span></td>
<td><span data-ttu-id="c6540-163">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-163">Yes</span></span></td>
<td><span data-ttu-id="c6540-164">Booléen. format : [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="c6540-164">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="c6540-165">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="c6540-165">Example: 0</span></span><br/></td>
<td><span data-ttu-id="c6540-166">Indique si la liste a été récemment ajoutée.</span><span class="sxs-lookup"><span data-stu-id="c6540-166">Indicates whether the list was recently added.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6540-167">IsFeatured</span><span class="sxs-lookup"><span data-stu-id="c6540-167">IsFeatured</span></span></td>
<td><span data-ttu-id="c6540-168">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-168">Yes</span></span></td>
<td><span data-ttu-id="c6540-169">Booléen. format : [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="c6540-169">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="c6540-170">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="c6540-170">Example: 0</span></span><br/></td>
<td><span data-ttu-id="c6540-171">Indique si la liste est proposée.</span><span class="sxs-lookup"><span data-stu-id="c6540-171">Indicates whether the list is featured.</span></span> <span data-ttu-id="c6540-172">Peut être utilisé pour déterminer l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="c6540-172">Can be used in determining sort order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6540-173">EditorialGlyph</span><span class="sxs-lookup"><span data-stu-id="c6540-173">EditorialGlyph</span></span></td>
<td><span data-ttu-id="c6540-174">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-174">Yes</span></span></td>
<td><span data-ttu-id="c6540-175">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c6540-175">Non-negative integer.</span></span> <span data-ttu-id="c6540-176">Doit correspondre à 0.</span><span class="sxs-lookup"><span data-stu-id="c6540-176">Should be 0.</span></span></td>
<td><span data-ttu-id="c6540-177">Non utilisé dans cette version.</span><span class="sxs-lookup"><span data-stu-id="c6540-177">Not used in this release.</span></span> <span data-ttu-id="c6540-178">Doit correspondre à 0.</span><span class="sxs-lookup"><span data-stu-id="c6540-178">Should be 0.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6540-179">ViewType</span><span class="sxs-lookup"><span data-stu-id="c6540-179">ViewType</span></span></td>
<td><span data-ttu-id="c6540-180">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-180">Yes</span></span></td>
<td><span data-ttu-id="c6540-181">Chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="c6540-181">Unicode string.</span></span> <span data-ttu-id="c6540-182">Format : [I | T | R | L | O] exemple : T</span><span class="sxs-lookup"><span data-stu-id="c6540-182">Format: [I|T|R|L|O]Example: T</span></span><br/></td>
<td><span data-ttu-id="c6540-183">Indique le type d’affichage à utiliser pour la liste.</span><span class="sxs-lookup"><span data-stu-id="c6540-183">Indicates the view type to use for the list.</span></span>
<ul>
<li><span data-ttu-id="c6540-184">I = icône</span><span class="sxs-lookup"><span data-stu-id="c6540-184">I = Icon</span></span></li>
<li><span data-ttu-id="c6540-185">T = vignette</span><span class="sxs-lookup"><span data-stu-id="c6540-185">T = Tile</span></span></li>
<li><span data-ttu-id="c6540-186">R = rapport</span><span class="sxs-lookup"><span data-stu-id="c6540-186">R = Report</span></span></li>
<li><span data-ttu-id="c6540-187">L = liste</span><span class="sxs-lookup"><span data-stu-id="c6540-187">L = List</span></span></li>
<li><span data-ttu-id="c6540-188">O = liste triée</span><span class="sxs-lookup"><span data-stu-id="c6540-188">O = Ordered List</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6540-189">ViewImageSize</span><span class="sxs-lookup"><span data-stu-id="c6540-189">ViewImageSize</span></span></td>
<td><span data-ttu-id="c6540-190">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-190">Yes</span></span></td>
<td><span data-ttu-id="c6540-191">Entier non négatif. Exemple : 180</span><span class="sxs-lookup"><span data-stu-id="c6540-191">Non-negative integer.Example: 180</span></span><br/></td>
<td><span data-ttu-id="c6540-192">Taille à laquelle l’image de liste est affichée.</span><span class="sxs-lookup"><span data-stu-id="c6540-192">The size at which the list image is displayed.</span></span> <span data-ttu-id="c6540-193">Si la valeur est 0, la taille est déterminée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c6540-193">If 0, size is determined automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6540-194">GroupBy</span><span class="sxs-lookup"><span data-stu-id="c6540-194">GroupBy</span></span></td>
<td><span data-ttu-id="c6540-195">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-195">Yes</span></span></td>
<td><span data-ttu-id="c6540-196">Chaîne Unicode. Format : [-| P | A | C | R | E</span><span class="sxs-lookup"><span data-stu-id="c6540-196">Unicode string.Format: [-|P|A|C|R|D]</span></span><br/> <span data-ttu-id="c6540-197">Exemple : P</span><span class="sxs-lookup"><span data-stu-id="c6540-197">Example: P</span></span><br/></td>
<td><span data-ttu-id="c6540-198">Indique quel champ est utilisé pour regrouper les éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="c6540-198">Indicates what field is used to group the items in the list.</span></span>
<ul>
<li><span data-ttu-id="c6540-199">- = Automatique</span><span class="sxs-lookup"><span data-stu-id="c6540-199">- = Automatic</span></span></li>
<li><span data-ttu-id="c6540-200">P = l’intervenant</span><span class="sxs-lookup"><span data-stu-id="c6540-200">P = Performer</span></span></li>
<li><span data-ttu-id="c6540-201">A = album</span><span class="sxs-lookup"><span data-stu-id="c6540-201">A = Album</span></span></li>
<li><span data-ttu-id="c6540-202">C = compositeur</span><span class="sxs-lookup"><span data-stu-id="c6540-202">C = Composer</span></span></li>
<li><span data-ttu-id="c6540-203">R = évaluation</span><span class="sxs-lookup"><span data-stu-id="c6540-203">R = Rating</span></span></li>
<li><span data-ttu-id="c6540-204">D = date</span><span class="sxs-lookup"><span data-stu-id="c6540-204">D = Date</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6540-205">ListItemsAreDynamic</span><span class="sxs-lookup"><span data-stu-id="c6540-205">ListItemsAreDynamic</span></span></td>
<td><span data-ttu-id="c6540-206">Oui</span><span class="sxs-lookup"><span data-stu-id="c6540-206">Yes</span></span></td>
<td><span data-ttu-id="c6540-207">Propriété booléenne.</span><span class="sxs-lookup"><span data-stu-id="c6540-207">Boolean.</span></span> <span data-ttu-id="c6540-208">Peut avoir la valeur 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="c6540-208">Can be 0 or 1.</span></span></td>
<td><span data-ttu-id="c6540-209">Indique si la liste est générée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="c6540-209">Indicates whether the list is generated dynamically.</span></span> <span data-ttu-id="c6540-210">Les listes dynamiques n’ont pas d’éléments dans listitem.csv.</span><span class="sxs-lookup"><span data-stu-id="c6540-210">Dynamic lists do not have items in listitem.csv.</span></span> <span data-ttu-id="c6540-211">Si une liste est marquée comme dynamique, ses éléments sont fournis par <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner :: GetListContents</a></span><span class="sxs-lookup"><span data-stu-id="c6540-211">If a list is marked as dynamic, its items are provided by <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





