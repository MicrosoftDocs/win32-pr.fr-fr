---
title: PLAYLIST. colonnes
description: L’attribut Columns définit les colonnes qui apparaissent dans l’élément PLAYLIST.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- SÉLECTION. colonnes lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530441"
---
# <a name="playlistcolumns"></a><span data-ttu-id="d2f56-104">PLAYLIST. colonnes</span><span class="sxs-lookup"><span data-stu-id="d2f56-104">PLAYLIST.columns</span></span>

<span data-ttu-id="d2f56-105">L’attribut **Columns** définit les colonnes qui apparaissent dans l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="d2f56-105">The **columns** attribute defines the columns that appear in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.columns
```

## <a name="possible-values"></a><span data-ttu-id="d2f56-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d2f56-106">Possible Values</span></span>

<span data-ttu-id="d2f56-107">Cet attribut est une **chaîne** en lecture/écriture au format suivant :</span><span class="sxs-lookup"><span data-stu-id="d2f56-107">This attribute is a read/write **String** in the following format:</span></span>

<span data-ttu-id="d2f56-108">nom de la base de noms \_ = nom convivial ; nom de la base de noms \_ \_ = \_ nom convivial ;</span><span class="sxs-lookup"><span data-stu-id="d2f56-108">DB\_NAME=FRIENDLY\_NAME;DB\_NAME=FRIENDLY\_NAME;</span></span>

<span data-ttu-id="d2f56-109">\_Nom convivial est la valeur indiquée dans l’en-tête de colonne de l’élément playlist et le nom de la base de \_ code est une valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d2f56-109">FRIENDLY\_NAME is the value shown in the column header of the PLAYLIST element, and DB\_NAME is a value from the following table.</span></span> <span data-ttu-id="d2f56-110">Notez qu’un élément de sélection peut être un élément multimédia de la bibliothèque ou d’un CD, ou qu’il peut s’agir d’une autre **sélection** créée par l’utilisateur ou effectuée à partir d’un CD.</span><span class="sxs-lookup"><span data-stu-id="d2f56-110">Note that a Playlist item might be a media item from the library or from a CD, or it might be another **Playlist** that is either user-created or taken from a CD.</span></span> <span data-ttu-id="d2f56-111">Certaines colonnes sont valides uniquement avec certains éléments de playlist comme indiqué dans la colonne Description.</span><span class="sxs-lookup"><span data-stu-id="d2f56-111">Some columns are valid only with certain Playlist items as indicated in the Description column.</span></span>



| <span data-ttu-id="d2f56-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f56-112">Value</span></span>             | <span data-ttu-id="d2f56-113">Description</span><span class="sxs-lookup"><span data-stu-id="d2f56-113">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f56-114">Album</span><span class="sxs-lookup"><span data-stu-id="d2f56-114">Album</span></span>             | <span data-ttu-id="d2f56-115">Nom de l’album.</span><span class="sxs-lookup"><span data-stu-id="d2f56-115">The name of the album.</span></span> <span data-ttu-id="d2f56-116">Utilisé avec les éléments multimédias uniquement.</span><span class="sxs-lookup"><span data-stu-id="d2f56-116">Used with media items only.</span></span>                                                                      |
| <span data-ttu-id="d2f56-117">Peinture</span><span class="sxs-lookup"><span data-stu-id="d2f56-117">Artist</span></span>            | <span data-ttu-id="d2f56-118">Nom de l’artiste.</span><span class="sxs-lookup"><span data-stu-id="d2f56-118">The name of the artist.</span></span> <span data-ttu-id="d2f56-119">Non utilisé avec les sélections créées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-119">Not used with user-created playlists.</span></span>                                                           |
| <span data-ttu-id="d2f56-120">Auteur</span><span class="sxs-lookup"><span data-stu-id="d2f56-120">Author</span></span>            | <span data-ttu-id="d2f56-121">Nom de l’artiste.</span><span class="sxs-lookup"><span data-stu-id="d2f56-121">The name of the artist.</span></span>                                                                                                 |
| <span data-ttu-id="d2f56-122">Bitrate</span><span class="sxs-lookup"><span data-stu-id="d2f56-122">Bitrate</span></span>           | <span data-ttu-id="d2f56-123">Vitesse de transmission du contenu.</span><span class="sxs-lookup"><span data-stu-id="d2f56-123">The bit rate of the content.</span></span> <span data-ttu-id="d2f56-124">Utilisé uniquement avec les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d2f56-124">Used only with media items from the library.</span></span>                                               |
| <span data-ttu-id="d2f56-125">CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="d2f56-125">CDTrackEnabled</span></span>    | <span data-ttu-id="d2f56-126">Indique si la piste CD est activée.</span><span class="sxs-lookup"><span data-stu-id="d2f56-126">Indicates whether the CD track is enabled.</span></span> <span data-ttu-id="d2f56-127">Utilisé uniquement avec les éléments de support CD.</span><span class="sxs-lookup"><span data-stu-id="d2f56-127">Used only with CD media items.</span></span>                                               |
| <span data-ttu-id="d2f56-128">Activée</span><span class="sxs-lookup"><span data-stu-id="d2f56-128">Checked</span></span>           | <span data-ttu-id="d2f56-129">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-129">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="d2f56-130">copyright</span><span class="sxs-lookup"><span data-stu-id="d2f56-130">Copyright</span></span>         | <span data-ttu-id="d2f56-131">Copyright de la sélection.</span><span class="sxs-lookup"><span data-stu-id="d2f56-131">The copyright of the playlist.</span></span> <span data-ttu-id="d2f56-132">Non utilisé avec les sélections de CD ou les éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="d2f56-132">Not used with CD playlists or media items.</span></span>                                               |
| <span data-ttu-id="d2f56-133">CreationDate</span><span class="sxs-lookup"><span data-stu-id="d2f56-133">CreationDate</span></span>      | <span data-ttu-id="d2f56-134">Date et heure de création de l’entrée dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d2f56-134">The date and time that the entry in the library was created.</span></span> <span data-ttu-id="d2f56-135">Utilisé uniquement avec les éléments de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d2f56-135">Used only with items from the library.</span></span>                     |
| <span data-ttu-id="d2f56-136">DigitallySecure</span><span class="sxs-lookup"><span data-stu-id="d2f56-136">DigitallySecure</span></span>   | <span data-ttu-id="d2f56-137">Indique si l’élément est protégé par le gestionnaire de droits Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d2f56-137">Indicates whether the item is protected with Windows Media Rights Manager.</span></span> <span data-ttu-id="d2f56-138">Utilisé uniquement avec les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d2f56-138">Used only with media items from the library.</span></span> |
| <span data-ttu-id="d2f56-139">Duration</span><span class="sxs-lookup"><span data-stu-id="d2f56-139">Duration</span></span>          | <span data-ttu-id="d2f56-140">Durée de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="d2f56-140">The duration of the media item.</span></span>                                                                                         |
| <span data-ttu-id="d2f56-141">FileType</span><span class="sxs-lookup"><span data-stu-id="d2f56-141">FileType</span></span>          | <span data-ttu-id="d2f56-142">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-142">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="d2f56-143">Genre</span><span class="sxs-lookup"><span data-stu-id="d2f56-143">Genre</span></span>             | <span data-ttu-id="d2f56-144">Genre de la sélection.</span><span class="sxs-lookup"><span data-stu-id="d2f56-144">The genre of the playlist.</span></span> <span data-ttu-id="d2f56-145">Non utilisé avec les playlists des CDs.</span><span class="sxs-lookup"><span data-stu-id="d2f56-145">Not used with playlists from CDs.</span></span>                                                            |
| <span data-ttu-id="d2f56-146">MediaAttribute</span><span class="sxs-lookup"><span data-stu-id="d2f56-146">MediaAttribute</span></span>    | <span data-ttu-id="d2f56-147">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-147">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="d2f56-148">MediaType</span><span class="sxs-lookup"><span data-stu-id="d2f56-148">MediaType</span></span>         | <span data-ttu-id="d2f56-149">Type de l’élément multimédia (audio ou vidéo).</span><span class="sxs-lookup"><span data-stu-id="d2f56-149">The type of the media item (audio or video).</span></span>                                                                            |
| <span data-ttu-id="d2f56-150">Sous-dataSource</span><span class="sxs-lookup"><span data-stu-id="d2f56-150">MetadataSource</span></span>    | <span data-ttu-id="d2f56-151">Source des métadonnées de cette piste de CD (AMG, WindowsMedia.com, etc.).</span><span class="sxs-lookup"><span data-stu-id="d2f56-151">The source of the metadata for this CD track (AMG, WindowsMedia.com, and so on).</span></span> <span data-ttu-id="d2f56-152">Utilisé uniquement avec les éléments de support CD.</span><span class="sxs-lookup"><span data-stu-id="d2f56-152">Used only with CD media items.</span></span>         |
| <span data-ttu-id="d2f56-153">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="d2f56-153">ModifiedBy</span></span>        | <span data-ttu-id="d2f56-154">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-154">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="d2f56-155">Nom</span><span class="sxs-lookup"><span data-stu-id="d2f56-155">Name</span></span>              | <span data-ttu-id="d2f56-156">Nom de la sélection.</span><span class="sxs-lookup"><span data-stu-id="d2f56-156">The name of the playlist.</span></span>                                                                                               |
| <span data-ttu-id="d2f56-157">OriginalIndex</span><span class="sxs-lookup"><span data-stu-id="d2f56-157">OriginalIndex</span></span>     | <span data-ttu-id="d2f56-158">Le cas échéant, l’identificateur de piste CD correspondant.</span><span class="sxs-lookup"><span data-stu-id="d2f56-158">If applicable, the corresponding CD track identifier.</span></span> <span data-ttu-id="d2f56-159">Utilisé uniquement avec les éléments de support CD.</span><span class="sxs-lookup"><span data-stu-id="d2f56-159">Used only with CD media items.</span></span>                                    |
| <span data-ttu-id="d2f56-160">PlayCount</span><span class="sxs-lookup"><span data-stu-id="d2f56-160">PlayCount</span></span>         | <span data-ttu-id="d2f56-161">Nombre de fois où le contenu a été lu jusqu’à la fin.</span><span class="sxs-lookup"><span data-stu-id="d2f56-161">The number of times the content has been played through to the end.</span></span> <span data-ttu-id="d2f56-162">Utilisé uniquement avec les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d2f56-162">Used only with media items from the library.</span></span>        |
| <span data-ttu-id="d2f56-163">PlaylistAttribute</span><span class="sxs-lookup"><span data-stu-id="d2f56-163">PlaylistAttribute</span></span> | <span data-ttu-id="d2f56-164">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-164">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="d2f56-165">Rating</span><span class="sxs-lookup"><span data-stu-id="d2f56-165">Rating</span></span>            | <span data-ttu-id="d2f56-166">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-166">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="d2f56-167">SourceURL</span><span class="sxs-lookup"><span data-stu-id="d2f56-167">SourceURL</span></span>         | <span data-ttu-id="d2f56-168">Chemin d’accès ou URL du contenu.</span><span class="sxs-lookup"><span data-stu-id="d2f56-168">The path or URL to the content.</span></span> <span data-ttu-id="d2f56-169">Utilisé uniquement avec les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d2f56-169">Used only with media items from the library.</span></span>                                            |
| <span data-ttu-id="d2f56-170">Statut</span><span class="sxs-lookup"><span data-stu-id="d2f56-170">Status</span></span>            | <span data-ttu-id="d2f56-171">État de copie d’une piste de CD en cours de copie.</span><span class="sxs-lookup"><span data-stu-id="d2f56-171">The copying status of a CD track being copied.</span></span> <span data-ttu-id="d2f56-172">Utilisé uniquement avec les éléments de support CD.</span><span class="sxs-lookup"><span data-stu-id="d2f56-172">Used only with CD media items.</span></span>                                           |
| <span data-ttu-id="d2f56-173">Style</span><span class="sxs-lookup"><span data-stu-id="d2f56-173">Style</span></span>             | <span data-ttu-id="d2f56-174">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-174">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="d2f56-175">Table des matières</span><span class="sxs-lookup"><span data-stu-id="d2f56-175">TOC</span></span>               | <span data-ttu-id="d2f56-176">Le cas échéant, l’identificateur de la table des matières du CD correspondant.</span><span class="sxs-lookup"><span data-stu-id="d2f56-176">If applicable, the corresponding CD Table of Contents Identifier.</span></span> <span data-ttu-id="d2f56-177">Non utilisé avec les sélections créées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2f56-177">Not used with user-created playlists.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="d2f56-178">Notes</span><span class="sxs-lookup"><span data-stu-id="d2f56-178">Remarks</span></span>

<span data-ttu-id="d2f56-179">Si l’une des colonnes n’existe pas dans la bibliothèque, elle est laissée vide.</span><span class="sxs-lookup"><span data-stu-id="d2f56-179">If one of the columns does not exist in the library, it is left blank.</span></span>

<span data-ttu-id="d2f56-180">Vous pouvez spécifier au maximum 31 colonnes.</span><span class="sxs-lookup"><span data-stu-id="d2f56-180">A maximum of 31 columns may be specified.</span></span>

<span data-ttu-id="d2f56-181">Si vous spécifiez une colonne dupliquée, les données de la première colonne sont alignées à gauche, mais toutes les autres colonnes dupliquées sont alignées à droite.</span><span class="sxs-lookup"><span data-stu-id="d2f56-181">If you specify a duplicate column, the data in the first column will be left-aligned but all other duplicate columns will be right-aligned.</span></span> <span data-ttu-id="d2f56-182">Par exemple, si vous avez deux colonnes de durée, les données sont alignées à gauche dans le premier et aligné à droite dans la seconde.</span><span class="sxs-lookup"><span data-stu-id="d2f56-182">For example, if you have two duration columns, the data will be left-aligned in the first and right-aligned in the second.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f56-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2f56-183">Requirements</span></span>



| <span data-ttu-id="d2f56-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2f56-184">Requirement</span></span> | <span data-ttu-id="d2f56-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f56-185">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d2f56-186">Version</span><span class="sxs-lookup"><span data-stu-id="d2f56-186">Version</span></span><br/> | <span data-ttu-id="d2f56-187">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="d2f56-187">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2f56-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2f56-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f56-189">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="d2f56-189">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="d2f56-190">**PLAYLIST. columnsVisible**</span><span class="sxs-lookup"><span data-stu-id="d2f56-190">**PLAYLIST.columnsVisible**</span></span>](playlist-columnsvisible.md)
</dt> </dl>

 

 





