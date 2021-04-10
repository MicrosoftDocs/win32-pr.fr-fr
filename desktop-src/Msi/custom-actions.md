---
description: Le Windows Installer fournit de nombreuses actions intégrées pour exécuter le processus d’installation. Pour obtenir la liste de ces actions, consultez les informations de référence sur les actions standard.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034648"
---
# <a name="custom-actions"></a>Actions personnalisées

Le Windows Installer fournit de nombreuses actions intégrées pour exécuter le processus d’installation. Pour obtenir la liste de ces actions, consultez les informations de référence sur les [actions standard](standard-actions-reference.md).

Les actions standard sont suffisantes pour exécuter une installation dans la plupart des cas. Toutefois, il existe des situations où le développeur d’un package d’installation trouve qu’il est nécessaire d’écrire une action personnalisée. Par exemple :

-   Vous souhaitez lancer un fichier exécutable au cours de l’installation qui est installée sur l’ordinateur de l’utilisateur ou qui est installée avec l’application.
-   Vous souhaitez appeler des fonctions spéciales pendant une installation qui sont définies dans une bibliothèque de liens dynamiques (DLL).
-   Vous souhaitez utiliser des fonctions écrites dans les langages de développement Microsoft Visual Basic Scripting Edition ou le texte de script littéral Microsoft JScript pendant une installation.
-   Vous souhaitez différer l’exécution de certaines actions jusqu’à l’exécution du script d’installation.
-   Vous souhaitez ajouter des informations de temps et de progression à un contrôle ProgressBar et à un contrôle de texte TimeRemaining.

Les sections suivantes décrivent les actions personnalisées et la façon de les incorporer dans un package d’installation :

-   [À propos des actions personnalisées](about-custom-actions.md)
-   [Utilisation d’actions personnalisées](using-custom-actions.md)
-   [Référence des actions personnalisées](custom-action-reference.md)
-   [Liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md)

 

 



