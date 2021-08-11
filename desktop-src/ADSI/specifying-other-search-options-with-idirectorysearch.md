---
title: Spécification d’autres options de recherche avec IDirectorySearch
description: L’interface IDirectorySearch offre un contrôle supplémentaire sur la manière dont la recherche est effectuée par le biais des options de recherche.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Spécification d’autres options de recherche avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67105d9716934c8c7d1d56193ca0cdfde5f6a4bc4c32605420513dc62700d8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178764"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>Spécification d’autres options de recherche avec IDirectorySearch

L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) offre un contrôle supplémentaire sur la manière dont la recherche est effectuée par le biais des options de recherche. Ces options de recherche sont définies en remplissant un tableau de [**\_ SEARCHPREF d' \_ informations sur les publicités**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) et en appelant la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Pour plus d'informations, voir les rubriques suivantes :

-   [Utilisation de la méthode SetSearchPreference](using-the-setsearchpreference-method.md)
-   [Recherches synchrones et asynchrones avec IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Pagination avec IDirectorySearch](paging-with-idirectorysearch.md)
-   [Mise en cache des résultats avec IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Exécution d’une requête d’étendue d’attribut](performing-an-attribute-scoped-query.md)
-   [Tri des résultats de la recherche avec IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md)
-   [Repérage de références avec IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Limite de taille avec IDirectorySearch](size-limit-with-idirectorysearch.md)
-   [Limite de temps du serveur avec IDirectorySearch](server-time-limit-with-idirectorysearch.md)
-   [Limite de temps du client avec IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Retour uniquement des noms d’attributs avec IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)

 

 




