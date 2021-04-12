---
title: Pointeurs Top-Level et incorporés
description: Pour comprendre comment les pointeurs et leurs éléments de données associés sont alloués dans Microsoft RPC, vous devez faire la différence entre les pointeurs de niveau supérieur et les pointeurs incorporés.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462423"
---
# <a name="top-level-and-embedded-pointers"></a>Pointeurs Top-Level et incorporés

Pour comprendre comment les pointeurs et leurs éléments de données associés sont alloués dans Microsoft RPC, vous devez faire la différence entre les *pointeurs de niveau supérieur* et les *pointeurs incorporés*. Il est également utile de faire référence au jeu de tous les pointeurs qui ne sont pas des pointeurs de niveau supérieur.

Les *pointeurs de niveau supérieur* sont ceux qui sont spécifiés en tant que noms de paramètres dans les prototypes de fonction. Les pointeurs de niveau supérieur et leurs référents sont toujours alloués sur le serveur.

Les *pointeurs incorporés* sont des pointeurs incorporés dans les structures de données telles que les tableaux, les structures et les unions. Lorsque les pointeurs incorporés écrivent uniquement la sortie dans une mémoire tampon et que la valeur est null en entrée, l’application serveur peut modifier leurs valeurs en valeur non null. Dans ce cas, les stubs du client allouent une nouvelle mémoire pour ces données.

Si le pointeur incorporé n’est pas null sur le client avant l’appel, les stubs n’allouent pas de mémoire sur le client lors du retour. Au lieu de cela, les stubs essaient d’écrire la mémoire associée au pointeur incorporé dans la mémoire existante sur le client associé à ce pointeur, en remplaçant les données déjà présentes.

> [!Note]  
> Pour les données lues ou écrites dans une mémoire tampon, et qui ne spécifie pas la taille de la mémoire tampon, la longueur de sortie doit être inférieure ou égale à la longueur d’entrée. Une exception RPC est levée quand un dépassement de capacité est détecté. Pour les données de type chaîne, la longueur de sortie est déterminée en vérifiant la longueur de la chaîne d’entrée. Par conséquent, les chaînes de sortie ne peuvent pas dépasser la longueur des chaînes d’entrée. La meilleure pratique consiste à éviter cela en incluant toujours un paramètre de taille spécifié pour indiquer la taille de la mémoire tampon.

 

Les pointeurs incorporés en écriture seule sont décrits dans la [combinaison d’attributs pointeur et directionnel](combining-pointer-and-directional-attributes.md).

Le terme *pointeurs de niveau nontop* fait référence à tous les pointeurs qui ne sont pas spécifiés en tant que noms de paramètres dans le prototype de fonction, y compris les pointeurs incorporés et les différents niveaux de pointeurs imbriqués.

 

 




