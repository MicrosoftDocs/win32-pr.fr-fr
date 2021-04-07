---
title: Publication dans un conteneur de système de domaine
description: Le conteneur système d’une partition de domaine contient des informations opérationnelles par domaine.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publication dans un conteneur de système de domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839274"
---
# <a name="publishing-in-a-domain-system-container"></a>Publication dans un conteneur de système de domaine

Le conteneur système d’une partition de domaine contient des informations opérationnelles par domaine. Cela comprend la stratégie de sécurité locale par défaut, le suivi des liaisons de fichiers, les réunions réseau et les conteneurs pour les points de connexion de résolution et d’inscription Windows Sockets (RnR) et de service de noms RPC (RpcNs). Le conteneur système est masqué par défaut et fournit un emplacement pratique pour le stockage des objets qui présentent un intérêt pour les administrateurs, mais pas pour les utilisateurs finaux.

Les services qui ne sont pas liés à un seul hôte peuvent créer leur SCP sous le conteneur système d’une partition de domaine. Cette alternative peut être utile pour les services dont les réplicas sont installés sur plusieurs hôtes, chaque réplica fournissant des services identiques aux clients dans l’ensemble du domaine. Elle vous permet de regrouper tous les objets pour le service répliqué sous un seul conteneur.

Les services qui créent des objets spécifiques au service dans le conteneur système doivent effectuer les opérations suivantes :

1.  Créez un sous-conteneur de **conteneur** de classe d’objets en tant qu’enfant immédiat du conteneur système. Donnez à ce sous-conteneur un nom qui l’identifie clairement comme appartenant au service.
2.  Créez les objets liés au service dans ce sous-conteneur. Par exemple, NetMeeting utilise le conteneur de réunions pour publier les objets de réunion réseau.

Un fournisseur avec plusieurs produits peut utiliser une stratégie similaire pour regrouper des objets liés au service pour tous ses produits. Dans ce cas, vous pouvez créer un objet **conteneur** avec un nom qui identifie clairement le fournisseur ; Ensuite, créez des objets **conteneurs** pour chaque service en tant qu’enfants du conteneur du fournisseur. Créez le conteneur spécifique au fournisseur en tant qu’enfant du conteneur système.

 

 




