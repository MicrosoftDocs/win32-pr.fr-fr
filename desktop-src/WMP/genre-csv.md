---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player Online stores, genre.csv
- magasins en ligne, genre.csv
- tapez 1 magasins en ligne, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940174"
---
# <a name="genrecsv"></a><span data-ttu-id="792ce-107">genre.csv</span><span class="sxs-lookup"><span data-stu-id="792ce-107">genre.csv</span></span>

<span data-ttu-id="792ce-108">Ce fichier contient une entrée pour chaque genre représenté dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="792ce-108">This file contains an entry for each genre represented in the catalog.</span></span> <span data-ttu-id="792ce-109">Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="792ce-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="792ce-110">Les champs doivent apparaître dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="792ce-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="792ce-111">Tous les champs de genre.csv sont requis.</span><span class="sxs-lookup"><span data-stu-id="792ce-111">All fields in genre.csv are required.</span></span>

<span data-ttu-id="792ce-112">La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="792ce-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="792ce-113">Elle ne fait pas référence au type de données du contenu.</span><span class="sxs-lookup"><span data-stu-id="792ce-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="792ce-114">Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.</span><span class="sxs-lookup"><span data-stu-id="792ce-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="792ce-115">Champ</span><span class="sxs-lookup"><span data-stu-id="792ce-115">Field</span></span>             | <span data-ttu-id="792ce-116">Format</span><span class="sxs-lookup"><span data-stu-id="792ce-116">Format</span></span>                                                    | <span data-ttu-id="792ce-117">Description</span><span class="sxs-lookup"><span data-stu-id="792ce-117">Description</span></span>                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="792ce-118">ID de genre \_</span><span class="sxs-lookup"><span data-stu-id="792ce-118">Genre\_ID</span></span>         | <span data-ttu-id="792ce-119">Entier non négatif. Exemple : 22</span><span class="sxs-lookup"><span data-stu-id="792ce-119">Non-negative integer.Example: 22</span></span><br/>               | <span data-ttu-id="792ce-120">Identificateur de genre, unique dans genre.csv.</span><span class="sxs-lookup"><span data-stu-id="792ce-120">Genre identifier, unique within genre.csv.</span></span> <span data-ttu-id="792ce-121">Doit être inférieur à 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="792ce-121">Must be less than 2^32.</span></span> <span data-ttu-id="792ce-122">Un maximum de 64 genres est possible.</span><span class="sxs-lookup"><span data-stu-id="792ce-122">A maximum of 64 genres is possible.</span></span>                                             |
| <span data-ttu-id="792ce-123">GenreTitle</span><span class="sxs-lookup"><span data-stu-id="792ce-123">GenreTitle</span></span>        | <span data-ttu-id="792ce-124">Chaîne Unicode. Exemple : Rock</span><span class="sxs-lookup"><span data-stu-id="792ce-124">Unicode string.Example: Rock</span></span><br/>                   | <span data-ttu-id="792ce-125">Nom complet du genre.</span><span class="sxs-lookup"><span data-stu-id="792ce-125">Genre display name.</span></span>                                                                                                                                |
| <span data-ttu-id="792ce-126">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="792ce-126">FeedsAreAvailable</span></span> | <span data-ttu-id="792ce-127">Boolean. format : \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="792ce-127">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="792ce-128">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="792ce-128">Example: 0</span></span><br/> | <span data-ttu-id="792ce-129">Indique si le comportement « radio Play » est possible en sautant à un flux.</span><span class="sxs-lookup"><span data-stu-id="792ce-129">Indicates whether "radio play" behavior is possible by jumping to a feed.</span></span>                                                                          |
| <span data-ttu-id="792ce-130">HasComposer</span><span class="sxs-lookup"><span data-stu-id="792ce-130">HasComposer</span></span>       | <span data-ttu-id="792ce-131">Boolean. format : \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="792ce-131">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="792ce-132">Exemple : 1</span><span class="sxs-lookup"><span data-stu-id="792ce-132">Example: 1</span></span><br/> | <span data-ttu-id="792ce-133">True si ce genre doit enregistrer les informations de compositeur dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="792ce-133">True if this genre should save composer information in the catalog.</span></span> <span data-ttu-id="792ce-134">S’il n’est pas défini, les informations du compositeur sont ignorées et ne sont pas compilées dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="792ce-134">If not set, composer information is ignored and not compiled into the catalog.</span></span> |



 

 

 





