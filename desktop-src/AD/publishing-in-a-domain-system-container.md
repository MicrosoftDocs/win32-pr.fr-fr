---
title: Publication dans un conteneur de système de domaine
description: Le conteneur système d’une partition de domaine contient des informations opérationnelles par domaine.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publication dans un conteneur de système de domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb86a49bb14bc88d64a723ca9ab289723ff4ac2b9259f112323e19a04497362c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184953"
---
# <a name="publishing-in-a-domain-system-container"></a>Publication dans un conteneur de système de domaine

Le conteneur système d’une partition de domaine contient des informations opérationnelles par domaine. cela comprend la stratégie de sécurité locale par défaut, le suivi des liaisons de fichiers, les réunions réseau et les conteneurs pour Windows les points de connexion RnR (inscription et résolution des problèmes) et RpcNs (RPC name service). Le conteneur système est masqué par défaut et fournit un emplacement pratique pour le stockage des objets qui présentent un intérêt pour les administrateurs, mais pas pour les utilisateurs finaux.

Les services qui ne sont pas liés à un seul hôte peuvent créer leur SCP sous le conteneur système d’une partition de domaine. Cette alternative peut être utile pour les services dont les réplicas sont installés sur plusieurs hôtes, chaque réplica fournissant des services identiques aux clients dans l’ensemble du domaine. Elle vous permet de regrouper tous les objets pour le service répliqué sous un seul conteneur.

Les services qui créent des objets spécifiques au service dans le conteneur système doivent effectuer les opérations suivantes :

1.  Créez un sous-conteneur de **conteneur** de classe d’objets en tant qu’enfant immédiat du conteneur système. Donnez à ce sous-conteneur un nom qui l’identifie clairement comme appartenant au service.
2.  Créez les objets liés au service dans ce sous-conteneur. Par exemple, NetMeeting utilise le conteneur de réunions pour publier les objets de réunion réseau.

Un fournisseur avec plusieurs produits peut utiliser une stratégie similaire pour regrouper des objets liés au service pour tous ses produits. Dans ce cas, vous pouvez créer un objet **conteneur** avec un nom qui identifie clairement le fournisseur ; Ensuite, créez des objets **conteneurs** pour chaque service en tant qu’enfants du conteneur du fournisseur. Créez le conteneur spécifique au fournisseur en tant qu’enfant du conteneur système.

 

 




