---
description: à partir de Windows 7, les incohérences restent dans le traitement et l’analyse des url. Cette rubrique fournit un guide limité pour la navigation dans les incohérences dans les formats d’URL de fichier.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: Configuration requise pour la mise en forme des URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1bb413501548922eaf1b60801b6d35495d7f8a37dc743675052d4e0e5bae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462231"
---
# <a name="url-formatting-requirements"></a>Configuration requise pour la mise en forme des URL

à partir de Windows 7, les incohérences restent dans le traitement et l’analyse des url. Cette rubrique fournit un guide limité pour la navigation dans les incohérences dans les formats d’URL de fichier.

Cette rubrique est organisée comme suit :

-   [Formats d’URL utilisés](#url-formats-in-use)
-   [Sens de la barre oblique, étoile de fin et respect de la barre oblique finale](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [Formats d’URL par API et requête](#url-formats-by-api-and-query)
-   [Rubriques connexes](#related-topics)

## <a name="url-formats-in-use"></a>Formats d’URL utilisés

Les protocoles tiers sont responsables de la définition de leur format d’URL et de la définition de requêtes d’une manière conforme à leur standard. par exemple, Microsoft Outlook prend en charge les noms de dossiers avec des caractères arbitraires, y compris ceux qui ne sont pas autorisés dans les url telles que le `"?"` caractère. Le gestionnaire de protocole MAPI effectue son propre encodage d’URL de ses URL. par conséquent, l’index est stocké `"%3F"` au lieu de `"?"` , et Outlook devez prendre ceci en compte lors de la création de requêtes.

Les différents formats sont répertoriés dans le tableau suivant et chaque identificateur de lettre leur est attribué plus loin dans cette rubrique.



| ID  | URL du fichier local ou distant |  Exemple                     |
|-----|--------------------------|-----------------------------|
| A   | Local                    | file:///c : \\ exemple de test \\\\ |
| B   | Local                    | fichier : c:/test/example/       |
| C   | Local                    | c : \\ exemple de test \\\\         |
| D   | À distance                   | \\ \\ partage de serveur file:/// \\\\ |
| E   | À distance                   | file://server/share/        |
| F   | À distance                   | \\\\partage de serveur \\\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Sens de la barre oblique, étoile de fin et respect de la barre oblique finale

dans Windows recherche, il n’existe pratiquement aucune sensibilité à la direction de la barre oblique. Si le format `c:\test\example` est accepté, c:/test/example est également accepté. Toutefois, bien que l' [étendue](-search-sql-folderdepth.md) ne soit généralement pas sensible à la barre oblique, elle est sensible à la barre oblique dans le cas du format d’URL distant F. par conséquent, `Scope = '//server/share'` ne fonctionne pas.

La seule API qui est sensible aux étoiles de fin et fait la distinction entre `c:\test\ ` et `c:\test\*` est [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager). S’il existe une règle d’exclusion pour `c:\test\*` , le répertoire d’URL `c:\test` lui-même est toujours indexé. Toutefois, si l’URL d’exclusion est `c:\test\` , le répertoire d’URL `c:\test` lui-même ne sera pas indexé.

il existe deux emplacements où la recherche Windows est sensible aux barres obliques de fin : ItemUrl et Path queries. s’il existe un répertoire `c:\test` , Windows recherche traite `c:\test\` différemment de `c:\test` pour les prédicats like `path = 'c:\test'` et `System.ItemUrl = 'c:\test'` . Par exemple, le prédicat `path='file:c:/test'` correspond au répertoire `c:\test` , mais ce `path='file:c:/test/'` n’est pas le cas en raison de la barre oblique finale.

## <a name="url-formats-by-api-and-query"></a>Formats d’URL par API et requête

Les formats d’URL de fichier local acceptés par les requêtes et les API sélectionnées sont répertoriés dans le tableau suivant. Les formats sont associés à une lettre (A à F), ce qui a été indiqué dans la section «[formats d’URL utilisés](#url-formats-in-use)» plus haut dans cette rubrique.



| API ou requête                                                                                                    | Mettre en forme un | Format B | Format C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | O        | N        | O        |
| [**IGatherNotifyInline :: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | O        | O        | O        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | O        | O        | O        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | O        | N        | N        |
| [**ISearchCatalogManager2 ::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | O        | O        | O        |
| Étendue =                                                                                                          | N        | O        | O        |
| Répertoire =                                                                                                      | N        | O        | O        |
| ItemUrl =                                                                                                        | N        | O        | O        |
| Chemin d’accès =                                                                                                           | N        | O        | O        |



 

Les formats d’URL de fichiers distants acceptés par les requêtes sélectionnées sont répertoriés dans le tableau suivant.



| Requête                                                                                                           | Format D | Format E | Format F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | N/A      | N/A      | N/A      |
| [**IGatherNotifyInline :: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | N/A      | N/A      | N/A      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | N/A      | N/A      | N/A      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | N/A      | N/A      | N/A      |
| [**ISearchCatalogManager2 ::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | N/A      | N/A      | N/A      |
| Étendue =                                                                                                          | O        | O        | O        |
| Répertoire =                                                                                                      | O        | O        | O        |
| ItemUrl =                                                                                                        | O        | O        | O        |
| Chemin d’accès =                                                                                                           | O        | O        | O        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ce qui est inclus dans l’index](-search-indexing-process-overview.md)
</dt> <dt>

[processus d’indexation dans Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[interrogation du processus dans Windows la recherche](querying-process--windows-search-.md)
</dt> <dt>

[processus de notifications dans Windows Search](-search-3x-wds-support.md)
</dt> </dl>

 

 
