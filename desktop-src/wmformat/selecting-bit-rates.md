---
title: Sélection des vitesses de transmission
description: Sélection des vitesses de transmission
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- profils, choix des vitesses de transmission
- profils, vitesses de transmission
- codecs, choix des vitesses de transmission
- codecs, vitesses de transmission
- profils, sélection de vitesses de transmission
- codecs, sélection de vitesses de transmission
- vitesses de transmission, sélection
- vitesses de transmission, profils
- vitesses de transmission, codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309161"
---
# <a name="selecting-bit-rates"></a>Sélection des vitesses de transmission

Pour les fichiers qui seront diffusés en continu sur un réseau, vous devez prendre en compte soigneusement les vitesses de transmission que vous devez utiliser. Dans la plupart des cas, vous pouvez ajouter les vitesses de transmission de tous les flux d’un fichier pour obtenir une idée générale de la bande passante disponible nécessaire pour diffuser le fichier. Toutefois, une certaine surcharge est également requise pour chaque flux. Cette surcharge est résumée dans le tableau suivant.



| Plage du taux de bits (Kbits/s) | Bande passante supplémentaire requise pour la surcharge (Kbits/s) |
|-----------------------|---------------------------------------------------|
| 10 – 16               | 3                                                 |
| 17 – 30               | 4                                                 |
| 31 – 45               | 5                                                 |
| 46 – 70               | 6                                                 |
| 71 – 225              | 7                                                 |
| >225               | 9                                                 |



 

La surcharge normale requise pour un flux ne prend pas en compte les extensions d’unité de données. Chaque extension d’unité de données ajoute à la taille de l’échantillon auquel elle est attachée. Selon le type d’extension d’unité de données, cela peut augmenter de façon considérable la vitesse de transmission du flux.

Vous devez également tenir compte du fait que la bande passante maximale théorique disponible sur une connexion réseau n’est pas une vitesse de transmission cible pratique. La bande passante disponible moyenne pour une connexion donnée se situe bien au-dessus de la capacité de bande passante de la connexion, en raison du trafic réseau et de nombreux autres facteurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conception de profils**](designing-profiles.md)
</dt> </dl>

 

 




