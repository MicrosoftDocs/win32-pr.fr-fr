---
title: Événements (Windows Remote Management)
description: Le service collecteur d’événements utilise le protocole WS-Management pour collecter des événements à partir d’ordinateurs distants.
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06f96877904a5e76ea61a6b2f636e962e4dbd9b9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383563"
---
# <a name="events-windows-remote-management"></a>Événements (Windows Remote Management)

Le service collecteur d’événements utilise le protocole WS-Management pour collecter des événements à partir d’ordinateurs distants. Avec le service collecteur d’événements, vous pouvez créer des abonnements à des événements Windows sur des ordinateurs distants et des événements matériels générés par les contrôleurs de gestion de la carte de contrôleurs BMC. Contrôleurs BMC doit prendre en charge le protocole WS-Management.

Lorsque vous créez un abonnement, les événements sont transférés à l’ordinateur sur lequel l’abonnement a été créé. Ils s’affichent dans la observateur d’événements.

Les événements matériels générés par l’interface de gestion de plateforme intelligente (IPMI) sur les ordinateurs Windows sont collectés localement à l’aide du pilote IPMI et stockés dans le journal des événements matériels, après quoi ils peuvent être transférés comme d’autres événements du système d’exploitation Windows.

Vous pouvez créer des abonnements à l’aide de l’outil de ligne de commande Wecutil.exe. Pour plus d’informations sur l’utilisation de cet outil, à l’invite de commandes, tapez **wecutil/ ?**. Pour plus d’informations sur le service collecteur d’événements, consultez [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector).

> [!Note]  
> Les API Windows Remote Management requièrent que toutes les adresses IPv6 soient placées entre crochets.

 

> [!Caution]
>
> Lorsque vous utilisez des abonnements déclenchés par le collecteur, limitez le nombre d’ordinateurs distants à 500 et isolez le service [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) dans un processus hôte distinct.
>
> Une erreur de connexion contiendra un thread jusqu’à ce qu’il expire. Un grand nombre d’erreurs de connexion simultanées peuvent entraîner l’épuisement du pool de threads et rendre le serveur sans réponse.

 

 

 
