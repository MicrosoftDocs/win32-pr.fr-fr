---
description: Les interfaces ISearchCatalogManager et ISearchCatalogManager2 fournissent des méthodes pour gérer un catalogue de recherche, telles que la réindexation ou la définition de délais d’attente.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Utilisation du gestionnaire de catalogues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1295cc9cc76fb334b4687b876fa1959a22e33235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532078"
---
# <a name="using-the-catalog-manager"></a>Utilisation du gestionnaire de catalogues

Les interfaces [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) et [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) fournissent des méthodes pour gérer un catalogue de recherche, telles que la réindexation ou la définition de délais d’attente. Bien que Windows Search n’utilise actuellement qu’un seul catalogue, cette interface a été conçue pour vous offrir un meilleur contrôle de la gestion de plusieurs catalogues de manière indépendante. L’interface gère le catalogue des manières suivantes :

- Accès à d’autres interfaces : récupération d’autres interfaces relatives à la recherche requises par le gestionnaire de portée d’analyse, les notifications de modification de données et l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .
- Contenu du catalogue : s’assurer que les nouvelles données sont indexées et que d’autres applications et composants fonctionnent correctement en forçant la réindexation de tout ou partie du catalogue ou en réinitialisant l’intégralité du catalogue.
- Propriétés de catalogue : définition des propriétés qui déterminent comment le catalogue gère les délais d’attente lors de la connexion aux gestionnaires de protocole et comment les marques diacritiques sont traitées dans les recherches.
- État du catalogue : obtention d’informations sur le catalogue, y compris l’État, la taille et l’état de l’activité actuelle.

Cette rubrique est organisée comme suit :

