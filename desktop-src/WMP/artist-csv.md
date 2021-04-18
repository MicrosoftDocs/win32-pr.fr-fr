---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player Online stores, artist.csv
- magasins en ligne, artist.csv
- tapez 1 magasins en ligne, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311350"
---
# <a name="artistcsv"></a><span data-ttu-id="6c437-107">artist.csv</span><span class="sxs-lookup"><span data-stu-id="6c437-107">artist.csv</span></span>

<span data-ttu-id="6c437-108">Ce fichier contient une entrée pour chaque artiste dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="6c437-108">This file contains an entry for each artist in the catalog.</span></span> <span data-ttu-id="6c437-109">Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6c437-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="6c437-110">Les champs doivent apparaître dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="6c437-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="6c437-111">Tous les champs de artist.csv sont requis.</span><span class="sxs-lookup"><span data-stu-id="6c437-111">All fields in artist.csv are required.</span></span>

<span data-ttu-id="6c437-112">La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="6c437-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="6c437-113">Elle ne fait pas référence au type de données du contenu.</span><span class="sxs-lookup"><span data-stu-id="6c437-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="6c437-114">Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.</span><span class="sxs-lookup"><span data-stu-id="6c437-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="6c437-115">Champ</span><span class="sxs-lookup"><span data-stu-id="6c437-115">Field</span></span>                  | <span data-ttu-id="6c437-116">Format</span><span class="sxs-lookup"><span data-stu-id="6c437-116">Format</span></span>                                            | <span data-ttu-id="6c437-117">Description</span><span class="sxs-lookup"><span data-stu-id="6c437-117">Description</span></span>                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c437-118">ArtistID</span><span class="sxs-lookup"><span data-stu-id="6c437-118">ArtistID</span></span>               | <span data-ttu-id="6c437-119">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="6c437-119">Non-negative integer.</span></span> <span data-ttu-id="6c437-120">Exemple : 65832</span><span class="sxs-lookup"><span data-stu-id="6c437-120">Example: 65832</span></span>              | <span data-ttu-id="6c437-121">Identificateur unique de l’artiste, unique dans artist.csv.</span><span class="sxs-lookup"><span data-stu-id="6c437-121">Unique identifier for the artist, unique within artist.csv.</span></span> <span data-ttu-id="6c437-122">Doit être inférieur à 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="6c437-122">Must be less than 2^32.</span></span>                        |
| <span data-ttu-id="6c437-123">ArtistName</span><span class="sxs-lookup"><span data-stu-id="6c437-123">ArtistName</span></span>             | <span data-ttu-id="6c437-124">Chaîne Unicode. Exemple : Don Funk</span><span class="sxs-lookup"><span data-stu-id="6c437-124">Unicode string.Example: Don Funk</span></span><br/>       | <span data-ttu-id="6c437-125">Nom complet de l’artiste.</span><span class="sxs-lookup"><span data-stu-id="6c437-125">Display name for the artist.</span></span>                                                                               |
| <span data-ttu-id="6c437-126">LinkedGenreID</span><span class="sxs-lookup"><span data-stu-id="6c437-126">LinkedGenreID</span></span>          | <span data-ttu-id="6c437-127">Entier non négatif. Exemple : 313</span><span class="sxs-lookup"><span data-stu-id="6c437-127">Non-negative integer.Example: 313</span></span><br/>      | <span data-ttu-id="6c437-128">GenreID du genre principal de l’artiste.</span><span class="sxs-lookup"><span data-stu-id="6c437-128">GenreID of the artist's primary genre.</span></span> <span data-ttu-id="6c437-129">Doit être un genre principal et non un sous-genre.</span><span class="sxs-lookup"><span data-stu-id="6c437-129">Must be a main genre and not a subgenre.</span></span> <span data-ttu-id="6c437-130">Une seule valeur est autorisée.</span><span class="sxs-lookup"><span data-stu-id="6c437-130">Only one value is allowed.</span></span> |
| <span data-ttu-id="6c437-131">LinkedSimilarArtistIDs</span><span class="sxs-lookup"><span data-stu-id="6c437-131">LinkedSimilarArtistIDs</span></span> | <span data-ttu-id="6c437-132">N/A</span><span class="sxs-lookup"><span data-stu-id="6c437-132">N/A</span></span>                                               | <span data-ttu-id="6c437-133">Non utilisé dans cette version.</span><span class="sxs-lookup"><span data-stu-id="6c437-133">Not used in this release.</span></span> <span data-ttu-id="6c437-134">Doit être vide.</span><span class="sxs-lookup"><span data-stu-id="6c437-134">Should be empty.</span></span>                                                                 |
| <span data-ttu-id="6c437-135">Popularité</span><span class="sxs-lookup"><span data-stu-id="6c437-135">Popularity</span></span>             | <span data-ttu-id="6c437-136">Il peut s’agir d’un entier ou d’une valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="6c437-136">Can be integer or decimal value.</span></span> <span data-ttu-id="6c437-137">Exemple : 1252,25</span><span class="sxs-lookup"><span data-stu-id="6c437-137">Example: 1252.25</span></span> | <span data-ttu-id="6c437-138">Classement de la popularité.</span><span class="sxs-lookup"><span data-stu-id="6c437-138">Popularity ranking.</span></span> <span data-ttu-id="6c437-139">Peut être la position dans la liste lorsqu’elle est triée par popularité.</span><span class="sxs-lookup"><span data-stu-id="6c437-139">Can be the position in the list when sorted by popularity.</span></span>                             |
| <span data-ttu-id="6c437-140">FeedsAvailable</span><span class="sxs-lookup"><span data-stu-id="6c437-140">FeedsAvailable</span></span>         | <span data-ttu-id="6c437-141">Propriété booléenne.</span><span class="sxs-lookup"><span data-stu-id="6c437-141">Boolean.</span></span> <span data-ttu-id="6c437-142">Format : \[ 0 \| 1 \] exemple : 0</span><span class="sxs-lookup"><span data-stu-id="6c437-142">Format: \[0\|1\]Example: 0</span></span><br/>    | <span data-ttu-id="6c437-143">Non utilisé dans cette version.</span><span class="sxs-lookup"><span data-stu-id="6c437-143">Not used in this release.</span></span> <span data-ttu-id="6c437-144">Doit être vide.</span><span class="sxs-lookup"><span data-stu-id="6c437-144">Should be empty.</span></span>                                                                 |



 

 

 





