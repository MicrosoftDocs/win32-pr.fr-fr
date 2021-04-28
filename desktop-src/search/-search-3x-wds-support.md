---
description: Processus de notification dans Windows Search
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Processus de notification dans Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b37747d1ec13c3a4a865e16721c64d4a0186dbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089817"
---
# <a name="notifications-process-in-windows-search"></a>Processus de notification dans Windows Search

Cette rubrique est organisée comme suit :

-   [Vue d’ensemble du processus de notification](#overview-of-the-notifications-process)
-   [Analyses](#crawls)
-   [Notifications gérées par l’indexeur](#indexer-managed-notifications)
-   [Notifications gérées par le fournisseur](#provider-managed-notifications)
-   [Notifications sur les ensembles de lignes](#notifications-on-rowsets)
-   [Rubriques connexes](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Vue d’ensemble du processus de notification

Il existe trois approches permettant d’indexer les données de votre magasin de données :

-   Analyses
-   Notifications gérées par l’indexeur
-   Notifications gérées par le fournisseur

Les avantages de chaque approche sont décrits dans les sections suivantes.

## <a name="crawls"></a>Analyses

Les sources prenant en charge les notifications effectuent une analyse incrémentielle au démarrage, puis s’appuient sur des notifications ou une commande explicite pour une nouvelle analyse. Cela se produit automatiquement sur Windows Vista et versions ultérieures. Sur les systèmes d’exploitation antérieurs à Windows Vista, vous devez configurer un événement planifié dans le [Planificateur de tâches](../taskschd/task-scheduler-start-page.md) qui appelle votre code pour lancer une analyse sur vos pages de démarrage. Vous n’avez pas besoin d’implémenter une forme de notifications. En tant que processus en arrière-plan, l’indexeur parcourt sa portée d’analyse, en recherchant des modifications et en mettant à jour le catalogue. Cette option est recommandée pour presque toutes les situations.

## <a name="indexer-managed-notifications"></a>Notifications de Indexer-Managed

Avec les notifications gérées par l’indexeur, vous implémentez une stratégie de notification qui notifie l’indexeur lorsque les données du magasin de données ont changé, et l’indexeur gère le suivi des notifications et l’indexation des données. Dans ce cas, votre composant (que nous appelons un fournisseur de notifications) surveille le magasin de données, collecte des informations sur les modifications apportées au magasin, puis avertit périodiquement l’indexeur avec une liste d’éléments nécessitant une indexation. L’indexeur est responsable de la récupération et de la résolution des notifications en cas d’échec. Cette option, que vous pouvez considérer comme la stratégie « envoyer et oublier », réduit la fréquence des analyses de l’indexeur.

## <a name="provider-managed-notifications"></a>Notifications de Provider-Managed

Avec les notifications gérées par le fournisseur, vous implémentez une stratégie de notification qui est similaire à la deuxième approche, sauf que votre fournisseur de notifications doit effectuer le suivi des notifications et est responsable de la récupération et de la résolution des notifications en cas de défaillance. Dans ce cas, votre fournisseur de notifications surveille le magasin de données, collecte et gère les informations relatives aux modifications apportées au magasin, notifie périodiquement l’indexeur avec une liste d’éléments nécessitant une indexation, reçoit des mises à jour d’état de l’indexeur et envoie de nouveau des notifications en cas d’échec.

> [!Note]  
> Cette option n’est **pas recommandée, sauf si** vous pensez que les analyses incrémentielles de votre magasin de données entravent considérablement les performances et que vous avez besoin d’un contrôle granulaire sur l’état de l’indexation.

 

## <a name="notifications-on-rowsets"></a>Notifications sur les ensembles de lignes

Dans Windows 7 et versions ultérieures, l’indexation des événements permet aux fournisseurs de recevoir des notifications sur leurs ensembles de lignes. Les fournisseurs qui utilisent l’événement d’indexation peuvent gérer leurs ensembles de lignes d’une manière qui ressemble au comportement des emplacements de système de fichiers réels. Les bibliothèques et les recherches sont des exemples principaux d’emplacements non-système de fichiers dans Windows 7. L’événement d’indexeur consiste à afficher les vues de la bibliothèque en tant que notifications dans les vues de dossiers de fichiers. L’interface [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) doit être implémentée afin de recevoir des notifications d’événements. La couche de données est le client principal de l’indexation des événements et décide de ce qu’il faut faire avec les événements dans l’interface utilisateur de la vue éléments. Pour plus d’informations, consultez [indexation des priorités et des événements d’ensemble de lignes dans Windows 7](indexing-prioritization-and-rowset-events.md).

En revanche, dans Windows Vista, les vues basées sur les requêtes n’ont pas d’événements associés, à l’exception du cache du Shell pour les modifications de propriété de fichier. Lorsque vous effectuez une recherche, les résultats retournés sont statiques. Par conséquent, si un autre document est ajouté à votre système qui correspond à votre terme de recherche, votre affichage n’est pas mis à jour pour inclure le nouvel ajout. Ce comportement est standard pour les résultats Web statiques. Toutefois, les résultats statiques sont moins acceptables lorsque vous essayez de fournir une vue basée sur une requête sur un emplacement de stockage. Les utilisateurs s’attendent à ce que le contenu de l’indexeur soit à jour. Pour plus d’informations, consultez [notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md). Pour obtenir de la documentation de référence, consultez [interfaces de notifications](-search-notifications-interfaces-entry-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexation, interrogation et notifications dans Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Ce qui est inclus dans l’index](-search-indexing-process-overview.md)
</dt> <dt>

[Processus d’indexation dans la recherche Windows](-search-indexing-process-overview.md)
</dt> <dt>

[Interrogation du processus dans la recherche Windows](querying-process--windows-search-.md)
</dt> <dt>

[Configuration requise pour la mise en forme des URL](url-formatting-requirements.md)
</dt> </dl>

 

 
