---
description: Microsoft Message Queuing (MSMQ)-suppression du service de support client Windows 2000
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ)-suppression du service de support client Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088147"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ)-suppression du service de support client Windows 2000

## <a name="affected-platforms"></a>Plateformes affectées

**Serveurs** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -haute  
**Fréquence** -faible  

## <a name="description"></a>Description

Le service de support client Windows 2000 est un composant facultatif du serveur Message Queuing que vous pouvez installer sur un ordinateur contrôleur de domaine Windows 2003 ou Windows 2008. Ce service permet aux clients Windows 2000 de fonctionner en mode intégré au domaine, avec n’importe quel serveur Message Queuing installé sur les ordinateurs Windows 2003/2008. Les clients MSMQ fonctionnant sur Windows XP vers le haut n’ont pas besoin de ce service.

### <a name="manifestation-of-impact"></a>Manifeste de l’impact

Cette modification a un impact sur Windows 2000 lors de l’interopérabilité dans un domaine Windows 7 où tous les contrôleurs de domaine sont Windows Server 2008 R2. Si un client est mis à niveau vers le domaine Windows 7, les applications MSMQ existantes sur les ordinateurs Windows 2000 dans le domaine ne pourront pas fonctionner en mode intégré au domaine, sauf si ces clients sont mis à niveau vers une version plus récente de Windows.

### <a name="mitigation"></a>Limitation des risques

Les utilisateurs qui ont des ordinateurs clients Windows 2000 sur un domaine Windows 7 peuvent configurer un contrôleur de domaine Windows 2003/2008 dans le domaine et installer le service de support client de MSMQ Windows 2000 sur ce contrôleur de domaine.

### <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

Les utilisateurs qui ont des ordinateurs clients Windows 2000 exécutant MSMQ doivent effectuer une mise à niveau vers une version plus récente de Windows afin de tirer parti de l’implémentation Active Directory du serveur MSMQ.

### <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

Les utilisateurs qui ont des ordinateurs clients Windows 2000 exécutant MSMQ sur un domaine Windows 7 avec un ou plusieurs contrôleurs de domaine de niveau inférieure doivent vérifier que leurs applications sont opérationnelles sur ce domaine mixte.

 

 



