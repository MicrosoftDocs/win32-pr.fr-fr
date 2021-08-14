---
title: À propos de TBS
description: Service système qui permet le partage transparent des ressources du Module de plateforme sécurisée (TPM) (GPC).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- Services de base TPM (TBS), à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4997bf6181a1da7aabaf811d0f1d0cf3e3ca813bb11a8f2d73b3b286e4e5ebde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954450"
---
# <a name="about-tbs"></a>À propos de TBS

La fonctionnalité des services de base du module de plateforme sécurisée (TBS) est un service système qui permet le partage transparent des ressources du Module de plateforme sécurisée (TPM) (GPC). Il partage simultanément les ressources TPM entre plusieurs applications sur le même ordinateur physique, même si ces applications s’exécutent sur des machines virtuelles différentes. à partir de Windows 8 et Windows Server 2012, TBS est préinstallé sur tous les systèmes avec un module de plateforme sécurisée (TPM).

Le Trusted Computing Group (TCG) définit un Module de plateforme sécurisée (TPM) qui fournit des fonctions de chiffrement conçues pour fournir une confiance dans la plateforme. Étant donné que le module de plateforme sécurisée est implémenté dans le matériel, il dispose de ressources limitées. Le TCG définit également une pile de logiciels qui utilise ces ressources pour fournir des opérations approuvées pour les logiciels d’application. Toutefois, il n’est pas possible d’exécuter une implémentation TSS côte à côte avec des logiciels de système d’exploitation qui peuvent également utiliser des ressources TPM. La fonctionnalité TBS résout ce problème en permettant à chaque pile logicielle qui communique avec TBS d’utiliser la vérification des ressources TPM pour toutes les autres piles logicielles qui peuvent s’exécuter sur l’ordinateur.

La spécification TPM et la spécification de la pile de logiciels TCG (TSS) sont disponibles à l’adresse [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

TBS est implémenté en tant que service hors processus qui accepte les commandes qui utilisent un service RPC. Une bibliothèque liée de manière dynamique présente l’interface du langage C et communique avec le service TBS.

> [!Note]  
> Le service TBS accepte uniquement les demandes RPC de la part de l’ordinateur local.

 

Les principaux objectifs du TBS sont les suivants :

-   Fournir un partage efficace des ressources TPM limitées, telles que des emplacements de clés, des emplacements de sessions d’autorisation et des emplacements de transport.
-   Fournir un accès par ordre de priorité et synchronisé aux ressources du module de plateforme sécurisée entre plusieurs instances de piles de logiciels TPM.
-   Fournir une gestion appropriée des ressources du module de plateforme sécurisée dans les États d’alimentation.
-   Empêcher les piles de logiciels du module de plateforme sécurisée d’accéder aux commandes du module de plateforme sécurisée qui doivent être limitées, en raison des limitations de la plateforme ou des exigences administratives.

L’illustration suivante montre la relation entre le TBS et le module de plateforme sécurisée.

![relation entre le TBS en mode utilisateur et le module de plateforme sécurisée en mode noyau](images/tbs-block-diagram-as11601.png)

 

 




