---
title: Exemple de texture DDS
description: Pour une texture non compressée, utilisez les \_ indicateurs RGB DDSD et DDPF \_ . pour une texture compressée, utilisez les \_ indicateurs DDSD LINEARSIZE et DDPF \_ FourCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510831"
---
# <a name="dds-texture-example"></a>Exemple de texture DDS

Pour une texture non compressée, utilisez les \_ indicateurs RGB DDSD et DDPF \_ . pour une texture compressée, utilisez les \_ indicateurs DDSD LINEARSIZE et DDPF \_ FourCC. Pour une texture mipmapped, utilisez également les \_ indicateurs DDSD MIPMAPCOUNT, DDSCAPS \_ MIPMAP et DDSCAPS Complex, ainsi que \_ le membre de décompte mipmap. Si les des mipmaps sont générés, tous les niveaux jusqu’à 1 par 1 sont généralement écrits.

Pour une texture compressée, la taille de chaque image de niveau de mipmap correspond généralement à un quart de la taille du précédent, avec un minimum de 8 (DXT1) ou 16 (DXT2-5) octets (pour les textures carrées). Utilisez la formule suivante pour calculer la taille de chaque niveau pour une texture non carrée :


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



Ce tableau répertorie la quantité d’espace occupé par chaque couche pour une texture R8G8B8 de 256 par 256, sans utiliser la compression.



| Composants DDS          | \# Bits |
|-------------------------|----------|
| en-tête                  | 128      |
| 256-par-256 image principale   | 196 608   |
| image mipmap 128-par-128 | 49152    |
| image mipmap 64-par-64   | 12288    |
| image mipmap 32-par-32   | 3 072     |
| image mipmap 16 par 16   | 768      |
| image mipmap 8 par 8     | 192      |
| image mipmap 4-par-4     | 48       |
| image mipmap 2 par 2     | 12       |
| image mipmap 1-par-1     | 3        |



 

Ce tableau répertorie la quantité d’espace occupé par chaque couche pour la même texture à l’aide de la compression (DXT1).



| Composants DDS         | \# Bits |
|------------------------|----------|
| en-tête                 | 128      |
| 256-par-64 image principale   | 8 192     |
| image mipmap 128-par-32 | 2 048     |
| image mipmap 64-par-16  | 512      |
| image mipmap 32-par-8   | 128      |
| image mipmap 16 par 4   | 32       |
| image mipmap 8 par 2    | 16       |
| image mipmap de 4 par 1    | 8        |
| image mipmap 2 par 1    | 8        |
| image mipmap 1-par-1    | 8        |



 

Ce tableau répertorie la quantité d’espace occupée par chaque couche pour la même texture à l’aide d’un format de compression DXGI (dans ce cas BC3 \_ UNORM) qui requiert par conséquent l’en-tête étendu :



| Composants DDS                                                | \# Bits |
|---------------------------------------------------------------|----------|
| Header (FourCC défini sur « facilement »)                                 | 128      |
| en-tête étendu (DXGI format défini au \_ format dxgi \_ BC3 \_ UNORM) | 20       |
| 256-par-64 image principale                                          | 16384    |
| image mipmap 128-par-32                                        | 4096     |
| image mipmap 64-par-16                                         | 1 024     |
| image mipmap 32-par-8                                          | 256      |
| image mipmap 16 par 4                                          | 64       |
| image mipmap 8 par 2                                           | 32       |
| image mipmap de 4 par 1                                           | 16       |
| image mipmap 2 par 1                                           | 16       |
| image mipmap 1-par-1                                           | 16       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




