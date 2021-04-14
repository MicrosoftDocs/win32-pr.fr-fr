---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player Online stores, track.csv
- magasins en ligne, track.csv
- tapez 1 magasins en ligne, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310370"
---
# <a name="trackcsv"></a><span data-ttu-id="dc199-107">track.csv</span><span class="sxs-lookup"><span data-stu-id="dc199-107">track.csv</span></span>

<span data-ttu-id="dc199-108">Ce fichier contient une entrée pour chaque piste dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="dc199-108">This file contains an entry for each track in the catalog.</span></span> <span data-ttu-id="dc199-109">Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="dc199-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="dc199-110">Les champs doivent apparaître dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="dc199-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="dc199-111">La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="dc199-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="dc199-112">Elle ne fait pas référence au type de données du contenu.</span><span class="sxs-lookup"><span data-stu-id="dc199-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="dc199-113">Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.</span><span class="sxs-lookup"><span data-stu-id="dc199-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc199-114">Champ</span><span class="sxs-lookup"><span data-stu-id="dc199-114">Field</span></span></th>
<th><span data-ttu-id="dc199-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dc199-115">Required</span></span></th>
<th><span data-ttu-id="dc199-116">Format</span><span class="sxs-lookup"><span data-stu-id="dc199-116">Format</span></span></th>
<th><span data-ttu-id="dc199-117">Description</span><span class="sxs-lookup"><span data-stu-id="dc199-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc199-118">TrackID tel</span><span class="sxs-lookup"><span data-stu-id="dc199-118">TrackID</span></span></td>
<td><span data-ttu-id="dc199-119">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-119">Yes</span></span></td>
<td><span data-ttu-id="dc199-120">Entier non négatif. Exemple : 32789</span><span class="sxs-lookup"><span data-stu-id="dc199-120">Non-negative integer.Example: 32789</span></span><br/></td>
<td><span data-ttu-id="dc199-121">Identificateur unique fourni par le fournisseur de contenu.</span><span class="sxs-lookup"><span data-stu-id="dc199-121">Unique identifier provided by the content provider.</span></span> <span data-ttu-id="dc199-122">Doit être inférieur à 2 ^ 32. Conseil en matière de performances : si les ID affectés aux pistes du même album sont numérotés consécutivement, la compression du catalogue est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="dc199-122">Must be less than 2^32.Performance tip: If the IDs assigned to tracks from the same album are numbered consecutively, catalog compression will be more efficient.</span></span> <span data-ttu-id="dc199-123">Toutefois, la numérotation consécutive des suivis d’albums n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dc199-123">However, consecutive numbering of album tracks is not required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc199-124">TrackTitle</span><span class="sxs-lookup"><span data-stu-id="dc199-124">TrackTitle</span></span></td>
<td><span data-ttu-id="dc199-125">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-125">Yes</span></span></td>
<td><span data-ttu-id="dc199-126">Chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="dc199-126">Unicode string.</span></span> <span data-ttu-id="dc199-127">Exemple : Raygun Robbers’Blues</span><span class="sxs-lookup"><span data-stu-id="dc199-127">Example: Raygun Robbers' Blues</span></span></td>
<td><span data-ttu-id="dc199-128">Nom de la piste.</span><span class="sxs-lookup"><span data-stu-id="dc199-128">Name of the track.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc199-129">Duration</span><span class="sxs-lookup"><span data-stu-id="dc199-129">Duration</span></span></td>
<td><span data-ttu-id="dc199-130">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-130">Yes</span></span></td>
<td><span data-ttu-id="dc199-131">Entier non négatif. Exemple : 543</span><span class="sxs-lookup"><span data-stu-id="dc199-131">Non-negative integer.Example: 543</span></span><br/></td>
<td><span data-ttu-id="dc199-132">Durée de la piste en secondes.</span><span class="sxs-lookup"><span data-stu-id="dc199-132">Duration of the track in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc199-133">TrackNumber</span><span class="sxs-lookup"><span data-stu-id="dc199-133">TrackNumber</span></span></td>
<td><span data-ttu-id="dc199-134">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-134">Yes</span></span></td>
<td><span data-ttu-id="dc199-135">Entier non négatif. Exemple : 7</span><span class="sxs-lookup"><span data-stu-id="dc199-135">Non-negative integer.Example: 7</span></span><br/></td>
<td><span data-ttu-id="dc199-136">Numéro de piste sur l’album de la piste.</span><span class="sxs-lookup"><span data-stu-id="dc199-136">Track number on the track's album.</span></span> <span data-ttu-id="dc199-137">Le suivi des nombres commence à 1 et augmente sur les jeux de disques.</span><span class="sxs-lookup"><span data-stu-id="dc199-137">Track numbers begin at 1 and increase across disc sets.</span></span> <span data-ttu-id="dc199-138">Le numéro de piste doit être inférieur à 256.</span><span class="sxs-lookup"><span data-stu-id="dc199-138">The track number must be less than 256.</span></span> <span data-ttu-id="dc199-139">Un numéro de piste supérieur ou égal à 256 entraîne un comportement inattendu dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dc199-139">A track number greater than or equal to 256 will cause unexpected behavior in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc199-140">TrackPrice</span><span class="sxs-lookup"><span data-stu-id="dc199-140">TrackPrice</span></span></td>
<td><span data-ttu-id="dc199-141">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-141">Yes</span></span></td>
<td><span data-ttu-id="dc199-142">Chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="dc199-142">Unicode string.</span></span> <span data-ttu-id="dc199-143">Exemple : $0,99.</span><span class="sxs-lookup"><span data-stu-id="dc199-143">Example: $0.99.</span></span></td>
<td><span data-ttu-id="dc199-144">Suivre le prix.</span><span class="sxs-lookup"><span data-stu-id="dc199-144">Track price.</span></span> <span data-ttu-id="dc199-145">Le symbole monétaire doit être inclus.</span><span class="sxs-lookup"><span data-stu-id="dc199-145">The currency symbol should be included.</span></span> <span data-ttu-id="dc199-146">La chaîne vide, 0 et-ont une signification particulière.</span><span class="sxs-lookup"><span data-stu-id="dc199-146">The empty string, 0, and - have special meaning.</span></span> <span data-ttu-id="dc199-147">Une chaîne vide indique que le prix est inconnu.</span><span class="sxs-lookup"><span data-stu-id="dc199-147">An empty string indicates that the price is unknown.</span></span> <span data-ttu-id="dc199-148">Un zéro dans ce champ signifie que la piste est libre et un trait d’Union (-) indique que la piste ne peut pas être achetée.</span><span class="sxs-lookup"><span data-stu-id="dc199-148">A zero in this field means the track is free, and a hyphen (-) indicates that the track cannot be bought.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc199-149">CanStream</span><span class="sxs-lookup"><span data-stu-id="dc199-149">CanStream</span></span></td>
<td><span data-ttu-id="dc199-150">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-150">Yes</span></span></td>
<td><span data-ttu-id="dc199-151">Propriété booléenne.</span><span class="sxs-lookup"><span data-stu-id="dc199-151">Boolean.</span></span> <span data-ttu-id="dc199-152">Peut être 0 ou 1. exemple : 0</span><span class="sxs-lookup"><span data-stu-id="dc199-152">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="dc199-153">Indique si la piste peut être diffusée en continu.</span><span class="sxs-lookup"><span data-stu-id="dc199-153">Indicates whether the track can be streamed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc199-154">CanDownload</span><span class="sxs-lookup"><span data-stu-id="dc199-154">CanDownload</span></span></td>
<td><span data-ttu-id="dc199-155">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-155">Yes</span></span></td>
<td><span data-ttu-id="dc199-156">Propriété booléenne.</span><span class="sxs-lookup"><span data-stu-id="dc199-156">Boolean.</span></span> <span data-ttu-id="dc199-157">Peut être 0 ou 1. exemple : 0</span><span class="sxs-lookup"><span data-stu-id="dc199-157">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="dc199-158">Indique si la piste peut être téléchargée.</span><span class="sxs-lookup"><span data-stu-id="dc199-158">Indicates whether the track can be downloaded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc199-159">HasPreviewClip</span><span class="sxs-lookup"><span data-stu-id="dc199-159">HasPreviewClip</span></span></td>
<td><span data-ttu-id="dc199-160">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-160">Yes</span></span></td>
<td><span data-ttu-id="dc199-161">Propriété booléenne.</span><span class="sxs-lookup"><span data-stu-id="dc199-161">Boolean.</span></span> <span data-ttu-id="dc199-162">Peut être 0 ou 1. exemple : 0</span><span class="sxs-lookup"><span data-stu-id="dc199-162">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="dc199-163">Indique si la piste a un clip d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="dc199-163">Indicates whether the track has a preview clip.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc199-164">HasVideoClip</span><span class="sxs-lookup"><span data-stu-id="dc199-164">HasVideoClip</span></span></td>
<td><span data-ttu-id="dc199-165">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-165">Yes</span></span></td>
<td><span data-ttu-id="dc199-166">Propriété booléenne.</span><span class="sxs-lookup"><span data-stu-id="dc199-166">Boolean.</span></span> <span data-ttu-id="dc199-167">Peut être 0 ou 1. exemple : 0</span><span class="sxs-lookup"><span data-stu-id="dc199-167">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="dc199-168">Indique si la piste a un clip vidéo.</span><span class="sxs-lookup"><span data-stu-id="dc199-168">Indicates whether the track has a video clip.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc199-169">ParentalRating</span><span class="sxs-lookup"><span data-stu-id="dc199-169">ParentalRating</span></span></td>
<td><span data-ttu-id="dc199-170">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-170">Yes</span></span></td>
<td><span data-ttu-id="dc199-171">Énumération.</span><span class="sxs-lookup"><span data-stu-id="dc199-171">Enumeration.</span></span> <span data-ttu-id="dc199-172">Peut être N, E ou C. exemple : N</span><span class="sxs-lookup"><span data-stu-id="dc199-172">Can be N, E, or C.Example: N</span></span><br/></td>
<td><span data-ttu-id="dc199-173">Indique l’évaluation de l’avis parental.</span><span class="sxs-lookup"><span data-stu-id="dc199-173">Indicates the Parental Advisory Rating.</span></span> <span data-ttu-id="dc199-174">Les valeurs N, E et C sont pour normal, Explicit et Clean.</span><span class="sxs-lookup"><span data-stu-id="dc199-174">The values N, E, and C stand for Normal, Explicit, and Clean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc199-175">LinkedAlbumID</span><span class="sxs-lookup"><span data-stu-id="dc199-175">LinkedAlbumID</span></span></td>
<td><span data-ttu-id="dc199-176">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-176">Yes</span></span></td>
<td><span data-ttu-id="dc199-177">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="dc199-177">Non-negative integer.</span></span> <span data-ttu-id="dc199-178">Doit être l’ID d’un album.</span><span class="sxs-lookup"><span data-stu-id="dc199-178">Must be the ID of an Album.</span></span> <span data-ttu-id="dc199-179">Exemple : 32423</span><span class="sxs-lookup"><span data-stu-id="dc199-179">Example: 32423</span></span></td>
<td><span data-ttu-id="dc199-180">ID de l’album qui contient cette piste.</span><span class="sxs-lookup"><span data-stu-id="dc199-180">The ID of the album that contains this track.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="dc199-181">Chaque suivi doit appartenir à un album.</span><span class="sxs-lookup"><span data-stu-id="dc199-181">Every track must belong to an album.</span></span> <span data-ttu-id="dc199-182">Autrement dit, pour chaque piste, le champ LinkedAlbumID doit être égal à l’un des ID d’album figurant dans le fichier album.csv.</span><span class="sxs-lookup"><span data-stu-id="dc199-182">That is, for each track, the LinkedAlbumID field must be equal to one of the album IDs in the album.csv file.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc199-183">LinkedTrackArtist_ArtistIDs</span><span class="sxs-lookup"><span data-stu-id="dc199-183">LinkedTrackArtist_ArtistIDs</span></span></td>
<td><span data-ttu-id="dc199-184">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-184">Yes</span></span></td>
<td><span data-ttu-id="dc199-185">Liste d’entiers.</span><span class="sxs-lookup"><span data-stu-id="dc199-185">List of integers.</span></span> <span data-ttu-id="dc199-186">La liste contient les ID d’artiste, séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="dc199-186">The list contains artist IDs, separated by semicolons.</span></span> <span data-ttu-id="dc199-187">Exemple : 41322 ; 12321 ; 82123 ;</span><span class="sxs-lookup"><span data-stu-id="dc199-187">Example: 41322;12321; 82123;</span></span></td>
<td><span data-ttu-id="dc199-188">Liste d’ID correspondant aux artistes contributeurs.</span><span class="sxs-lookup"><span data-stu-id="dc199-188">A list of IDs corresponding to the contributing artists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc199-189">Composer</span><span class="sxs-lookup"><span data-stu-id="dc199-189">Composer</span></span></td>
<td><span data-ttu-id="dc199-190">Non</span><span class="sxs-lookup"><span data-stu-id="dc199-190">No</span></span></td>
<td><span data-ttu-id="dc199-191">Chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="dc199-191">Unicode string.</span></span> <span data-ttu-id="dc199-192">Exemple : Beethoven</span><span class="sxs-lookup"><span data-stu-id="dc199-192">Example: Beethoven</span></span></td>
<td><span data-ttu-id="dc199-193">Compositeur de la piste. Si le genre de la piste n’a pas le champ HasComposer défini, la valeur du champ compositeur sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="dc199-193">The composer of the track. If the track's genre does not have the HasComposer field set, the value of the Composer field will be ignored.</span></span> <span data-ttu-id="dc199-194">Généralement utilisé uniquement pour les pistes Jazz ou classiques.</span><span class="sxs-lookup"><span data-stu-id="dc199-194">Typically used only for jazz or classical tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc199-195">Popularité</span><span class="sxs-lookup"><span data-stu-id="dc199-195">Popularity</span></span></td>
<td><span data-ttu-id="dc199-196">Oui</span><span class="sxs-lookup"><span data-stu-id="dc199-196">Yes</span></span></td>
<td><span data-ttu-id="dc199-197">Entier non négatif ou float. exemple : 1252,6</span><span class="sxs-lookup"><span data-stu-id="dc199-197">Non-negative integer or Float.Example: 1252.6</span></span><br/></td>
<td><span data-ttu-id="dc199-198">Détermine la position de la piste dans la liste lorsqu’elle est triée par popularité.</span><span class="sxs-lookup"><span data-stu-id="dc199-198">Determines the position of the track in the list when sorted by popularity.</span></span> <span data-ttu-id="dc199-199">Un nombre inférieur indique une popularité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="dc199-199">A lower number indicates higher popularity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc199-200">StarRating</span><span class="sxs-lookup"><span data-stu-id="dc199-200">StarRating</span></span></td>
<td><span data-ttu-id="dc199-201">Non</span><span class="sxs-lookup"><span data-stu-id="dc199-201">No</span></span></td>
<td><span data-ttu-id="dc199-202">Float. exemple : 4,21</span><span class="sxs-lookup"><span data-stu-id="dc199-202">Float.Example: 4.21</span></span><br/></td>
<td><span data-ttu-id="dc199-203">L’évaluation de l’étoile sera arrondie à l’étoile 1/4 la plus proche par le lecteur Windows Media avant d’être affichée dans l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dc199-203">The star rating will be rounded to the nearest 1/4 star by Windows Media Player before being displayed in the Windows Media Player user interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 





