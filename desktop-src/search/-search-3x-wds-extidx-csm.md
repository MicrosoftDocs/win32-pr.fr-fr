---
description: le gestionnaire de portée d’analyse (CSM) est un ensemble d’interfaces qui fournit des méthodes pour informer le moteur de recherche Windows sur les conteneurs à analyser et les éléments sous ces conteneurs à inclure ou exclure dans le catalogue.
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: Utilisation du gestionnaire de portée d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a440041c4af9b0ab5e1d282b91cf8fba35c041a546b8247d320884f072a641c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681205"
---
# <a name="using-the-crawl-scope-manager"></a>Utilisation du gestionnaire de portée d’analyse

le gestionnaire de portée d’analyse (CSM) est un ensemble d’interfaces qui fournit des méthodes pour informer le moteur de recherche Windows sur les conteneurs à analyser et les éléments sous ces conteneurs à inclure ou exclure dans le catalogue. Les développeurs peuvent utiliser le CSM pour définir par programmation une étendue d’analyse pour un nouveau magasin de données ou gestionnaire de protocole. Les administrateurs peuvent utiliser le CSM pour afficher tous les index des utilisateurs, les racines de recherche et les règles d’étendue.

Cette section est organisée comme suit :

-   [Qu’est-ce que le gestionnaire de portée d’analyse ?](#what-is-the-crawl-scope-manager)
-   [Rechercher les racines et les règles d’étendue](#search-roots-and-scope-rules)
    -   [Rechercher les racines](#search-roots-and-scope-rules)
    -   [Règles d’étendue](#scope-rules)
-   [Stratégies de groupe prises en charge par le gestionnaire de portée d’analyse](#group-policies-supported-by-the-crawl-scope-manager)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a>Qu’est-ce que le gestionnaire de portée d’analyse ?

Pour comprendre le gestionnaire de portée d’analyse, vous devez comprendre les termes suivants :

-   Une *étendue d’analyse* est un ensemble d’URL pointant vers des magasins de données ou des conteneurs (magasins de données de messagerie, bases de données, partages de fichiers réseau, etc.) que l’indexeur analyse pour indexer les éléments. Dans le cas d’une banque de données hiérarchique, l’étendue de l’analyse peut inclure une URL parente, mais elle exclut une URL enfant et vice versa. Les éléments de la portée de l’analyse sont indexés ; les éléments en dehors de la portée de l’analyse sont ignorés.
-   Une *racine de recherche* est l’URL de niveau supérieur qui identifie un conteneur ou un magasin de données associé à un gestionnaire de protocole particulier. Les racines de recherche peuvent identifier les emplacements qui sont spécifiques à un utilisateur, qui se trouvent sur un ordinateur distant ou qui correspondent à un modèle de caractère générique. Lorsque vous ajoutez un nouveau magasin de données ou un nouveau gestionnaire de protocole, vous devez également ajouter une racine de recherche à la portée de l’analyse.
-   Une *règle d’étendue* est une règle qui inclut ou exclut de l’analyse et de l’indexation des URL d’une racine de recherche. Par exemple, supposons que vous souhaitiez que tout le contenu du dossier ProjectFiles soit indexé, à l’exception des prototypes de sous-dossier. Vous avez besoin d’une règle d’inclusion pour file:///C : \\ WorkteamA \\ ProjectFiles \\ et d’une règle d’exclusion pour file:///C : \\ WorkteamA \\ ProjectFiles \\ prototypes \\ .

le **gestionnaire de portée d’analyse (CSM)** est un ensemble d’api qui vous permet d’ajouter, de supprimer et d’énumérer des racines de recherche et des règles d’étendue pour le Windows indexeur de recherche. Lorsque vous souhaitez que l’indexeur commence l’analyse d’un nouveau conteneur, vous pouvez utiliser CSM pour définir les règles de racine et d’étendue de recherche pour les chemins d’accès dans la ou les racines de recherche. Par exemple, si vous installez un nouveau gestionnaire de protocole, vous pouvez créer une racine de recherche et ajouter une ou plusieurs règles d’inclusion. l’indexeur peut ensuite lancer une analyse pour l’indexation initiale. Le CSM offre les interfaces suivantes pour vous aider à effectuer cette opération par programme.

-   [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [IEnumSearchScopeRules](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [ISearchCrawlScopeManager2](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [ISearchItem](./-search-isearchitem.md)

Bien que vous puissiez utiliser les API CSM pour définir une étendue d’analyse par programme, CSM a été conçu pour prendre également en charge les utilisateurs finaux. Par exemple, supposez que vous avez développé un gestionnaire de protocole pour un nouveau magasin de données et que vous souhaitez permettre aux utilisateurs ou aux administrateurs de gérer les chemins d’accès à indexer. vous pouvez utiliser le gestionnaire de portée d’analyse pour définir une ou plusieurs racines de recherche (par exemple, file:///C : \\ MyContainer \\ ), et l’interface utilisateur de recherche Windows pour définir les options d’indexation affiche chaque racine de recherche avec une case à cocher. Les utilisateurs peuvent ensuite inclure ou exclure ce chemin d’accès ou les enfants de ce chemin d’accès.

## <a name="search-roots-and-scope-rules"></a>Rechercher les racines et les règles d’étendue

Les racines de recherche et les règles d’étendue définissent ensemble un jeu de travail d’URL qui composent la portée de l’analyse de l’indexeur.

### <a name="search-roots"></a>Rechercher les racines

La définition d’une racine de recherche ne spécifie pas les parties de ce magasin qui doivent être indexées ; Il signale simplement qu’un magasin de contenu existe et est associé à un gestionnaire de protocole inscrit. La syntaxe d’une racine de recherche comprend un protocole, un identificateur de sécurité de site ou d’utilisateur, ainsi qu’un chemin d’accès aux emplacements à analyser.

Vous devez créer des racines de recherche lorsque vous :

-   Installer un gestionnaire de protocole ou
-   Vous souhaitez indexer un nouveau magasin de données

AND

-   ce magasin de données n’est pas déjà dans l’étendue de l’analyse de l’indexeur.

Reportez-vous à [gestion des racines de recherche](-search-3x-wds-extidx-csm-searchroots.md) pour obtenir des instructions sur l’ajout, la suppression et l’énumération des racines de recherche.

### <a name="scope-rules"></a>Règles d’étendue

Les règles d’étendue incluent ou excluent de l’analyse et de l’indexation des URL dans une racine de recherche. Les règles d’étendue peuvent être définies par les utilisateurs finaux, par la stratégie de groupe ou par des développeurs tiers. Vous devez définir des règles d’étendue par programmation quand vous définissez une nouvelle racine de recherche. Vos règles de recherche et les racines de recherche comportent la portée de l’analyse par défaut de votre magasin de données et de votre gestionnaire de protocole.

> [!Note]  
> Les utilisateurs ayant accès au panneau de configuration peuvent modifier l’étendue de l’analyse par défaut. Par conséquent, toute application qui offre une gestion d’étendue doit toujours recevoir les règles directement à partir du CSM en utilisant les méthodes d’énumération au lieu de s’appuyer sur sa propre copie enregistrée des règles de l’utilisateur.

 

Reportez-vous à [gestion des règles d’étendue](-search-3x-wds-extidx-csm-scoperules.md) pour obtenir des instructions sur l’ajout, la suppression, le rétablissement et l’énumération des règles d’étendue.

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a>Stratégies de groupe prises en charge par le gestionnaire de portée d’analyse

Les administrateurs système peuvent définir des étendues d’analyse au sein de leurs organisations à l’aide de stratégies de groupe. Ces règles de stratégie de groupe peuvent également servir de règles par défaut, que les utilisateurs peuvent remplacer. Par exemple, vous pouvez avoir un ensemble de répertoires indexés pour un groupe d’utilisateurs et un ensemble différent pour un autre groupe d’utilisateurs, ce qui permet aux utilisateurs de désélectionner ces valeurs par défaut. Les règles de stratégie de groupe peuvent également servir de règles d’exclusion forcée que les utilisateurs ne peuvent pas remplacer, ce qui empêche certains utilisateurs d’indexer certains partages réseau, par exemple.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des racines de recherche](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[Gestion des règles d’étendue](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[Processus d’indexation](-search-indexing-process-overview.md)
</dt> </dl>

 

 
