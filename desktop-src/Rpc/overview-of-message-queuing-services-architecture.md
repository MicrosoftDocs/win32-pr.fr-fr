---
title: Vue d’ensemble de l’architecture des services Message Queuing
description: Les services de Message Queuing (MSMQ) utilisent un modèle site/entreprise. En règle générale, un site est un emplacement physique, tel qu’un immeuble. Une entreprise se compose d’un ou de plusieurs sites et représente une organisation.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae7eb93ab7d12ab245b905e83bc129ea656d10d70602d2235304a02966020f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019313"
---
# <a name="overview-of-message-queuing-services-architecture"></a>Vue d’ensemble de l’architecture des services Message Queuing

Les services de Message Queuing (MSMQ) utilisent un modèle site/entreprise. En règle générale, un site est un emplacement physique, tel qu’un immeuble. Une entreprise se compose d’un ou de plusieurs sites et représente une organisation.

Le diagramme suivant illustre l’architecture du service MSMQ.

![architecture MSMQ](images/msmq.png)

Au cœur de MSMQ se trouve la base de données MQIS (message queue Information Service), qui s’exécute sur SQL Server. une entreprise possède un MQIS maître unique, appelé contrôleur de Enterprise principal. Chaque site dispose de son propre MQIS, appelé *contrôleur de site principal* et zéro ou plusieurs *contrôleurs de site de sauvegarde*. Enfin, il existe des ordinateurs clients individuels, chacun ayant son propre gestionnaire de files d’attente, implémenté comme un service. le contrôleur de Enterprise principal peut également être un contrôleur principal de Site, et tout contrôleur peut également être un client.

Les files d’attente de messages peuvent être publiques ou privées. Les files d’attente publiques sont inscrites dans Active Directory et sont accessibles sur le réseau. Les messages d’une file d’attente publique sont routés au sein de l’entreprise, sous le contrôle de MSMQ. Les messages d’application cliente sont déplacés du gestionnaire de files d’attente du client vers la file d’attente de destination en circulant entre les gestionnaires de files d’attente des contrôleurs de site.

Les files d’attente privées sont gérées par le gestionnaire de files d’attente local et ne sont pas inscrites dans Active Directory. L’étendue des messages de file d’attente privée est limitée à l’ordinateur sur lequel ils résident.

 

 




