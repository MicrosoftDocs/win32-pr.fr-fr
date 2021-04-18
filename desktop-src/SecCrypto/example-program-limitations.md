---
description: Exemples de limitations de programme
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Exemples de limitations de programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520654"
---
# <a name="example-program-limitations"></a>Exemples de limitations de programme

Les principes de bonnes pratiques de programmation ne sont pas toujours suivis dans ces exemples de programmes afin de fournir un code plus concis et plus lisible. En particulier :

-   Seules les réponses d’erreur limitées sont affichées. Les programmes de travail doivent toujours vérifier les codes d’erreur renvoyés et effectuer les actions appropriées lorsqu’une erreur est rencontrée.
-   Seule la gestion de la mémoire et des ressources est limitée. Dans les programmes de travail, toutes les clés et tous les [*hachages*](../secgloss/h-gly.md) doivent être détruits, toute la mémoire allouée doit être libérée, tous les fichiers doivent être fermés et tous les descripteurs doivent être libérés. Ces exemples de programmes fournissent uniquement des démonstrations limitées de l’utilisation des fonctions qui effectuent ces tâches. Ces exemples de programmes n’effectuent aucune tâche de gestion de la mémoire ou des ressources en cas d’arrêt du programme en raison d’erreurs.

 

 
