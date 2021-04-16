---
title: Sommes de contrôle et nombre d’objets
description: Les sommes de contrôle et le nombre d’objets sont des stratégies de détection qui permettent à une application de détecter un état de mise à jour partielle.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461963"
---
# <a name="checksums-and-object-counts"></a>Sommes de contrôle et nombre d’objets

Les sommes de contrôle et le nombre d’objets sont des stratégies de détection qui permettent à une application de détecter un état de mise à jour partielle. Les sommes de contrôle peuvent également être utilisées pour détecter les incohérences introduites par la résolution des collisions. Les sommes de contrôle et les nombres d’objets nécessitent un emplacement pour stocker la valeur utilisée pour vérifier un total de contrôle ou un nombre d’objets. Il peut s’agir d’un objet « maître » choisi parmi ceux qui sont impliqués dans la relation spécifique à l’application ou sur un objet parent sous lequel les objets connexes sont stockés.

Pour les sommes de contrôle, les applications qui lisent les objets connexes vérifient la somme de contrôle en calculant un résultat local et en le comparant à la valeur stockée. Si les valeurs ne correspondent pas, le réplica est dans un état de mise à jour partielle et les objets ne peuvent pas être utilisés.

Pour le nombre d’objets, les applications dénombrent les objets connexes (généralement les enfants d’un seul parent) et comparent le nombre à la valeur stockée. Si les nombres ne correspondent pas, le réplica est dans un état de mise à jour partielle et les objets ne peuvent pas être utilisés.

Quelques points importants à prendre en compte :

-   Pour que l’approche checksum fonctionne, vous devez mettre à jour un ou plusieurs attributs utilisés dans le calcul de la somme de contrôle. L’algorithme utilisé pour calculer la somme de contrôle doit refléter de manière fiable les différences d’entrée. Si de nombreuses entrées différentes produit le même Checksum, l’algorithme ne détecte pas de manière fiable les mises à jour partielles. « Salage » l’entrée avec des valeurs telles que l' **objectGUID** de l’ordinateur source et la date et l’heure de la mise à jour sont également utiles.
-   Le nombre d’objets fonctionne mieux lorsqu’il est utilisé avec de nouveaux ensembles d’objets ou en combinaison avec des GUID de cohérence (pour plus d’informations, consultez la section suivante). L’application effectuant la mise à jour doit soit savoir, à l’avance, le nombre d’objets qui se trouveront dans le conteneur lorsque la mise à jour est terminée, soit utiliser d’autres moyens pour marquer le conteneur comme étant non valide pendant la mise à jour (par exemple, en définissant le nombre à zéro). À la fin de la mise à jour, l’application source marque le conteneur avec le nombre d’objets contenus.

 

 




