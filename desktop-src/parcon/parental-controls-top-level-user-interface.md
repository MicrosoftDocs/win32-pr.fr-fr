---
description: Contrôle parental Top-Level interface utilisateur
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: Contrôle parental Top-Level interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321475097e25b812aca8d1e65f8b88843ebb1055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529867"
---
# <a name="parental-controls-top-level-user-interface"></a>Contrôle parental Top-Level interface utilisateur

Le lien fort entre la sécurité des familles et les comptes d’utilisateurs Windows a entraîné une catégorie combinée qui apparaît comme **comptes d’utilisateur et sécurité des familles** dans le panneau de configuration pour les références de Windows Vista orientées consommateur.

> [!Note]  
> La catégorie apparaît en tant que **comptes d’utilisateurs** lorsqu’un ordinateur avec la fonctionnalité de jonction de domaine est joint.

 

Si un compte d’utilisateur standard n’a pas encore été configuré pour l’utilisateur contrôlé, un lien dans le panneau de configuration fournit un flux de travail simple pour ajouter un nouveau compte contrôlé de manière parente.

Une fois qu’un compte est créé, le panneau de configuration du contrôle parental expose les fonctionnalités de niveau supérieur pour l’utilisateur contrôlé. Html

-   Options globales de contrôle parental pour les cases d’option.
-   Cases d’option de contrôle de l’activité indépendante.
-   Une section de paramètres avec le lien restrictions Web implémentées par Microsoft, qui est indiquée de manière conditionnelle, et les types de restrictions implémentés principaux de Microsoft en mode hors connexion sont affichés.
-   Une autre zone de paramètres qui s’affiche si les extensions d’interface utilisateur sont inscrites par Microsoft ou par des tiers.
-   Zone d’état résumé qui indique le nom d’utilisateur et la vignette, le lien Afficher les rapports d’activité et l’état des paramètres de contrôle parental. Si la valeur est on, l’affichage comprend le niveau du paramètre de filtre de contenu Web (si le filtre Microsoft est actif) ou le nom du filtre en cas de remplacement par une extension tierce, ainsi que l’état des paramètres hors connexion de l’utilisateur.

La case d’option Activer le contrôle parental global est définie initialement à l’état désactivé. Lorsqu’il est activé par un administrateur, la création de rapports d’activité est également activée par défaut, mais peut être désactivée indépendamment. Comme avec presque tous les paramètres du contrôle parental, la configuration peut être effectuée par programme par le biais des API disponibles.

 

 



