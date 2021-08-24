---
description: Lorsque j’utilise le VBR avec un pic restreint, le taux de bits moyen récupéré à partir de l’objet codec est plus grand que le taux binaire de pointe.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Lorsque j’utilise le VBR avec un pic restreint, le taux de bits moyen récupéré à partir de l’objet codec est plus grand que le taux binaire de pointe. Comment est-ce possible ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa27e1a03c12f854486c65d7959c66f6592da4c3fea84936ee671a911f7fa46d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011949"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Lorsque j’utilise le VBR avec un pic restreint, le taux de bits moyen récupéré à partir de l’objet codec est plus grand que le taux binaire de pointe. Comment est-ce possible ?

La relation entre la vitesse de transmission moyenne et la vitesse de transmission maximale est souvent mal comprise. Le taux de bits de pointe décrit une contrainte de mémoire tampon sur une période spécifiée par la fenêtre de mémoire tampon de pointe. La vitesse de transmission moyenne pour le VBR à deux passes (sans contrainte ou PIC) est le nombre moyen de bits par seconde sur la durée du fichier.

Comme décrit dans [le modèle de mémoire tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md), le taux de bits réel utilisé sur une période de temps égale à la fenêtre de mémoire tampon peut s’approcher de deux fois la vitesse de transmission. Cela est dû au fait que la mémoire tampon, définie sous la forme d’un nombre de bits égal à la vitesse de transmission de la mémoire tampon (en secondes), est vidée à une fréquence constante.

Par exemple, dans une seconde d’un flux de 56 Kbits/s, l’encodeur crée des exemples totalisant 59 Ko. Ainsi, 56 Ko de données sont supprimés de la mémoire tampon dans cette seconde, ce qui laisse 3 Ko dans la mémoire tampon. Si le flux a une fenêtre de mémoire tampon de trois secondes, et donc une taille de mémoire tampon totale de 168 Ko, il faut presque 40 secondes pour remplir la mémoire tampon. La vitesse de transmission moyenne du flux (si sa durée est inférieure au temps nécessaire pour remplir la mémoire tampon) est de 59 Kbits/s, même si la vitesse de transmission est définie à 56 Kbps.

Le même phénomène s’applique aux contraintes de taux de bits de pointe. Pour du contenu de petite taille, le taux de bits moyen calculé par l’objet codec après l’encodage est supérieur au taux de bits de pointe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Questions fréquentes (FAQ)](frequentlyaskedquestions.md)
</dt> </dl>

 

 



