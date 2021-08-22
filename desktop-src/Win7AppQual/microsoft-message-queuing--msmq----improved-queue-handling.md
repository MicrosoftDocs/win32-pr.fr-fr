---
description: Microsoft Message Queuing (MSMQ)-amélioration de la gestion des files d’attente
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ)-amélioration de la gestion des files d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4de125062dfdd705165e83e8a34d2bc0ef595eb08b6152d37aed5520e9ed39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053057"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ)-amélioration de la gestion des files d’attente

## <a name="platforms"></a>Plateformes

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

Le service MSMQ n’a pas de limite matérielle sur le nombre de files d’attente qui peuvent être créées sur un système. Toutefois, les performances du système sont affectées lors de la création d’un grand nombre de files d’attente. Plus précisément, lorsqu’il y a plus de quelques milliers de files d’attente, le temps de démarrage du service MSMQ augmente de façon exponentielle, ce qui a un impact visible.

Microsoft a optimisé le démarrage du Service MSMQ dans Windows 7 pour réduire la surcharge de recherche pour le chargement des files d’attente en mémoire. Cette optimisation a entraîné une amélioration spectaculaire du temps de démarrage du service MSMQ, même lorsque plusieurs milliers de files d’attente sont créées dans le système.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Cette amélioration des performances n’a pas d’impact sur les fonctionnalités d’une application existante.

## <a name="leveraging-the-changed-feature"></a>Tirer parti de la fonctionnalité modifiée

les développeurs d’applications qui utilisent MSMQ sur Windows 7 peuvent désormais concevoir leurs solutions sans limiter le nombre de files d’attente. Notez que le nombre de files d’attente affecte toujours les performances globales du serveur MSMQ, mais l’impact sur les performances est désormais linéaire au lieu d’une mise à l’échelle exponentielle.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Compatibilité, performances, fiabilité et tests d’utilisation

Si vous utilisez un grand nombre de files d’attente, Simulez l’environnement de production sur un banc d’essai, surveillez les performances et analysez le temps de démarrage du service et le débit des messages avec un grand nombre de files d’attente et de messages présents dans le système de test.

 

 



