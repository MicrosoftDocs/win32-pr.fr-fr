---
title: À propos des métadonnées
description: À propos des métadonnées
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Lecteur Windows Media, métadonnées
- métadonnées, à propos de
- métadonnées, attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309301"
---
# <a name="about-the-metadata"></a><span data-ttu-id="29d69-106">À propos des métadonnées</span><span class="sxs-lookup"><span data-stu-id="29d69-106">About the Metadata</span></span>

<span data-ttu-id="29d69-107">Le lecteur Windows Media 10 ou une version ultérieure tente de synchroniser les attributs de métadonnées suivants.</span><span class="sxs-lookup"><span data-stu-id="29d69-107">Windows Media Player 10 or later attempts to synchronize the following metadata attributes.</span></span>



| <span data-ttu-id="29d69-108">Attribut Player</span><span class="sxs-lookup"><span data-stu-id="29d69-108">Player attribute</span></span> | <span data-ttu-id="29d69-109">WMDM constante globale)</span><span class="sxs-lookup"><span data-stu-id="29d69-109">WMDM global constant</span></span>  | <span data-ttu-id="29d69-110">Description</span><span class="sxs-lookup"><span data-stu-id="29d69-110">Description</span></span>                                                                                                 | <span data-ttu-id="29d69-111">Version requise</span><span class="sxs-lookup"><span data-stu-id="29d69-111">Required version</span></span>                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="29d69-112">AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="29d69-112">AlbumArtist</span></span>      | <span data-ttu-id="29d69-113">\_wszWMDMAlbumArtist g</span><span class="sxs-lookup"><span data-stu-id="29d69-113">g\_wszWMDMAlbumArtist</span></span> | <span data-ttu-id="29d69-114">**Chaîne** terminée par le caractère NULL contenant le nom de l’artiste principal de l’album.</span><span class="sxs-lookup"><span data-stu-id="29d69-114">Null-terminated **string** containing the name of the primary artist for the album.</span></span>                         | <span data-ttu-id="29d69-115">Lecteur Windows Media 11 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-115">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="29d69-116">Album</span><span class="sxs-lookup"><span data-stu-id="29d69-116">Album</span></span>            | <span data-ttu-id="29d69-117">\_wszWMDMAlbumTitle g</span><span class="sxs-lookup"><span data-stu-id="29d69-117">g\_wszWMDMAlbumTitle</span></span>  | <span data-ttu-id="29d69-118">**Chaîne** terminée par le caractère null qui contient le titre de l’album sur lequel le contenu a été publié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="29d69-118">Null-terminated **string** containing the title of the album on which the content was originally released.</span></span>  | <span data-ttu-id="29d69-119">Lecteur Windows Media 11 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-119">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="29d69-120">Auteur</span><span class="sxs-lookup"><span data-stu-id="29d69-120">Author</span></span>           | <span data-ttu-id="29d69-121">\_wszWMDMAuthor g</span><span class="sxs-lookup"><span data-stu-id="29d69-121">g\_wszWMDMAuthor</span></span>      | <span data-ttu-id="29d69-122">**Chaîne** terminée par le caractère NULL contenant le nom de l’artiste multimédia ou de l’acteur associé au contenu.</span><span class="sxs-lookup"><span data-stu-id="29d69-122">Null-terminated **string** containing the name of the media artist or actor associated with the content.</span></span>    | <span data-ttu-id="29d69-123">Lecteur Windows Media 11 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-123">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="29d69-124">BuyNow</span><span class="sxs-lookup"><span data-stu-id="29d69-124">BuyNow</span></span>           | <span data-ttu-id="29d69-125">\_wszWMDMBuyNow g</span><span class="sxs-lookup"><span data-stu-id="29d69-125">g\_wszWMDMBuyNow</span></span>      | <span data-ttu-id="29d69-126">**Valeur booléenne** indiquant si l’utilisateur a choisi d’acheter le contenu.</span><span class="sxs-lookup"><span data-stu-id="29d69-126">**Boolean** indicating whether the user has chosen to purchase the content.</span></span>                                 | <span data-ttu-id="29d69-127">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-127">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="29d69-128">WM/genre</span><span class="sxs-lookup"><span data-stu-id="29d69-128">WM/Genre</span></span>         | <span data-ttu-id="29d69-129">\_wszWMDMGenre g</span><span class="sxs-lookup"><span data-stu-id="29d69-129">g\_wszWMDMGenre</span></span>       | <span data-ttu-id="29d69-130">**Chaîne** terminée par le caractère null qui contient le genre du contenu.</span><span class="sxs-lookup"><span data-stu-id="29d69-130">Null-terminated **string** containing the genre of the content.</span></span>                                             | <span data-ttu-id="29d69-131">Lecteur Windows Media 11 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-131">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="29d69-132">UserPlayCount</span><span class="sxs-lookup"><span data-stu-id="29d69-132">UserPlayCount</span></span>    | <span data-ttu-id="29d69-133">\_wszWMDMPlayCount g</span><span class="sxs-lookup"><span data-stu-id="29d69-133">g\_wszWMDMPlayCount</span></span>   | <span data-ttu-id="29d69-134">**Valeur DWORD** qui contient le nombre de fois que l’utilisateur a lu le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="29d69-134">**DWORD** containing the number of times the user has played the digital media file.</span></span>                        | <span data-ttu-id="29d69-135">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-135">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="29d69-136">ReleaseDate</span><span class="sxs-lookup"><span data-stu-id="29d69-136">ReleaseDate</span></span>      | <span data-ttu-id="29d69-137">\_wszWMDMYear g</span><span class="sxs-lookup"><span data-stu-id="29d69-137">g\_wszWMDMYear</span></span>        | <span data-ttu-id="29d69-138">Date de la version d’origine de l’élément.</span><span class="sxs-lookup"><span data-stu-id="29d69-138">The date of the original release of the item.</span></span>                                                               | <span data-ttu-id="29d69-139">Lecteur Windows Media 11 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-139">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="29d69-140">Intitulé</span><span class="sxs-lookup"><span data-stu-id="29d69-140">Title</span></span>            | <span data-ttu-id="29d69-141">\_wszWMDMTitle g</span><span class="sxs-lookup"><span data-stu-id="29d69-141">g\_wszWMDMTitle</span></span>       | <span data-ttu-id="29d69-142">**Chaîne** terminée par le caractère null qui contient le titre.</span><span class="sxs-lookup"><span data-stu-id="29d69-142">Null-terminated **string** containing the title.</span></span>                                                            | <span data-ttu-id="29d69-143">Lecteur Windows Media 11 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-143">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="29d69-144">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="29d69-144">WM/TrackNumber</span></span>   | <span data-ttu-id="29d69-145">\_wszWMDMTrack g</span><span class="sxs-lookup"><span data-stu-id="29d69-145">g\_wszWMDMTrack</span></span>       | <span data-ttu-id="29d69-146">**Valeur DWORD** qui contient le numéro de suivi de l’élément sur l’album sur lequel il a été publié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="29d69-146">**DWORD** containing the track number of the item on the album on which it was originally released.</span></span>         | <span data-ttu-id="29d69-147">Lecteur Windows Media 11 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-147">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="29d69-148">UserRating</span><span class="sxs-lookup"><span data-stu-id="29d69-148">UserRating</span></span>       | <span data-ttu-id="29d69-149">\_wszWMDMUserRating g</span><span class="sxs-lookup"><span data-stu-id="29d69-149">g\_wszWMDMUserRating</span></span>  | <span data-ttu-id="29d69-150">**DWORD** contenant une valeur qui représente l’évaluation de l’étoile spécifiée par l’utilisateur pour le fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="29d69-150">**DWORD** containing a value that represents the star rating the user specified for the digital media file.</span></span> | <span data-ttu-id="29d69-151">Lecteur Windows Media 10 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="29d69-151">Windows Media Player 10 or later.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="29d69-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29d69-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29d69-153">**Extensions d’appareil pour le transfert de métadonnées accéléré**</span><span class="sxs-lookup"><span data-stu-id="29d69-153">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




