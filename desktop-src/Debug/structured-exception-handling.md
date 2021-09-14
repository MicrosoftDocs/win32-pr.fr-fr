---
description: Une exception est un événement qui se produit pendant l’exécution d’un programme et qui requiert l’exécution du code en dehors du déroulement normal du contrôle.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Gestion structurée des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114570"
---
# <a name="structured-exception-handling"></a>Gestion structurée des exceptions

Une *exception* est un événement qui se produit pendant l’exécution d’un programme et qui requiert l’exécution du code en dehors du déroulement normal du contrôle. Il existe deux types d’exceptions : les exceptions matérielles et les exceptions logicielles. Les *exceptions matérielles* sont initiées par le processeur. Ils peuvent résulter de l’exécution de certaines séquences d’instructions, telles que la division par zéro ou d’une tentative d’accès à une adresse mémoire non valide. Les *exceptions logicielles* sont initiées explicitement par les applications ou le système d’exploitation. Par exemple, le système peut détecter si une valeur de paramètre non valide est spécifiée.

La *gestion structurée des exceptions* est un mécanisme permettant de gérer les exceptions matérielles et logicielles. Par conséquent, votre code gère les exceptions matérielles et logicielles de la même manière. La gestion structurée des exceptions vous permet d’avoir un contrôle complet sur la gestion des exceptions, fournit la prise en charge des débogueurs et est utilisable dans l’ensemble des langages de programmation et des ordinateurs. La *gestion des exceptions vectorisées* est une extension de la gestion structurée des exceptions.

Le système prend également en charge la *gestion des arrêts*, ce qui vous permet de vous assurer que chaque fois qu’un corps de code protégé est exécuté, un bloc de code d’arrêt spécifié est également exécuté. Le code d’arrêt est exécuté, quelle que soit la façon dont le contrôle de workflow quitte le corps protégé. Par exemple, un gestionnaire de terminaisons peut garantir que les tâches de nettoyage sont effectuées même si une exception ou une autre erreur se produit pendant l’exécution du corps de code protégé.

-   [À propos de la gestion structurée des exceptions](about-structured-exception-handling.md)
-   [Utilisation de la gestion structurée des exceptions](using-structured-exception-handling.md)
-   [Référence de gestion structurée des exceptions](structured-exception-handling-reference.md)

 

 



