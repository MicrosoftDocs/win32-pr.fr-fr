---
title: À propos de NDF
description: Network Diagnostics Framework (NDF) réduit l’implication des administrateurs réseau et des utilisateurs d’ordinateurs en gérant les problèmes réseau courants au fur et à mesure de leur apparition.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b638298fe321d314815c74fced49d3dfb623022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672726"
---
# <a name="about-ndf"></a>À propos de NDF

Network Diagnostics Framework (NDF) réduit l’implication des administrateurs réseau et des utilisateurs d’ordinateurs en gérant les problèmes réseau courants au fur et à mesure de leur apparition. En utilisant les fonctionnalités de diagnostic et de réparation d’NDF, les utilisateurs et les administrateurs n’ont pas besoin d’outils supplémentaires pour gérer certains problèmes relativement courants. NDF est fourni avec Windows Vista, Windows Server 2008 et versions ultérieures. Elle est disponible chaque fois qu’un système est démarré (mais ne peut pas être exécuté en mode sans échec).

## <a name="ndf-helper-classes"></a>Classes d’assistance NDF

NDF comprend des classes d’assistance qui diagnostiquent les problèmes de mise en réseau à mesure qu’ils se produisent. Chacune de ces classes d’assistance contient la logique requise pour dépanner au moins un composant ou une application.

Les classes d’assistance NDF individuelles effectuent les tâches principales de la session de diagnostic. Chaque classe d’assistance est une unité de code conçue pour évaluer un aspect d’intégrité de son composant réseau respectif. La classe d’assistance comprend également les options de réparation possibles disponibles pour restaurer l’intégrité du composant, ainsi que le coût et le risque d’une option de réparation particulière.

Chaque classe d’assistance se connecte à l’infrastructure de diagnostics réseau globale. Si un composant réseau tiers comprend une classe d’assistance NDF, les problèmes liés à ce composant peuvent être résolus par d’autres applications utilisant NDF, sans qu’il soit nécessaire d’avoir une connaissance spécifique de ce composant.

Les classes d’assistance développées par Microsoft fournissent aux développeurs de logiciels les fonctionnalités de diagnostic et de réparation principales. Il existe également un petit ensemble d’API que les développeurs peuvent utiliser pour diagnostiquer les problèmes réseau à l’aide d’NDF. Pour plus d’informations, consultez l’exemple des [fonctions NDF](ndf-functions.md) et des [Diagnostics NDF](ndf-diagnostics-example.md).

## <a name="extensible-helper-classes"></a>Classes d’assistance extensibles

Dans certains cas, des fonctionnalités de diagnostic et de réparation plus spécifiques peuvent être fournies par les développeurs d’applications.

Certaines des classes d’assistance NDF de Microsoft sont conçues pour être étendues afin de fournir des fonctionnalités de diagnostic et de réparation supplémentaires. Cela signifie que les développeurs peuvent inclure des fonctionnalités permettant d’utiliser les fonctionnalités de diagnostic et de réparation NDF pour résoudre les problèmes spécifiques à leur logiciel ou matériel.

Par exemple, l’équipe sans fil de Microsoft fournit une classe d’assistance extensible qui permet à tous les fournisseurs de réseaux sans fil tiers d’ajouter une logique de dépannage spécifique pour leur matériel et/ou logiciel spécifique. Pour ce faire, ils peuvent développer une extension de classe d’assistance NDF. Pour plus d’informations, consultez [802,11 Wireless Diagnostics extensible helper classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

Une extension de classe d’assistance NDF, par définition, étend les fonctionnalités d’une classe d’assistance extensible existante. Si une classe d’assistance n’est pas extensible, personne ne peut écrire une extension pour cette classe d’assistance.

## <a name="benefits-of-helper-class-extensions"></a>Avantages des extensions de classe d’assistance

NDF offre plusieurs avantages distincts pour encourager son utilisation par les développeurs de composants réseau. La partie supérieure de la liste indique que les clients du logiciel de fournisseur peuvent libérer certaines de leurs propres ressources de dépannage et réduire le coût total de possession. Une extension de classe d’assistance bien écrite offre également les avantages suivants :

-   Permet à une équipe de déterminer quand son composant n’est pas la cause d’un problème de connectivité. Par exemple, la mise en réseau est souvent responsable des problèmes de connectivité qui ne sont pas réellement le résultat d’une défaillance d’un composant réseau. En écrivant une extension de classe d’assistance, une équipe peut plus facilement éliminer un composant particulier en raison d’un échec de connectivité.
-   Permet à une équipe de diagnostiquer et de déboguer rapidement un problème au sein du composant. Le temps passé au débogage et à la résolution des problèmes peut être éliminé si une classe d’assistance est écrite pour effectuer toutes les étapes de diagnostics standard requises.
-   Élimine la nécessité d’écrire et de prendre en charge des outils uniques pour diagnostiquer les problèmes. Une classe d’assistance peut être le référentiel central pour les fonctionnalités de diagnostic d’un composant et les techniques de collecte d’informations.
-   Rend les diagnostics spécifiques à un composant accessibles aux applications, sans qu’ils aient besoin d’avoir une connaissance directe du composant.

 

 




