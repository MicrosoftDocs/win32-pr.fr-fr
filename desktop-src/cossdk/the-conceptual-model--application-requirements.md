---
description: 'Modèle conceptuel : exigences de l’application'
ms.assetid: 124b329b-f745-45b4-b266-7c177c76a5cd
title: 'Modèle conceptuel : exigences de l’application'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a287ff940f154bf104bbb50f6362bf573d9223
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526409"
---
# <a name="the-conceptual-model-application-requirements"></a>Modèle conceptuel : exigences de l’application

Lorsque vous concevez le modèle conceptuel, vous devez définir les problèmes d’entreprise et les fonctions requises pour résoudre ces problèmes. Une approche des meilleures pratiques consiste à communiquer avec les personnes qui utiliseront réellement l’application, à rencontrer un grand nombre d’utilisateurs et à inclure autant de scénarios commerciaux ou utilisateur que possible. Déterminez les identités et le nombre d’utilisateurs potentiels du système, ainsi que la taille et l’étendue des données impliquées. Bien que la collecte de ces informations puisse être l’aspect le moins technique du processus de conception, il s’agit de l’un des plus importants. Pour développer une application réussie, vous devez avoir une compréhension claire des problèmes et des processus de l’entreprise qui doivent être traités.

Tout en déterminant les exigences de l’application, gardez à l’esprit les considérations suivantes :

-   Exigences en matière de performances. Quel est le temps de réponse attendu pour les tâches d’application ? Quelle est la prise en charge du basculement pour les serveurs inactifs ? Quelles sont les heures de disponibilité ?
-   Environnement. Quels sont les serveurs disponibles ? Des serveurs supplémentaires sont-ils prévus pour gérer les exigences de mise à l’échelle ?
-   Déploiement. Comment l’application s’intègre-t-elle à un système actuel ? Quels sont les autres systèmes avec lesquels l’application interagit ? Quels systèmes d’exploitation les autres systèmes utilisent-ils ? Quels protocoles de communication doivent être pris en charge ? Quelle API pouvez-vous utiliser pour interagir avec les autres systèmes ? Où se trouvent les autres systèmes sur le réseau ? Quelles sont les restrictions applicables à l’utilisation de l’ordinateur ? Quels sont les comptes d’utilisateurs autorisés à accéder ?
-   Lieu. Où se trouvent les données par rapport au client ? Les données sont-elles accessibles à distance ou sont-elles locales ?
-   Sécurité. Existe-t-il des exigences de chiffrement ou de vérification de l’intégrité ? Existe-t-il des exigences d’authentification ou de protection des données ?
-   Droits d’accès. Existe-t-il des contraintes sur les personnes autorisées à effectuer certaines opérations ? Dans ce cas, vous devez d’abord documenter les opérations qui nécessitent une autorisation, puis documenter les types d’utilisateurs qui peuvent avoir une autorisation. Ces exigences peuvent avoir un impact important sur la façon dont certaines parties de l’application sont implémentées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle logique : définition et planification de l’application](the-logical-model--application-definition-and-planning.md)
</dt> <dt>

[Modèle physique : architecture de l’application](the-physical-model--application-architecture.md)
</dt> </dl>

 

 



