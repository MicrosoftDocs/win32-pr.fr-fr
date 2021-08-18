---
description: Exemples de limitations de programme
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Exemples de limitations de programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0244f373264ed6886632979f00ace873949c1ab7e781262b4ef30dab2072f8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007437"
---
# <a name="example-program-limitations"></a>Exemples de limitations de programme

Les principes de bonnes pratiques de programmation ne sont pas toujours suivis dans ces exemples de programmes afin de fournir un code plus concis et plus lisible. En particulier :

-   Seules les réponses d’erreur limitées sont affichées. Les programmes de travail doivent toujours vérifier les codes d’erreur renvoyés et effectuer les actions appropriées lorsqu’une erreur est rencontrée.
-   Seule la gestion de la mémoire et des ressources est limitée. Dans les programmes de travail, toutes les clés et tous les [*hachages*](../secgloss/h-gly.md) doivent être détruits, toute la mémoire allouée doit être libérée, tous les fichiers doivent être fermés et tous les descripteurs doivent être libérés. Ces exemples de programmes fournissent uniquement des démonstrations limitées de l’utilisation des fonctions qui effectuent ces tâches. Ces exemples de programmes n’effectuent aucune tâche de gestion de la mémoire ou des ressources en cas d’arrêt du programme en raison d’erreurs.

 

 
