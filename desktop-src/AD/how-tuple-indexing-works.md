---
title: Fonctionnement de l’indexation des tuples
description: Les index de tuple sont utilisés pour optimiser les recherches qui ont 0 ou plusieurs chaînes de recherche médiane et 0 ou 1 chaînes de recherche finale. Elles peuvent également être utilisées pour optimiser les recherches d’une chaîne de recherche initiale si aucun index ordinaire n’est disponible sur cet attribut.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indexation des tuples
- Recherche Active Directory Active Directory, optimisation
- Active Directory, l’optimisation de la recherche Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724485"
---
# <a name="how-tuple-indexing-works"></a><span data-ttu-id="4f040-107">Fonctionnement de l’indexation des tuples</span><span class="sxs-lookup"><span data-stu-id="4f040-107">How Tuple Indexing Works</span></span>

<span data-ttu-id="4f040-108">Les index de tuple sont utilisés pour optimiser les recherches qui ont 0 ou plusieurs [chaînes de recherche médiane](search-string-types.md) et 0 ou 1 chaînes de recherche finale.</span><span class="sxs-lookup"><span data-stu-id="4f040-108">Tuple indices are used to optimize searches that have 0 or more [medial-search strings](search-string-types.md) and 0 or 1 final-search strings.</span></span> <span data-ttu-id="4f040-109">Elles peuvent également être utilisées pour optimiser les recherches d’une chaîne de recherche initiale si aucun index ordinaire n’est disponible sur cet attribut.</span><span class="sxs-lookup"><span data-stu-id="4f040-109">They can also be used to optimize searches for an initial search string if no ordinary index is available over that attribute.</span></span>

<span data-ttu-id="4f040-110">Vous pouvez activer l’indexation des tuples pour un attribut en définissant le bit 5, qui correspond à la valeur 32, dans l’attribut [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .</span><span class="sxs-lookup"><span data-stu-id="4f040-110">You can turn on tuple indexing for an attribute by setting bit 5, which corresponds to the value 32, in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute.</span></span> <span data-ttu-id="4f040-111">Cet attribut est défini dans l’objet de schéma qui représente l’attribut qui a besoin de l’index de Tuple.</span><span class="sxs-lookup"><span data-stu-id="4f040-111">This attribute is set in the schema object that represents the attribute that needs the tuple index.</span></span> <span data-ttu-id="4f040-112">L’impact sur les performances de l’activation de l’indexation des tuples est que toute valeur de chaîne définie pour cet attribut sera développée en un grand nombre de fragments dans l’index de Tuple.</span><span class="sxs-lookup"><span data-stu-id="4f040-112">The performance impact of turning on tuple indexing is that any string value that is set for that attribute will be expanded into a large number of fragments in the tuple index.</span></span> <span data-ttu-id="4f040-113">Lorsqu’un attribut est développé, il consomme une plus grande quantité d’espace disque dans le fichier de l’arborescence d’informations d’annuaire et est également mis à jour plus lentement.</span><span class="sxs-lookup"><span data-stu-id="4f040-113">When an attribute expands, it consumes a larger amount of disk space in the Directory Information Tree file, and also gets updated more slowly.</span></span>

<span data-ttu-id="4f040-114">Les index de tuple sont conçus pour accélérer les recherches dans le formulaire `*string*` .</span><span class="sxs-lookup"><span data-stu-id="4f040-114">Tuple indices are designed to accelerate searches of the form `*string*`.</span></span> <span data-ttu-id="4f040-115">L’accélération peut être considérable, car cette forme de recherche ne peut pas être optimisée d’une autre façon, et dans sa forme non optimisée, elle force le serveur Active Directory à parcourir chaque objet dans l’étendue de la recherche pour exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="4f040-115">The acceleration can be considerable because this form of search cannot be optimized in any other way, and in its un-optimized form, it forces the Active Directory server to walk every object in the scope of the search to perform the query.</span></span> <span data-ttu-id="4f040-116">Par conséquent, une recherche de base recherche simplement un objet, qui utiliseraient moins de ressources, une recherche d’enfants immédiates rechercherait uniquement les enfants d’un objet (qui pourrait utiliser moins de ressources ou plus de ressources en fonction de la taille du conteneur), et une recherche de sous-arborescence parcourra l’ensemble de la sous-arborescence sous l’objet de base, ce qui nécessiterait généralement beaucoup de ressources et sera très lente en raison de la</span><span class="sxs-lookup"><span data-stu-id="4f040-116">Thus, a base search would just search one object, which would use fewer resources, an immediate children search would search just the children of an object (which could use fewer resources or more resources depending on the container size), and a subtree search will walk the entire subtree under the base object, which would usually require a lot of resources and be very slow because of the subtree size.</span></span>

<span data-ttu-id="4f040-117">Les index de tuple fonctionnent en scindant une chaîne en *tuples*.</span><span class="sxs-lookup"><span data-stu-id="4f040-117">Tuple indices work by breaking a string into *tuples*.</span></span> <span data-ttu-id="4f040-118">Par exemple, la chaîne « Active Directory » est décomposée dans les tuples suivants :</span><span class="sxs-lookup"><span data-stu-id="4f040-118">For example, the string "Active Directory" would be broken into the following tuples:</span></span>

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> <span data-ttu-id="4f040-119">Le répertoire s’arrêtera à 32767 caractères lors du développement d’une chaîne pour l’indexation des tuples.</span><span class="sxs-lookup"><span data-stu-id="4f040-119">The directory will stop at 32767 characters when expanding a string for tuple indexing.</span></span>

 

<span data-ttu-id="4f040-120">Un index de tuple contient une entrée pour chacun de ces tuples.</span><span class="sxs-lookup"><span data-stu-id="4f040-120">A tuple index would contain an entry for each one of these tuples.</span></span> <span data-ttu-id="4f040-121">Par conséquent, si un utilisateur recherche `*cto*` , le serveur de Active Directory recherche toutes les correspondances pour « directeur de la configuration » dans l’index et, dans ce cas, retrouve un pointeur vers l’enregistrement qui avait un attribut (Tuple indexé) avec la valeur « Directory ».</span><span class="sxs-lookup"><span data-stu-id="4f040-121">So, if a user searches for `*cto*`, then the Active Directory server will look up all the matches for "cto" in the index and, in this case, find a pointer back to the record that had a (tuple indexed) attribute with a value of "Directory".</span></span>

<span data-ttu-id="4f040-122">Si la chaîne `*cto*` de recherche intégrée (dans l’exemple précédent) est suffisamment spécifique, la recherche est très efficace, car elle réduit considérablement le nombre d’objets que le serveur Active Directory doit inspecter pour exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="4f040-122">If the medial search string (`*cto*` in the previous example) is specific enough, then the search will be quite efficient because it greatly reduces the number of objects that the Active Directory server must inspect to perform the query.</span></span>

 

 