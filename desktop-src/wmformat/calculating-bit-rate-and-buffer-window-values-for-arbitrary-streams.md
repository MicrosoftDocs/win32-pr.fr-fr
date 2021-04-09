---
title: Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires
description: Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- flux, vitesses de transmission
- codecs, calcul des vitesses de transmission pour les flux arbitraires
- vitesses de transmission, calcul pour les flux arbitraires
- flux, calcul des vitesses de transmission pour les flux arbitraires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028636"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires

Le calcul de la vitesse de transmission et de la fenêtre de mémoire tampon appropriées pour un type de flux arbitraire n’est pas une science exacte. Une approche simple consiste à définir la vitesse de transmission pour qu’elle corresponde à la taille du flux divisé par sa longueur, en secondes. Par exemple, un flux contenant un total de 68000 bits durables 20 secondes peut avoir un débit binaire de 3400 bits par seconde (68000 bits/20 secondes = 3400 bits par seconde).

Le problème avec cette technique simple consistant à affecter la vitesse de transmission est qu’elle ne prend pas en compte la distribution des données dans le flux. De nombreux flux arbitraires contiennent de plus grandes quantités de données à des intervalles le long de la chronologie du fichier. Les flux d’images, par exemple, ont des exemples qui sont plutôt importants, mais qui sont généralement espacés de plusieurs secondes. La fenêtre de mémoire tampon doit être définie pour garantir que la mémoire tampon ne peut pas déborder.

Pour vérifier la fenêtre de mémoire tampon, multipliez la vitesse de transmission (bits par seconde) par la fenêtre de mémoire tampon (en secondes) et divisez par 1000 pour obtenir la taille, en bits, de la mémoire tampon pour le flux. Ensuite, assurez-vous que la taille de la mémoire tampon est suffisamment grande pour contenir toute combinaison d’échantillons dans le flux qui sont inférieurs à la fenêtre de la mémoire tampon en dehors de l’heure de présentation. En cas de doute, définissez les deux valeurs un peu plus haut que vous ne le jugez nécessaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Mise en mémoire tampon du contenu**](buffering-content.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




