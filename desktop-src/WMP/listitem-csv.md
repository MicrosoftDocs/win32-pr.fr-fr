---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player Online stores, listitem.csv
- magasins en ligne, listitem.csv
- tapez 1 magasins en ligne, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379807"
---
# <a name="listitemcsv"></a><span data-ttu-id="c731a-107">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="c731a-107">listitem.csv</span></span>

<span data-ttu-id="c731a-108">Ce fichier contient des entrées pour chaque élément inclus dans une liste.</span><span class="sxs-lookup"><span data-stu-id="c731a-108">This file contains entries for each item that is included in a list.</span></span> <span data-ttu-id="c731a-109">Chaque entrée est une ligne composée des champs délimités par des tabulations décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c731a-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="c731a-110">Les champs doivent apparaître dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="c731a-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="c731a-111">Tous les champs sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="c731a-111">All fields are required.</span></span>

<span data-ttu-id="c731a-112">La colonne format dans le tableau ci-dessous décrit la façon dont chaque champ de texte Unicode est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="c731a-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="c731a-113">Elle ne fait pas référence au type de données du contenu.</span><span class="sxs-lookup"><span data-stu-id="c731a-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="c731a-114">Par exemple, si l’entier est indiqué dans la colonne format, cela signifie que le champ contient une chaîne Unicode représentant une valeur intégrale, plutôt qu’un entier réel.</span><span class="sxs-lookup"><span data-stu-id="c731a-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="c731a-115">Champ</span><span class="sxs-lookup"><span data-stu-id="c731a-115">Field</span></span>              | <span data-ttu-id="c731a-116">Format</span><span class="sxs-lookup"><span data-stu-id="c731a-116">Format</span></span>                                          | <span data-ttu-id="c731a-117">Description</span><span class="sxs-lookup"><span data-stu-id="c731a-117">Description</span></span>                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c731a-118">\_ListId liés</span><span class="sxs-lookup"><span data-stu-id="c731a-118">Linked\_ListID</span></span>     | <span data-ttu-id="c731a-119">Entier non négatif. Exemple : 465</span><span class="sxs-lookup"><span data-stu-id="c731a-119">Non-negative integer.Example: 465</span></span><br/>    | <span data-ttu-id="c731a-120">ID de la liste dont cet élément fait partie.</span><span class="sxs-lookup"><span data-stu-id="c731a-120">The ID of the list this item is part of.</span></span>                                                                               |
| <span data-ttu-id="c731a-121">\_ListItem lié</span><span class="sxs-lookup"><span data-stu-id="c731a-121">Linked\_ListItem</span></span>   | <span data-ttu-id="c731a-122">Entier non négatif. Exemple : 684793</span><span class="sxs-lookup"><span data-stu-id="c731a-122">Non-negative integer.Example: 684793</span></span><br/> | <span data-ttu-id="c731a-123">ID de l'élément.</span><span class="sxs-lookup"><span data-stu-id="c731a-123">The ID of the item.</span></span> <span data-ttu-id="c731a-124">Il peut s’agir de l’ID d’une piste, d’un album, d’un artiste, d’un genre, d’un sous-genre, d’un flux radio ou d’une autre liste.</span><span class="sxs-lookup"><span data-stu-id="c731a-124">Can be the ID of a track, an album, an artist, a genre, a subgenre, a radio feed, or another list.</span></span> |
| <span data-ttu-id="c731a-125">ItemPositionInList</span><span class="sxs-lookup"><span data-stu-id="c731a-125">ItemPositionInList</span></span> | <span data-ttu-id="c731a-126">Entier non négatif. Exemple : 5</span><span class="sxs-lookup"><span data-stu-id="c731a-126">Non-negative integer.Example: 5</span></span><br/>      | <span data-ttu-id="c731a-127">Position de l’élément dans sa liste.</span><span class="sxs-lookup"><span data-stu-id="c731a-127">The position of the item within its list.</span></span> <span data-ttu-id="c731a-128">Le premier élément d’une liste est à la position 0.</span><span class="sxs-lookup"><span data-stu-id="c731a-128">The first item in a list is at position 0.</span></span>                                   |



 

 

 