- [Accès aux interfaces associées](#accessing-related-interfaces)
- [Gestion du contenu du catalogue](#managing-the-catalog-contents)
- [Gestion de l’état du catalogue](#managing-catalog-status)
- [Gestion des propriétés de catalogue](#managing-catalog-properties)
- [Exécution en mode élevé](#running-in-elevated-mode)
- [Rubriques connexes](#related-topics)

## <a name="accessing-related-interfaces"></a>Accès aux interfaces associées

Certaines interfaces utiles de la plateforme de recherche Windows nécessitent une instance du gestionnaire de catalogues avant de pouvoir être utilisées. Pour créer un gestionnaire de catalogue pour un catalogue spécifié, appelez la méthode [**ISearchManager :: getCatalog,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) . Les méthodes du gestionnaire de catalogues peuvent ensuite être utilisées pour instancier et retourner des interfaces basées sur le catalogue spécifié.

| Méthode                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Obtient une instance de l’interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) pour le catalogue actuel, pour vous permettre de créer facilement des requêtes.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Obtient une instance de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) pour ce catalogue de recherche, pour permettre aux développeurs de modifier la portée de l’analyse de l’indexeur de recherche Windows.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Obtient une instance de l’interface [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) , que les applications clientes utilisent pour notifier l’indexeur des modifications lorsque le client souhaite indexer les informations d’état de l’élément pour prendre en charge les notifications gérées par le fournisseur. Pour plus d’informations, consultez [notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md) . |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Obtient une instance de [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink), que les applications clientes utilisent pour notifier l’indexeur des modifications lorsque le client ne souhaite pas les informations d’état d’indexation (notifications gérées par l’indexeur). Pour plus d’informations, consultez [notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md) .            |

## <a name="managing-the-catalog-contents"></a>Gestion du contenu du catalogue

Il existe deux tâches principales impliquées dans la gestion du catalogue : la réindexation de l’ensemble ou de certaines des URL dans l’étendue de l’analyse de l’indexeur et la réinitialisation de l’ensemble du catalogue sous-jacent. Lorsque vous réindexez des URL, les anciennes données restent dans le catalogue jusqu’à ce qu’elles soient remplacées par de nouvelles données. Lorsque vous réinitialisez le catalogue, le catalogue entier est régénéré et toutes les URL de l’étendue de l’analyse sont réindexées. Ce processus peut prendre beaucoup de temps et ne doit être utilisé qu’en dernier recours pour la résolution de problèmes tels qu’un index potentiellement endommagé.

Lorsque vous installez une nouvelle application, un gestionnaire de protocole ou un filtre, l’application d’installation doit ajouter son répertoire ou sa racine à l’étendue de l’analyse pour s’assurer que l’indexeur comprend l’emplacement des données de cette application. Si les données n’apparaissent pas dans le catalogue après que l’indexeur a analysé son étendue d’analyse, vous devez d’abord vous assurer que l’emplacement des données est inclus dans la portée de l’analyse. Vous pouvez l’ajouter à l’aide de l’interface utilisateur pour les options de recherche Windows ou du gestionnaire de l’étendue de l' [analyse](-search-3x-wds-extidx-csm.md). Si l’emplacement semble se trouver dans l’étendue de l’analyse, vous pouvez forcer manuellement la réindexation de toutes les URL dans l’étendue de l’analyse de l’indexeur ou d’un sous-ensemble, à l’aide des méthodes suivantes de l’interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .

| Méthode de réindexation                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager :: réindexer**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Réindexe toutes les URL dans le catalogue. Les anciennes informations seront conservées jusqu’à ce qu’elles soient remplacées par de nouvelles informations.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Réindexe les URL qui correspondent au modèle ou commencent à une racine particulière (par exemple, file:///C : \\ NomDossier \\ Subfoldername \\ ). Cela est utile pour réanalyser tout ce qui se trouve dans un répertoire particulier ou avec une extension particulière, comme lors de l’installation d’une application. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Indique à l’indexeur de classer par ordre de priorité les éléments d’indexation avec des URL qui correspondent à un modèle spécifié sur la réalisation d’autres tâches d’indexation.                                                                                                                                    |

**Réinitialisation de l’index.** Vous pouvez réinitialiser l’index entier à l’aide d’un appel à [**ISearchCatalogManager :: Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset). Cela réinitialise le catalogue sous-jacent en reconstruisant les bases de données et en exécutant un index complet de toutes les URL dans l’étendue de l’analyse. Ce processus peut prendre beaucoup de temps et ne doit être utilisé qu’en dernier recours pour la résolution de problèmes tels qu’un index potentiellement endommagé.

> [!IMPORTANT]
> En raison du ralentissement de l’indexation que ces méthodes peuvent provoquer, vous devez les utiliser avec précaution lorsque vous essayez d’identifier les problèmes d’indexation ou de catalogue. Tout d’abord, assurez-vous que vos racines de recherche et règles d’étendue sont ajoutées au gestionnaire de l’étendue de l’analyse, puis assurez-vous que le bit FANCI (attribut de fichier non contenu indexé) est correctement défini pour les fichiers et les dossiers. Si vous avez confirmé que ces dernières sont correctes, essayez d’abord ReindexSearchRoot et réindexer la dernière. Si aucun de ces travaux n’est présent, essayez de réinitialiser en dernier recours.

Pour obtenir des informations connexes, consultez [notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md)et [interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Gestion de l’état du catalogue

Le gestionnaire de catalogues peut être utilisé pour obtenir l’état du catalogue pour les applications qui souhaitent personnaliser la manière dont le catalogue est géré (par exemple, une application de surveillance « État du catalogue » personnalisée). Toutefois, le gestionnaire de catalogues n’est généralement pas requis pour la plupart des scénarios de développement liés à la recherche. Les utilisations courantes sont pour une application de surveillance « État du catalogue » ou une application de type panneau de configuration.

Le tableau suivant décrit les méthodes de ISearchCatalogManager utilisées pour gérer l’état du catalogue.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Méthode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a></td>
<td>Obtient l’URL en cours d’indexation. Cette méthode est utile si vous essayez d’identifier si l’indexeur est &quot; bloqué &quot; sur un élément.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a></td>
<td>Obtient le nombre d’éléments dans le catalogue.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a></td>
<td>Récupère les informations suivantes sur les éléments à indexer :
<ul>
<li>plIncrementalCount : nombre d’éléments à indexer dans l’index incrémentiel suivant</li>
<li>plNotificationQueue : nombre d’éléments dans la file d’attente de notifications. Ces informations seraient utiles à une application de notification qui devait vérifier si l’indexeur reçoit les notifications envoyées par l’application.</li>
<li>plHighPriorityQueue : nombre d’éléments dans la file d’attente haute priorité. Les éléments dans le plHighPriorityQueue sont indexés en premier.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a></td>
<td>Obtient l’état du catalogue et retourne une valeur d’énumération qui donne l’état actuel. Les États de catalogue possibles sont les suivants :
<ul>
<li>Inactif : aucune indexation n’est nécessaire.</li>
<li>Paused : l’indexation est suspendue (en raison d’une batterie faible ou d’une utilisation élevée du processeur, par exemple).</li>
<li>Récupération : l’indexation est en récupération.</li>
<li>Analyse complète : l’indexeur effectue une analyse complète de la portée de l’analyse.</li>
<li>Analyse incrémentielle : l’indexeur effectue une analyse incrémentielle.</li>
<li>Traitement des notifications : l’indexeur traite les notifications.</li>
<li>Arrêt : l’indexeur est en cours d’arrêt.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a></td>
<td>Obtient le nom du catalogue actuel qui est spécifié dans la méthode <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>ISearchManager :: getCatalog,</strong></a> . Actuellement, le seul catalogue pris en charge est SystemIndex.</td>
</tr>
</tbody>
</table>

## <a name="managing-catalog-properties"></a>Gestion des propriétés de catalogue

Trois propriétés de catalogue peuvent être gérées avec le gestionnaire de catalogues :

- **Sensibilité diacritiques.** Les signes diacritiques sont ajoutés aux lettres pour indiquer la signification ou la prononciation d’un mot. Cette propriété détermine si le catalogue respecte les signes diacritiques et est important lorsque vous ou vos utilisateurs recherchez et indexez du texte dans plusieurs langues. Par exemple, si cette propriété a la valeur **false**, le catalogue traiterait « Resume » et « Resumé » comme s’il s’agissait du même mot.
- **Délais d’expiration de la connexion.** Cette propriété représente la durée d’attente d’une réponse de connexion à partir d’un serveur ou d’un magasin de données, comme représenté dans une structure [**d' \_ informations de délai d’attente**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . Vous pouvez utiliser cette propriété pour affiner la recherche Windows.
- **Délais d’attente des données** Cette propriété représente la durée d’attente d’une transaction de données entre l’indexeur et un gestionnaire de protocole ou un filtre, comme représenté dans une structure [**d' \_ informations de délai d’attente**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . Si ce délai est écoulé, le processus à partir du démon de filtre est interrompu pour empêcher les blocages et autres problèmes de ressources.

Les deux dernières propriétés sont principalement destinées à une utilisation ultérieure. Chacune de ces propriétés a `get` des `put` méthodes et.

| Méthode                                                                                                                                                                                                          | Description                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**put \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE si le catalogue doit différencier les mots avec des signes diacritiques. **False** si le catalogue doit ignorer les signes diacritiques. La modification de cette propriété nécessite la reconstruction de l’index, car les clés de l’index peuvent devenir non valides.                       |
| [**recevoir \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**placer \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | Durée, en secondes, pendant laquelle l’indexeur doit attendre une réponse de connexion d’un serveur ou d’un magasin de données. La définition de cette valeur trop élevée peut entraîner des retards si de nombreux sites ne répondent pas. La définition d’une valeur trop faible peut entraîner la non-analyse de certains sites. |
| [**Obtient \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**put \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | Durée, en secondes, pendant laquelle l’indexeur doit attendre une transaction de données.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Exécution en mode élevé

Tous les appels de méthode qui mettent à jour le SystemIndex requièrent que votre application soit exécutée avec des privilèges élevés. Dans le cas contraire, votre application échouera avec une erreur d’accès refusé.

## <a name="related-topics"></a>Rubriques connexes


[Gestion de l’index](-search-3x-wds-mngidx-overview.md)

[Interfaces pour la gestion de l’index](interfaces-for-managing-the-index.md)

[Utilisation du gestionnaire de recherche](-search-3x-wds-mngidx-searchmanager.md)

[Utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md)
