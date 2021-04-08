---
description: En utilisant les composants API de notification, vous pouvez informer l’indexeur qu’un élément a été modifié, déplacé ou supprimé et peut ajouter des étendues de recherche à la file d’attente de l’indexeur de recherche Windows des URL qui nécessitent une indexation.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: Notification de l’index des modifications (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a89112da20c4010e1fc23fab16778309195d20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112486"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>Notification de l’index des modifications (Windows Search)

En utilisant les composants API de notification, vous pouvez informer l’indexeur qu’un élément a été modifié, déplacé ou supprimé et peut ajouter des étendues de recherche à la file d’attente de l’indexeur de recherche Windows des URL qui nécessitent une indexation.

Les composants peuvent notifier à l’indexeur de recherche Windows que les données de leur magasin ont changé. En règle générale, vous pouvez vous appuyer sur les analyses planifiées de l’indexeur. Toutefois, le fait de fournir des notifications à l’indexeur peut améliorer les performances en veillant à ce que l’indexeur n’analyse pas l’intégralité du magasin sur les index incrémentiels. Par exemple, cela peut être recommandé si vous vous attendez à ce que votre magasin de données soit exceptionnellement volumineux et/ou exceptionnellement occupé, par exemple dans le cas d’un magasin de données de messagerie électronique.

-   [Implémentation des notifications gérées par l’indexeur](#implementing-indexer-managed-notifications)
    -   [File d’attente des notifications](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [Implémentation des notifications gérées par le fournisseur](#implementing-provider-managed-notifications)
    -   [File d’attente des notifications](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implémentation des notifications gérées par l’indexeur

Les notifications gérées par l’indexeur vous permettent de contrôler l’accès à votre magasin de données tout en vous libérant de la file d’attente de notifications tout au long du processus d’indexation. Votre fournisseur de notifications doit surveiller les modifications apportées au magasin de données et créer une file d’attente de notifications. Régulièrement, votre fournisseur envoie un lot de notifications de modifications à l’indexeur. Lorsque l’indexeur reçoit vos notifications, il renvoie un accusé de réception et vous pouvez supprimer le ou les éléments de votre file d’attente. Si, après un certain laps de temps, vous ne recevez pas d’accusé de réception, vous pouvez renvoyer les notifications. En cas d’échec, l’indexeur reconstruit sa file d’attente interne d’éléments pour analyser ou effectue une analyse incrémentielle du magasin.

Pour implémenter des notifications gérées par l’indexeur, vous devez implémenter les éléments suivants :

-   Mécanisme permettant de surveiller les modifications apportées à votre magasin de données.
-   Structure de données pour les informations de mise en file d’attente (plusieurs structures de [**\_ \_ \_ modification persistantes d’éléments de recherche**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) ) relatives à ces modifications.
-   Interface [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) pour envoyer vos notifications à l’indexeur et recevoir des accusés de réception de notification de l’indexeur.

### <a name="notifications-queue"></a>File d’attente des notifications

Vous devez surveiller et mettre en file d’attente chaque modification de votre magasin de données à envoyer à l’indexeur en tant que notification. Le nombre de notifications mises en file d’attente et la fréquence à laquelle vous les envoyez à l’indexeur dépend de vos circonstances. Vous pouvez peut-être envoyer un lot de notifications pour chaque *n* nombre de modifications ou après un intervalle de temps *t* , ou une combinaison des deux.

L’indexeur s’attend à ce que les notifications se trouvent dans un tableau de structures de [**\_ \_ \_ modification permanentes**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) de l’élément de recherche. vous pouvez donc choisir d’implémenter la file d’attente de la même manière.

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

Pour accéder à cette interface, vous devez d’abord instancier un objet [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) pour accéder à un objet [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . À partir de cet objet **ISearchCatalogManager** , vous instanciez un objet [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) et avertissez l’indexeur des modifications apportées aux données à l’aide d’un appel à la méthode **OnItemsChanged** .

Dans l’appel à cette méthode, vous incluez le nombre de modifications signalées et un tableau de structures de [**\_ \_ \_ modification persistantes d’éléments de recherche**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) . Vous récupérez un tableau de codes de saisie semi-automatique des RH indiquant si chaque URL a été acceptée pour l’indexation. Il s’agit de votre accusé de réception de l’indexeur.

## <a name="implementing-provider-managed-notifications"></a>Implémentation des notifications gérées par le fournisseur

Les notifications gérées par le fournisseur vous permettent de contrôler l’accès à votre magasin de données et de surveiller la progression de l’indexeur lorsqu’il met à jour le catalogue de recherche Windows. Votre fournisseur doit surveiller les modifications apportées au magasin de données et créer une file d’attente de notifications. Régulièrement, votre fournisseur envoie un lot de notifications de modifications à l’indexeur. Lorsque l’indexeur reçoit vos notifications, il renvoie un accusé de réception. Si, après un certain laps de temps, vous ne recevez pas d’accusé de réception, vous pouvez renvoyer les notifications. Étant donné que l’indexeur analyse le magasin de données et met à jour le catalogue de recherche Windows, il avertit votre fournisseur de chaque mise à jour du catalogue et vous permet de supprimer les éléments de votre file d’attente. Votre fournisseur gère sa file d’attente de notification tout au long de ce processus. ainsi, en cas de défaillance, vous pouvez renvoyer des notifications à l’indexeur.

Pour implémenter des notifications gérées par le fournisseur, vous devez implémenter les éléments suivants :

-   Mécanisme permettant de surveiller les modifications apportées à votre magasin de données.
-   Structure de données pour les informations de mise en file d’attente (plusieurs structures de [**\_ \_ modification d’élément de recherche**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) ) relatives à ces modifications.
-   Interface [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) pour envoyer vos notifications à l’indexeur et recevoir des accusés de réception de notification de l’indexeur.
-   Interface [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) pour recevoir des mises à jour sur l’état de l’indexation.

### <a name="notifications-queue"></a>File d’attente des notifications

Vous devez surveiller et mettre en file d’attente chaque modification de votre magasin de données à envoyer à l’indexeur en tant que notification. Le nombre de notifications mises en file d’attente et la fréquence à laquelle vous les envoyez à l’indexeur dépend de vos circonstances. Vous pouvez peut-être envoyer un lot de notifications pour chaque *n* nombre de modifications ou après un intervalle de temps *t* , ou une combinaison des deux.

L’indexeur s’attend à ce que les notifications se trouvent dans un tableau de structures de [**\_ \_ modification d’élément de recherche**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) . vous pouvez donc choisir de stocker les informations de modification de la même façon. Toutefois, vous devez également être en mesure de mettre en correspondance les notifications que vous envoyez avec les accusés de réception et les mises à jour renvoyés par l’indexeur. Vous pouvez également être en mesure de déterminer le temps nécessaire pour obtenir les accusés de réception, afin de déterminer si/à quel moment renvoyer les notifications.

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Pour accéder à cette interface, vous devez d’abord instancier un objet [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) pour accéder à un objet [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . À partir de cet objet **ISearchCatalogManager** , vous instanciez un objet [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) et avertissez l’indexeur des modifications apportées aux données à l’aide d’un appel à la méthode **OnItemsChanged** .

Dans l’appel à cette méthode, vous incluez le nombre de modifications signalées et un tableau de structures de [**\_ \_ modification d’élément de recherche**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) . Vous revenez à un tableau de DocIds affectés par un indexeur qui représentent chaque modification, ainsi qu’un tableau de codes de saisie semi-automatique des RH indiquant si chaque URL a été acceptée pour l’indexation. Il s’agit de votre accusé de réception de l’indexeur qu’il a reçu vos notifications et qu’il est en train de préparer l’indexation des éléments.

À partir de là, l’indexeur envoie des mises à jour à l’aide de l’interface [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) .

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

Pour obtenir des mises à jour sur l’état de vos éléments et du catalogue, vous devez inscrire votre interface [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) auprès de l’indexeur afin de pouvoir envoyer des rappels. Chaque mise à jour envoyée à l’aide de [**ISearchNotifyInlineSite :: OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) identifie les éléments par ID de produit, l’état de chaque élément ([**Rechercher l' \_ \_ \_ État**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)de l’indexation) et la phase d’indexation ([**\_ \_ phase d’indexation**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)de la recherche) dans laquelle se trouvent les éléments.

Non seulement vous recevez des mises à jour sur l’état de chaque élément, comme décrit précédemment, vous obtenez également des informations importantes sur l’état du catalogue. Le service de recherche Windows peut être interrompu ou redémarré par l’utilisateur final, une application tierce ou une autre défaillance. Dans ce cas, vous avez besoin d’un moyen de déterminer les notifications à réexécuter vers l’indexeur.

La méthode [**ISearchNotifyInlineSite :: OnCatalogStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) , appelée par le service de recherche Windows, informe les clients sur l’état du catalogue à l’aide des paramètres décrits dans le tableau suivant.



| Paramètre                 | Description                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | GUID représentant la réinitialisation du catalogue. Si ce GUID change, toutes les notifications doivent être renvoyées.                                                        |
| guidCheckPointSignature   | GUID représentant le dernier point de contrôle restauré. Si ce GUID change, toutes les notifications accumulées depuis le dernier point de contrôle enregistré doivent être renvoyées. |
| dwLastCheckPointNumber    | Nombre indiquant le dernier point de contrôle enregistré.                                                                                                        |



 

 

Lorsqu’un point de contrôle de catalogue se produit, le service de recherche met à jour le *dwLastCheckPointNumber*, et toutes les notifications envoyées avant ce point de contrôle sont sûres et récupérables en cas de défaillance d’un service. Les fournisseurs de notifications doivent suivre uniquement les notifications envoyées entre les points de contrôle et les réexécuter dans le cas d’une restauration ou d’une réinitialisation du catalogue.

Si une restauration de catalogue se produit, le service de recherche restaure le catalogue jusqu’au dernier point de contrôle enregistré et met à jour le *guidCheckPointSignature*. Dans ce cas, les fournisseurs de notifications doivent réexécuter toutes les notifications accumulées depuis le point de contrôle enregistré le plus récent, tel qu’il est identifié par *dwLastCheckPointNumber*.

Si une réinitialisation du catalogue doit avoir lieu, le service de recherche réinitialise l’intégralité du catalogue et met à jour le *guidCatalogResetSignature*. Le fournisseur de notifications doit réexécuter à nouveau la totalité de l’étendue de l’analyse.

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
-   Pour obtenir une vue d’ensemble du gestionnaire de catalogues et du gestionnaire de recherche de catalogue (CSM), consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).
-   Pour plus d’informations sur la création d’un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)
</dt> <dt>

[Fonctionnement des gestionnaires de protocole](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Ajout d’icônes et de menus contextuels](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemple de code : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Création d’un connecteur de recherche pour un gestionnaire de protocole](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Débogage de gestionnaires de protocole](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
