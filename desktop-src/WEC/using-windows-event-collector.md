---
title: Utilisation du collecteur d’événements Windows
description: Cette section répertorie les rubriques qui expliquent les tâches réalisables à l’aide du kit de développement logiciel (SDK) du collecteur d’événements Windows. Des exemples de code et des explications sur toutes les tâches sont inclus dans chacune des rubriques suivantes.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106525704"
---
# <a name="using-windows-event-collector"></a>Utilisation du collecteur d’événements Windows

Cette section répertorie les rubriques qui expliquent les tâches réalisables à l’aide du kit de développement logiciel (SDK) du collecteur d’événements Windows. Des exemples de code et des explications sur toutes les tâches sont inclus dans chacune des rubriques suivantes.

## <a name="in-this-section"></a>Dans cette section

-   [Création d’un abonnement initié par le collecteur](creating-an-event-collector-subscription.md)

    Fournit des informations et un exemple de code C++ pour créer un abonnement initié par le collecteur. Un abonnement initié par le collecteur vous permet de recevoir des événements sur un ordinateur local (le collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (une source d’événement).

-   [Configuration d’un abonnement initié par la source](setting-up-a-source-initiated-subscription.md)

    Fournit des informations et un exemple de code C++ pour la création d’un abonnement initié par la source. Un abonnement initié par la source vous permet de recevoir des événements sur un ordinateur local (le collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (une source d’événement) sans spécifier les sources d’événements dans l’abonnement.

-   [Ajout d’une source d’événement à un abonnement initié par le collecteur](adding-an-event-source-to-an-event-collector-subscription.md)

    Fournit des informations et un exemple de code C++ pour l’ajout d’une source d’événement (ordinateur local ou ordinateur distant) à un abonnement initié par le collecteur. Un abonnement initié par le collecteur ne peut pas commencer à collecter des événements tant qu’une source d’événement n’a pas été ajoutée à l’abonnement.

-   [Création d’abonnements aux événements matériels](creating-hardware-event-subscriptions.md)

    Contient des informations sur la création d’un abonnement aux événements pour recevoir des événements matériels d’un ordinateur sur lequel est installé un contrôleur BMC (Baseboard Management Controller).

-   [Suppression d’un abonnement à un collecteur d’événements](deleting-an-event-collector-subscription.md)

    Fournit des informations et un exemple de code C++ pour la suppression d’un abonnement d’un collecteur d’événements à partir d’un ordinateur local.

-   [Affichage des propriétés d’un abonnement à un collecteur d’événements](displaying-the-properties-of-an-event-collector-subscription.md)

    Fournit des informations et un exemple de code C++ permettant d’afficher les valeurs de propriété d’un abonnement au collecteur d’événements. Les valeurs de propriété peuvent fournir des informations utiles, telles que les adresses des sources d’événements, l’état de l’abonnement et des sources d’événements, ainsi que des informations sur la façon dont les événements sont remis.

-   [Affichage de l’état d’un abonnement au collecteur d’événements](displaying-the-status-of-an-event-collector-subscription.md)

    Fournit des informations et un exemple de code C++ permettant d’afficher l’état d’exécution des sources d’événements associées à un abonnement à un collecteur d’événements. Cela vous permet d’afficher les messages d’erreur qui peuvent aider à résoudre les problèmes, ce qui empêche une source d’événements de transférer des événements.

-   [Liste des abonnements du collecteur d’événements](listing-event-collector-subscriptions.md)

    Fournit des informations et un exemple de code C++ pour répertorier les abonnements qui existent sur un ordinateur local. Vous pouvez utiliser les noms d’abonnements obtenus avec cet exemple pour supprimer un abonnement, ajouter une source d’événement à un abonnement, récupérer les propriétés d’un abonnement ou afficher l’état d’un abonnement.

-   [Suppression d’une source d’événement d’un abonnement initié par le collecteur](removing-an-event-source-from-an-event-collector-subscription.md)

    Fournit des informations et un exemple de code C++ pour supprimer une source d’événement d’un abonnement initié par le collecteur. Vous pouvez supprimer une source d’événement d’un abonnement initié par le collecteur sans désactiver l’abonnement.

-   [Nouvelle tentative d’abonnement au collecteur d’événements](retrying-an-event-collector-subscription.md)

    Fournit des informations et un exemple de code C++ pour la nouvelle tentative d’abonnement d’un collecteur d’événements lorsqu’une ou plusieurs sources d’événements ont échoué. Vous pouvez réessayer une seule source d’événements ou vous pouvez réessayer l’intégralité de l’abonnement.

 

 




