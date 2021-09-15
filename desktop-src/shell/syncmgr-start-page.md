---
description: Le gestionnaire de synchronisation fournit une technologie centralisée et standard pour la synchronisation des fichiers en vue d’une utilisation hors connexion sur un ordinateur portable ou sur un ordinateur connecté à un réseau local.
title: gestionnaire de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522328"
---
# <a name="synchronization-manager"></a>gestionnaire de synchronisation

## <a name="purpose"></a>Objectif

Le gestionnaire de synchronisation fournit une technologie centralisée et standard pour la synchronisation des fichiers en vue d’une utilisation hors connexion sur un ordinateur portable ou sur un ordinateur connecté à un réseau local. Avec les fonctions de connectivité, les notifications (service de notification d’événements système) et la mise en cache côté client, le gestionnaire de synchronisation fournit une infrastructure pour prendre en charge l’informatique mobile. Au lieu que chaque application implémente sa propre technologie pour mettre en cache et synchroniser les ressources réseau pour une utilisation locale, le système d’exploitation fournit un modèle intégré que toutes les applications peuvent utiliser. Les fichiers sont synchronisés indépendamment du protocole. Par exemple, un programme de messagerie peut transférer ses messages à l’aide du protocole SMTP, NMTP ou POP3, tandis qu’un navigateur peut utiliser le protocole HTTP, et une base de données peut utiliser l’appel de procédure distante (RPC). Les développeurs peuvent utiliser l’interface commune au gestionnaire de synchronisation dans leurs applications pour synchroniser les fichiers entre l’ordinateur local de l’utilisateur et le stockage réseau.

## <a name="where-applicable"></a>Le cas échéant

Le gestionnaire de synchronisation est destiné aux applications qui s’exécutent principalement sur des ordinateurs portables. Les applications qui s’exécutent sur des ordinateurs connectés à des réseaux locaux à latence élevée peuvent également tirer parti de l’utilisation du gestionnaire de synchronisation.

## <a name="developer-audience"></a>Développeurs concernés

Ce document est destiné aux développeurs de logiciels qui développent des applications pour l’informatique mobile et des réseaux locaux à latence élevée. Ce document fournit une référence complète de toutes les parties du gestionnaire de synchronisation, y compris les méthodes et les interfaces du gestionnaire de synchronisation.

## <a name="run-time-requirements"></a>Conditions d’exécution

requiert Windows Server 2003, Windows XP, Windows 2000 ou Windows millennium edition (Windows Me). également disponible en tant que redistribuable pour Microsoft Windows NT 4,0, Windows 98 et Windows 95.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                       | Description                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos du gestionnaire de synchronisation](syncmgr-about.md)<br/>                               | Le gestionnaire de synchronisation fournit une technologie centralisée et standard pour la synchronisation des fichiers en vue d’une utilisation hors connexion sur un ordinateur local.<br/>     |
| [Configurations de l’informatique mobile](syncmgr-mobile-computing-configs.md)<br/>          | Les applications peuvent utiliser le gestionnaire de synchronisation pour conserver les fichiers et les ressources mis en cache localement et synchronisés sur les ordinateurs de bureau et mobiles.<br/> |
| [Scénarios d’application](syncmgr-app-scenarios.md)<br/>                               | Applications et services pouvant utiliser le gestionnaire de synchronisation.<br/>                                                                          |
| [Architecture du gestionnaire de synchronisation](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [Utilisation du gestionnaire de synchronisation à partir d’un programme](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [Informations de référence sur le gestionnaire de synchronisation](syncmgr-reference.md)<br/>                       | Les éléments de programmation suivants composent l’API pour le gestionnaire de synchronisation.<br/>                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du service de notification d’événements système](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
