---
description: le Windows Installer fournit de nombreuses actions intégrées pour exécuter le processus d’installation. Pour obtenir la liste de ces actions, consultez les informations de référence sur les actions standard.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3e2eb466934d7d332307e0d5288d6d328297d7664d884e62c406eb3409728a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947900"
---
# <a name="custom-actions"></a>Actions personnalisées

le Windows Installer fournit de nombreuses actions intégrées pour exécuter le processus d’installation. Pour obtenir la liste de ces actions, consultez les informations de référence sur les [actions standard](standard-actions-reference.md).

Les actions standard sont suffisantes pour exécuter une installation dans la plupart des cas. Toutefois, il existe des situations où le développeur d’un package d’installation trouve qu’il est nécessaire d’écrire une action personnalisée. Par exemple :

-   Vous souhaitez lancer un fichier exécutable au cours de l’installation qui est installée sur l’ordinateur de l’utilisateur ou qui est installée avec l’application.
-   Vous souhaitez appeler des fonctions spéciales pendant une installation qui sont définies dans une bibliothèque de liens dynamiques (DLL).
-   vous souhaitez utiliser les fonctions écrites dans les langages de développement microsoft Visual Basic scripting Edition ou microsoft JScript literal script text pendant une installation.
-   Vous souhaitez différer l’exécution de certaines actions jusqu’à l’exécution du script d’installation.
-   Vous souhaitez ajouter des informations de temps et de progression à un contrôle ProgressBar et à un contrôle de texte TimeRemaining.

Les sections suivantes décrivent les actions personnalisées et la façon de les incorporer dans un package d’installation :

-   [À propos des actions personnalisées](about-custom-actions.md)
-   [Utilisation d’actions personnalisées](using-custom-actions.md)
-   [Référence des actions personnalisées](custom-action-reference.md)
-   [Liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md)

 

 



