---
description: Uniscribe fournit des API pour prendre en charge la typographie et pour prendre en charge l’affichage et la modification de texte international, y compris les règles complexes de l’Asie du moyen et des scripts asiatiques.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Utilisation de Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542045"
---
# <a name="using-uniscribe"></a><span data-ttu-id="57261-103">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="57261-103">Using Uniscribe</span></span>

<span data-ttu-id="57261-104">Uniscribe fournit des API pour prendre en charge la typographie et pour prendre en charge l’affichage et la modification de texte international, y compris les règles complexes de l’Asie du moyen et des scripts asiatiques.</span><span class="sxs-lookup"><span data-stu-id="57261-104">Uniscribe provides APIs to support typography and to support the display and editing of international text, including the complex rules of Middle Eastern and Asian scripts.</span></span> <span data-ttu-id="57261-105">Uniscribe fournit des routines de bas niveau pour gérer le texte entièrement mis en forme, et une API ScriptString simple définie pour le texte non mis en forme.</span><span class="sxs-lookup"><span data-stu-id="57261-105">Uniscribe provides low-level routines for handling fully formatted text, and a simple ScriptString API set for unformatted text.</span></span>

<span data-ttu-id="57261-106">À l’aide de Uniscribe, les applications doivent uniquement gérer un magasin de stockage de codes de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="57261-106">Using Uniscribe, applications only have to manage a backing store of Unicode character codes.</span></span> <span data-ttu-id="57261-107">Les applications de disposition du texte n’ont pas besoin de gérer d’autres tampons ou tables de mappage pour suivre l’ordre des caractères.</span><span class="sxs-lookup"><span data-stu-id="57261-107">Text layout applications do not have to maintain any other buffer or mapping table to track character order.</span></span> <span data-ttu-id="57261-108">Chaque application ne doit stocker et gérer que l’ordre dans lequel les caractères sont entrés par l’utilisateur, ce qui correspond à l’ordre logique défini par Unicode.</span><span class="sxs-lookup"><span data-stu-id="57261-108">Each application only has to store and manage the order in which the characters are entered by the user, which is the same logical order as defined by Unicode.</span></span> <span data-ttu-id="57261-109">Le magasin de stockage ne change jamais suite à des opérations de disposition.</span><span class="sxs-lookup"><span data-stu-id="57261-109">The backing store never changes as a result of layout operations.</span></span> <span data-ttu-id="57261-110">Uniscribe gère un index à partir des clusters réorganisés jusqu’aux limites de caractères d’origine passées par l’application.</span><span class="sxs-lookup"><span data-stu-id="57261-110">Uniscribe maintains an index from the reordered clusters to the original character boundaries passed by the application.</span></span>

<span data-ttu-id="57261-111">Les rubriques suivantes sont traitées dans cette section.</span><span class="sxs-lookup"><span data-stu-id="57261-111">The following topics are covered in this section.</span></span>

<span data-ttu-id="57261-112">**Modélisation**</span><span class="sxs-lookup"><span data-stu-id="57261-112">**Shaping**</span></span>

-   [<span data-ttu-id="57261-113">Déterminer si un script nécessite la mise en forme de glyphes</span><span class="sxs-lookup"><span data-stu-id="57261-113">Determining If a Script Requires Glyph Shaping</span></span>](determining-if-a-script-requires-glyph-shaping.md)
-   [<span data-ttu-id="57261-114">Utilisation de moteurs de mise en forme</span><span class="sxs-lookup"><span data-stu-id="57261-114">Using Shaping Engines</span></span>](using-shaping-engines.md)

<span data-ttu-id="57261-115">**Autre traitement**</span><span class="sxs-lookup"><span data-stu-id="57261-115">**Other Processing**</span></span>

-   [<span data-ttu-id="57261-116">Mise en cache</span><span class="sxs-lookup"><span data-stu-id="57261-116">Caching</span></span>](caching.md)
-   [<span data-ttu-id="57261-117">Affichage de texte avec Uniscribe</span><span class="sxs-lookup"><span data-stu-id="57261-117">Displaying Text with Uniscribe</span></span>](displaying-text-with-uniscribe.md)
-   [<span data-ttu-id="57261-118">Traitement de scripts complexes</span><span class="sxs-lookup"><span data-stu-id="57261-118">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
-   [<span data-ttu-id="57261-119">Utilisation de la police de secours</span><span class="sxs-lookup"><span data-stu-id="57261-119">Using Font Fallback</span></span>](using-font-fallback.md)
-   [<span data-ttu-id="57261-120">Utilisation des fonctions ScriptString</span><span class="sxs-lookup"><span data-stu-id="57261-120">Using the ScriptString Functions</span></span>](using-the-scriptstring-functions.md)

<span data-ttu-id="57261-121">**Signe insertion**</span><span class="sxs-lookup"><span data-stu-id="57261-121">**Caret**</span></span>

-   [<span data-ttu-id="57261-122">Affichage du signe insertion dans les chaînes bidirectionnelles</span><span class="sxs-lookup"><span data-stu-id="57261-122">Displaying the Caret in Bidirectional Strings</span></span>](displaying-the-caret-in-bidirectional-strings.md)
-   [<span data-ttu-id="57261-123">Gestion de l’emplacement du signe insertion et du test de positionnement</span><span class="sxs-lookup"><span data-stu-id="57261-123">Managing Caret Placement and Hit Testing</span></span>](managing-caret-placement-and-hit-testing.md)
-   [<span data-ttu-id="57261-124">Translation de l’offset X de l’accès à la souris à la position du signe insertion</span><span class="sxs-lookup"><span data-stu-id="57261-124">Translating Mouse Hit X Offset to Caret Position</span></span>](translating-mouse-hit-x-offset-to-caret-position.md)

<span data-ttu-id="57261-125">**Mots et clusters de caractères**</span><span class="sxs-lookup"><span data-stu-id="57261-125">**Words and Character Clusters**</span></span>

-   [<span data-ttu-id="57261-126">Utilisation de clusters de caractères</span><span class="sxs-lookup"><span data-stu-id="57261-126">Using Character Clusters</span></span>](using-character-clusters.md)
-   [<span data-ttu-id="57261-127">Utilisation des points d’arrêt de mot</span><span class="sxs-lookup"><span data-stu-id="57261-127">Using Word Break Points</span></span>](using-word-break-points.md)
-   [<span data-ttu-id="57261-128">Utilisation des relations entre les positions du signe insertion, les points de justification et les clusters</span><span class="sxs-lookup"><span data-stu-id="57261-128">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



