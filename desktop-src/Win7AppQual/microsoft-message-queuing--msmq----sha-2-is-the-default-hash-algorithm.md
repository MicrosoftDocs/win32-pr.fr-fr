---
description: Microsoft Message Queuing (MSMQ)-SHA 2 est l’algorithme de hachage par défaut
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: Microsoft Message Queuing (MSMQ)-SHA 2 est l’algorithme de hachage par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3c54832d953e50f3b912fdf36374faa8ff9ed0466587f7ac3fed2572eb3b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053037"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a>Microsoft Message Queuing (MSMQ)-SHA 2 est l’algorithme de hachage par défaut

## <a name="affected-platforms"></a>Plateformes affectées

 **Clients** -Windows XP, Windows Vista, Windows 7  
**serveurs** -Windows server 2003, Windows server 2008, Windows server 2008 R2  










## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

dans Windows 7, MSMQ utilise SHA-2 comme valeur par défaut lors de la signature d’un message sortant. En outre, tous les messages entrants doivent être signés avec SHA-2. Vous pouvez activer la prise en charge d’un algorithme de chiffrement inférieur via une clé de Registre accessible par l’administrateur.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

-   msmq dans Windows 2003 ou versions antérieures n’acceptera pas les messages signés provenant de MSMQ dans Windows 7
-   MSMQ dans Windows 7 n’accepte pas les messages signés provenant de Windows 2008 ou inférieur

## <a name="mitigation"></a>Limitation des risques

les utilisateurs doivent envisager une mise à niveau vers Windows 7 pour tirer parti de l’algorithme de signature plus fort. pour activer l’échange de messages signés de manière transparente entre Windows 7 et tout système d’exploitation de niveau supérieur, l’administrateur doit ajouter des exceptions appropriées sur les ordinateurs MSMQ.

 

 



