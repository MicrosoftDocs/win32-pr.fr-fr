---
description: Le gestionnaire de contrôle des services (SCM) est démarré au démarrage du système. Il s’agit d’un serveur d’appel de procédure distante (RPC), afin que les programmes de configuration de service et de contrôle de service puissent manipuler des services sur des ordinateurs distants.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gestionnaire de contrôle des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37d651a96f9685fa82b5ea92ebb3a0b72d80bfc62cd0db80729ec1cb95acc45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889032"
---
# <a name="service-control-manager"></a>Gestionnaire de contrôle des services

Le gestionnaire de contrôle des services (SCM) est démarré au démarrage du système. Il s’agit d’un serveur d’appel de procédure distante (RPC), afin que les programmes de configuration de service et de contrôle de service puissent manipuler des services sur des ordinateurs distants.

Les fonctions de service fournissent une interface pour les tâches suivantes effectuées par le SCM :

-   Maintenance de la base de données des services installés.
-   Démarrage des services et des services de pilote lors du démarrage du système ou à la demande.
-   Énumération des services installés et des services de pilote.
-   Gestion des informations d’État pour les services en cours d’exécution et les services de pilote.
-   Transmission des demandes de contrôle aux services en cours d’exécution.
-   Verrouillage et déverrouillage de la base de données du service.

Les sections suivantes décrivent le SCM plus en détail :

-   [Base de données des services installés](database-of-installed-services.md)
-   [Démarrage automatique des services](automatically-starting-services.md)
-   [Démarrage des services à la demande](starting-services-on-demand.md)
-   [Liste des enregistrements de service](service-record-list.md)
-   [Handles SCM](scm-handles.md)

 

 



