---
title: Réservations d’espaces de noms, inscriptions et routage
description: La réservation et l’inscription sont les opérations par lesquelles l’API du serveur HTTP donne accès à l’espace de noms d’URL sur un ordinateur.
ms.assetid: dc66960b-36cd-4c09-be0a-3aec9a8a25d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6ad1e585487b03fa33448ddb99b6f1c7eaa779c56cd6fd1d07d4e73df2ea1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823169"
---
# <a name="namespace-reservations-registrations-and-routing"></a>Réservations d’espaces de noms, inscriptions et routage

La réservation et l’inscription sont les opérations par lesquelles l’API du serveur HTTP donne accès à l’espace de noms d’URL sur un ordinateur. Les applications peuvent s’inscrire pour une partie de l’espace de noms de l’URL afin de traiter les demandes des clients HTTP. L’application inscrit un espace de noms auprès de l’API du serveur HTTP à l’aide de la fonction [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . L’API du serveur HTTP ajoute les URL à la file d’attente des demandes pour l’application et achemine les requêtes vers les applications en fonction des URL dans leurs files d’attente. Pour que l’application puisse s’inscrire pour recevoir des demandes d’espace de noms d’URL, l’administrateur système doit faire une réservation pour cette URL pour le compte de l’utilisateur qui exécute l’application. Par défaut, l’espace de noms est fermé, c’est-à-dire que seul l’administrateur peut inscrire UrlPrefixes jusqu’à ce que l’administrateur entre une réservation.

Une réservation alloue de façon permanente une partie de l’espace de noms d’URL à des utilisateurs individuels, ce qui leur permet de réserver ou de « posséder » cette partie de l’espace de noms. Les réservations donnent à l’utilisateur le droit de s’inscrire aux demandes de service pour l’espace de noms. L’API du serveur HTTP garantit que les utilisateurs n’inscrivent pas les URL à partir de portions de l’espace de noms qu’ils ne possèdent pas. Pour garantir la sécurité de l’espace de noms, les listes de contrôle d’accès (liste Access Control) sont appliquées à la partie de l’espace de noms réservée pour chaque utilisateur.

Les espaces de noms réservés sont identifiés par des chaînes de préfixe d’URL, mis en forme de la même façon que les préfixes d’URL utilisés pour les inscriptions. Cela signifie que toutes les différentes catégories de spécificateurs d’hôte sont également disponibles pour les réservations.

Les réservations d’espaces de noms sont conservées entre les redémarrages et les modifications prennent effet de manière dynamique, de sorte qu’il n’est pas nécessaire d’arrêter et de redémarrer l’ordinateur.

Les concepts suivants sont expliqués plus en détail lorsqu’ils s’appliquent au processus d’inscription et de réservation d’espaces de noms.

-   Abonnement. L’inscription est l’opération par laquelle une application indique un intérêt à recevoir des demandes pour un UrlPrefix spécifié. L’API pour l’inscription de l’URL est [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl). L’inscription se produit généralement lors du démarrage de l’application et doit être effectuée à chaque démarrage de l’application.
-   Achemine. Le routage est effectué par l’API du serveur HTTP pour déterminer l’application vers laquelle distribuer la demande, en fonction du meilleur [URLPrefix](urlprefix-strings.md) correspondant inscrit et/ou réservé. L’opération de routage utilise à la fois les informations d’inscription et de réservation.
-   Réserve. La réservation alloue une partie de l’espace de noms d’URL à un ou plusieurs utilisateurs. Cette opération permet aux utilisateurs de s’inscrire à l’espace de noms spécifié. Un utilisateur pour lequel un espace de noms est réservé est dit « propre », qui fait partie de l’espace de noms de l’URL. Les réservations d’espaces de noms sont généralement effectuées au cours de l’installation de l’application et sont des opérations peu fréquentes. Les réservations sont conservées entre les redémarrages de l’ordinateur et requièrent des privilèges d’administrateur sur l’ordinateur ou la propriété avec des privilèges de délégation pour créer ou supprimer.
-   Délégation. Les privilèges de délégation permettent à un utilisateur qui possède un espace de noms de transmettre la propriété d’une sous-arborescence à un autre utilisateur par une réservation ultérieure. Les privilèges de délégation sont accordés à un utilisateur par l’administrateur système lorsque la réservation est effectuée. Un ou plusieurs utilisateurs peuvent se voir attribuer des privilèges de délégation à un espace de noms.

 

 




