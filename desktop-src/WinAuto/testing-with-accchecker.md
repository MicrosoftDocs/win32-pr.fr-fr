---
title: Test avec AccChecker
description: Décrit le flux de travail de test classique qui incorpore AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- test avec AccChecker
- AccChecker, test du flux de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507071"
---
# <a name="testing-with-accchecker"></a>Test avec AccChecker

Le scénario suivant décrit les étapes que vous suivez généralement lors des tests avec AccChecker.

> [!Note]  
> Lorsque les routines de vérification AccChecker sont en cours d’exécution, l’interaction de l’utilisateur avec l’ordinateur hôte peut interférer avec certaines routines. Nous vous recommandons de ne pas avoir d’interaction avec l’utilisateur tant que AccChecker n’a pas averti l’utilisateur que toutes les tâches sont terminées.

 

1.  Exécutez des vérifications AccChecker sur une application ou un contrôle cible spécifique. Pour plus d’informations, consultez l' [onglet vérifications](the-accchecker-graphical-user-interface.md).
    > [!Note]  
    > AccChecker n’explore pas toutes les permutations d’interface utilisateur dans une application. Les éléments masqués dans des contrôles tels que des fenêtres, des volets, des onglets et des menus doivent être exposés manuellement.

     

2.  Examinez le journal des erreurs AccChecker et évaluez ou triez les résultats. Corrigez les problèmes noordinaires et consignez les bogues graves comme il convient.
3.  Générez un fichier de suppression pour les bogues et les erreurs qui peuvent être ignorés jusqu’au test de régression.
4.  Réexécutez les vérifications AccChecker avec le fichier de suppression et les correctifs de bogues initiaux. Cela fournit un instantané des problèmes de l’implémentation actuelle de Microsoft Active Accessibility et établit une ligne de base pour les tests de régression.
5.  Intégrez les API AccChecker et le fichier de suppression dans une infrastructure de tests automatisés pour le test de régression sur les bogues enregistrés à partir des vérifications AccChecker initiales.
    > [!Note]  
    > À mesure que les bogues sont résolus, le fichier de suppression doit être modifié en fonction des besoins.

     

6.  Confirmez qu’aucune régression ou nouveau bogue d’accessibilité n’a été introduit dans l’application ou le contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
</dt> </dl>

 

 




