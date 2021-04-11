---
title: Message Queuing RPC
description: Message Queuing (MSMQ) permet aux utilisateurs de communiquer sur des réseaux et des systèmes, quel que soit l’état actuel des applications et systèmes communicants.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- Appel de procédure distante RPC, décrit, Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029624"
---
# <a name="rpc-message-queuing"></a>Message Queuing RPC

Message Queuing (MSMQ) permet aux utilisateurs de communiquer sur des réseaux et des systèmes, quel que soit l’état actuel des applications et systèmes communicants. Les applications envoient et reçoivent des messages via les files d’attente de messages gérées par MSMQ. Les files d’attente de messages continuent de fonctionner même lorsque l’application cliente ou serveur n’est pas en cours d’exécution. Message Queuing fournit les éléments suivants :

-   **Messagerie asynchrone.** Avec la messagerie asynchrone MSMQ, une application cliente peut envoyer un message à un serveur et effectuer un retour immédiatement, même si l’ordinateur cible ou le programme serveur ne répond pas.
-   **Remise des messages garantie.** Lorsqu’une application envoie un message via MSMQ, le message atteint sa destination même si l’application de destination n’est pas en cours d’exécution en même temps ou si les réseaux et systèmes sont hors connexion.
-   **Le routage et la configuration dynamique.** MSMQ assure un routage flexible sur des réseaux hétérogènes. La configuration de ces réseaux peut être modifiée de manière dynamique sans modification majeure des systèmes et réseaux eux-mêmes.
-   **Messagerie sans connexion.** Les applications utilisant MSMQ n’ont pas besoin de configurer des sessions directes avec les applications cibles.
-   [Sécurité](security.md). MSMQ fournit une communication sécurisée basée sur la sécurité Windows et l’API de chiffrement (CryptoAPI) pour le chiffrement et les signatures numériques.
-   **Messagerie hiérarchisée.** MSMQ transfère les messages sur les réseaux en fonction de leur priorité, ce qui permet une communication plus rapide pour les applications critiques.

Microsoft RPC étend le modèle OSF (Open Software Foundation – Data communication Equipment) pour les appels de procédure distante en permettant aux applications distribuées d’utiliser MSMQ comme transport et de contrôler un grand nombre de ses fonctionnalités. Cette fonctionnalité est disponible à la fois pour les applications RPC conventionnelles et, via l’interface **IRPCOptions** , aux applications com.

> [!Note]  
> La mise en file d’attente des messages RPC est disponible uniquement sur Windows 2000. Les versions ultérieures de Windows ne prennent pas en charge la mise en file d’attente de messages RPC.

 

Les rubriques suivantes fournissent une vue d’ensemble de Message Queuing :

-   [Vue d’ensemble de l’architecture des services Message Queuing](overview-of-message-queuing-services-architecture.md)
-   [Propriétés des messages et des files d’attente de messages](message-and-message-queue-properties.md)
-   [Utilisation de MSMQ en tant que transport RPC](using-msmq-as-an-rpc-transport.md)
-   [Configuration système requise pour les applications RPC-message \_ Queuing](system-requirements-for-rpc-message-queuing-applications.md)
-   [Développement d’applications de mise en file d’attente RPC-Message](developing-rpc-message-queuing-applications.md)
-   [Services de sécurité MSMQ](msmq-security-services.md)

 

 




