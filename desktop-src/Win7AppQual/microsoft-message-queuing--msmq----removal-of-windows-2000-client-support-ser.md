---
description: Microsoft Message Queuing (MSMQ)-suppression du Service de Support Client Windows 2000
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ)-suppression du Service de Support Client Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bdcba684faa0a25994f66cc9cd205ba22b5ed949d8dcdd3e67497484f2784ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053047"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ)-suppression du Service de Support Client Windows 2000

## <a name="affected-platforms"></a>Plateformes affectées

**serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -haute  
**Fréquence** -faible  

## <a name="description"></a>Description

le Service de prise en charge du Client Windows 2000 est un composant facultatif du serveur Message Queuing que vous pouvez installer sur un ordinateur de contrôleur de domaine Windows 2003 ou Windows 2008. ce service permet aux clients Windows 2000 de fonctionner en mode intégré à un domaine, avec n’importe quel serveur Message Queuing installé sur Windows ordinateurs 2003/2008. les Clients MSMQ fonctionnant sur Windows XP vers le haut n’ont pas besoin de ce service.

### <a name="manifestation-of-impact"></a>Manifeste de l’impact

cette modification a un impact sur Windows 2000 lors de l’interopérabilité dans un domaine Windows 7 dans lequel tous les contrôleurs de domaine sont Windows Server 2008 R2. si un client est mis à niveau vers le domaine Windows 7, les applications MSMQ existantes sur les ordinateurs Windows 2000 dans le domaine ne pourront pas fonctionner en mode intégré au domaine, sauf si ces clients sont mis à niveau vers une version de Windows supérieure.

### <a name="mitigation"></a>Limitation des risques

les utilisateurs qui ont des ordinateurs clients Windows 2000 sur un domaine Windows 7 peuvent configurer un contrôleur de domaine Windows 2003/2008 dans le domaine et installer le Service de Support Client MSMQ Windows 2000 sur ce contrôleur de domaine.

### <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

les utilisateurs qui ont des ordinateurs clients Windows 2000 qui exécutent MSMQ doivent effectuer une mise à niveau vers une version Windows plus élevée afin de tirer parti de l’implémentation basée sur Active Directory du serveur msmq.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

les utilisateurs qui ont des ordinateurs clients Windows 2000 qui exécutent MSMQ sur un domaine Windows 7 avec un ou plusieurs contrôleurs de domaine de niveau inférieure doivent vérifier que leurs applications sont opérationnelles sur ce domaine mixte.

 

 



