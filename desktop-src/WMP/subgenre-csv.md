---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player Online stores, subgenre.csv
- magasins en ligne, subgenre.csv
- tapez 1 magasins en ligne, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512063"
---
# <a name="subgenrecsv"></a><span data-ttu-id="6cd1c-107">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="6cd1c-107">subgenre.csv</span></span>

<span data-ttu-id="6cd1c-108">Ce fichier contient une entrée pour chaque sous-genre représenté dans le catalogue.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-108">This file contains an entry for each subgenre represented in the catalog.</span></span> <span data-ttu-id="6cd1c-109">Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="6cd1c-110">Les champs doivent apparaître dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="6cd1c-111">La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="6cd1c-112">Elle ne fait pas référence au type de données du contenu.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="6cd1c-113">Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="6cd1c-114">Champ</span><span class="sxs-lookup"><span data-stu-id="6cd1c-114">Field</span></span>             | <span data-ttu-id="6cd1c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6cd1c-115">Required</span></span> | <span data-ttu-id="6cd1c-116">Format</span><span class="sxs-lookup"><span data-stu-id="6cd1c-116">Format</span></span>                                                                                            | <span data-ttu-id="6cd1c-117">Description</span><span class="sxs-lookup"><span data-stu-id="6cd1c-117">Description</span></span>                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd1c-118">SubGenreID</span><span class="sxs-lookup"><span data-stu-id="6cd1c-118">SubGenreID</span></span>        | <span data-ttu-id="6cd1c-119">Oui</span><span class="sxs-lookup"><span data-stu-id="6cd1c-119">Yes</span></span>      | <span data-ttu-id="6cd1c-120">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-120">Non-negative integer.</span></span>                                                                             | <span data-ttu-id="6cd1c-121">Identificateur de sous-genre (ID), unique dans subgenre.csv.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-121">Subgenre identifier (ID), unique within subgenre.csv.</span></span> <span data-ttu-id="6cd1c-122">Jusqu’à 1024 sous-genres sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-122">Up to 1024 subgenres are allowed.</span></span>                                                                   |
| <span data-ttu-id="6cd1c-123">SubGenreTitle</span><span class="sxs-lookup"><span data-stu-id="6cd1c-123">SubGenreTitle</span></span>     | <span data-ttu-id="6cd1c-124">Oui</span><span class="sxs-lookup"><span data-stu-id="6cd1c-124">Yes</span></span>      | <span data-ttu-id="6cd1c-125">Chaîne Unicode. Exemple : musique de danse intelligente (IDM)</span><span class="sxs-lookup"><span data-stu-id="6cd1c-125">Unicode string.Example: Intelligent Dance Music (IDM)</span></span><br/>                                  | <span data-ttu-id="6cd1c-126">Nom complet du sous-genre.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-126">Subgenre display name.</span></span>                                                                                                                                    |
| <span data-ttu-id="6cd1c-127">SubGenreSubtitle</span><span class="sxs-lookup"><span data-stu-id="6cd1c-127">SubGenreSubtitle</span></span>  | <span data-ttu-id="6cd1c-128">Non</span><span class="sxs-lookup"><span data-stu-id="6cd1c-128">No</span></span>       | <span data-ttu-id="6cd1c-129">Chaîne Unicode. Exemple : nouvelle musique électronique à percussion, qui n’est pas très pure.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-129">Unicode string.Example: New, percussive electronic music that's not quite pure techno.</span></span><br/> | <span data-ttu-id="6cd1c-130">Décrivez la signification du nom d’affichage du sous-genre.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-130">Describe the meaning of the subgenre display name.</span></span> <span data-ttu-id="6cd1c-131">Doit être inférieur à 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-131">Should be less than 64 characters.</span></span>                                                                     |
| <span data-ttu-id="6cd1c-132">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="6cd1c-132">FeedsAreAvailable</span></span> | <span data-ttu-id="6cd1c-133">Oui</span><span class="sxs-lookup"><span data-stu-id="6cd1c-133">Yes</span></span>      | <span data-ttu-id="6cd1c-134">Boolean. format : \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="6cd1c-134">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="6cd1c-135">Exemple : 0</span><span class="sxs-lookup"><span data-stu-id="6cd1c-135">Example: 0</span></span><br/>                                         | <span data-ttu-id="6cd1c-136">Indique s’il est possible d’accéder à un flux.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-136">Indicates whether "radio play" is possible by jumping to a feed.</span></span>                                                                                          |
| <span data-ttu-id="6cd1c-137">\_GenreID liés</span><span class="sxs-lookup"><span data-stu-id="6cd1c-137">Linked\_GenreID</span></span>   | <span data-ttu-id="6cd1c-138">Oui</span><span class="sxs-lookup"><span data-stu-id="6cd1c-138">Yes</span></span>      | <span data-ttu-id="6cd1c-139">Entier non négatif (GenreID). Exemple : 12</span><span class="sxs-lookup"><span data-stu-id="6cd1c-139">Non-negative integer (GenreID).Example: 12</span></span><br/>                                             | <span data-ttu-id="6cd1c-140">GenreID du genre parent.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-140">The GenreID of the parent genre.</span></span> <span data-ttu-id="6cd1c-141">Un seul parent est autorisé.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-141">Only one parent is allowed.</span></span>                                                                                              |
| <span data-ttu-id="6cd1c-142">SortOrderRank</span><span class="sxs-lookup"><span data-stu-id="6cd1c-142">SortOrderRank</span></span>     | <span data-ttu-id="6cd1c-143">Oui</span><span class="sxs-lookup"><span data-stu-id="6cd1c-143">Yes</span></span>      | <span data-ttu-id="6cd1c-144">Entier non négatif. Exemple : 23</span><span class="sxs-lookup"><span data-stu-id="6cd1c-144">Non-negative integer.Example: 23</span></span><br/>                                                       | <span data-ttu-id="6cd1c-145">Classement, idéalement unique, utilisé pour trier les sous-genres dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-145">A ranking, ideally unique, used for sorting subgenres in the user interface.</span></span> <span data-ttu-id="6cd1c-146">Si le genre parent a 10 sous-genres, il peut s’agir d’un entier compris entre 1 et 10.</span><span class="sxs-lookup"><span data-stu-id="6cd1c-146">If the parent genre has 10 subgenres, this might be an integer from 1 to 10.</span></span> |



 

 

 





