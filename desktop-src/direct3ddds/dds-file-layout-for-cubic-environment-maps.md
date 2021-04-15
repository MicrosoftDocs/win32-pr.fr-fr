---
title: Exemple de mappage de cube DDS
description: Pour les cartes d’environnement cubiques, une ou plusieurs faces d’un cube sont écrites dans le fichier, à l’aide de formats non compressés ou compressés, et toutes les faces doivent avoir la même taille.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235749bc0cf95a2e2120f66f3bcfb8a46e158628
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507295"
---
# <a name="dds-cube-map-example"></a>Exemple de mappage de cube DDS

Pour les cartes d’environnement cubiques, une ou plusieurs faces d’un cube sont écrites dans le fichier, à l’aide de formats non compressés ou compressés, et toutes les faces doivent avoir la même taille. Chaque visage peut avoir des des mipmaps définis, bien que toutes les faces doivent avoir le même nombre de niveaux de mipmap. Si un fichier contient un mappage de cube, DDSCAPS \_ Complex, DDSCAPS2 \_ carte cubique et un ou plusieurs DSCAPS2 \_ carte cubique POSITIVEX \_ /y/z et/ou DDSCAPS2 carte cubique \_ \_ /y/z doivent être définis. Les visages sont écrits dans l’ordre suivant : x positif, x négatif, positif y, y négatif, y positif z, z négatif, avec les visages manquants omis. Chaque visage est écrit avec son image principale, suivi de tous les niveaux de mipmap.

Par exemple, un mappage de cube 256-par-256 avec des visages positif x, négatif y et z positif, un format de pixel de DXT1 et tous les niveaux de mipmap contiennent les éléments suivants :



| Composants DDS                                      | \# Bits |
|-----------------------------------------------------|----------|
| en-tête                                              | 128      |
| 256-par-256 image principale x positive                    | 32 768    |
| 128-par-128 image mipmap positive x                  | 8 192     |
| 64-par-64 image mipmap positive x                    | 2 048     |
| 32-par-32 image mipmap positive x                    | 512      |
| image mipmap 16 par 16 positive x                    | 128      |
| image mipmap 8 x 8 positive                      | 32       |
| image mipmap x 4 par 4 positive                      | 8        |
| image de mipmap x positif 2-par-2                      | 8        |
| image de mipmap x positive 1-par-1                      | 8        |
| répéter les 9 couches précédentes pour l’image de mipmap y | 43704    |
| répéter les 9 couches précédentes pour l’image de mipmap z | 43704    |



 

À partir de DirectX 8, un mappage de cube est stocké avec tous les visages définis.

## <a name="dxgi-cube-maps"></a>Mappages de cubes DXGI

Les mappages d’environnement cubique dans Direct3D 10. x et Direct3D 11 sont équivalents à un tableau de texture 2D avec 6 images et peuvent être stockés dans des fichiers DDS en tant que tels. Avec Direct3D 10,1 et Direct3D 11, le matériel peut également prendre en charge des tableaux de cubemaps qui sont eux-mêmes des tableaux de texture 2D avec un multiple de 6 images (6, 12, 18, 24, etc.).

Par exemple, voici un carte cubique de 256 par 256 avec des niveaux de mipmap stockés dans un format BC6H sous la forme d’un tableau de textures 2D :



| Composants DDS                                                                                                                                                                                                  | \# Bits |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| en-tête (FourCC de « facilement »)                                                                                                                                                                                       | 128      |
| en-tête étendu (DXGI format défini sur 95 \[ dxgi \_ format \_ BC6H \_ UF16 \] , valeur de dimension de 3 \[ D3Dxx \_ dimension de ressource TEXTURE2D \_ \_ \] , taille de tableau 6, indicateurs divers de 0x4 \[ D3Dxx \_ ressource diverse TEXTURECUBE \_ \_ \] ) | 20       |
| 256-par-256 entrée de tableau 0 (x positive) image principale                                                                                                                                                                | 65536    |
| 128-par-128 image de tableau de mipmap 0 (x positif)                                                                                                                                                              | 16384    |
| 64-par-64 image de tableau de mipmap 0 (x positif)                                                                                                                                                                | 4096     |
| 32-par-32 image de tableau de mipmap 0 (x positif)                                                                                                                                                                | 1 024     |
| image de tableau 16 par 16 (x positif x) mipmap                                                                                                                                                                | 256      |
| image de tableau 8 x 8 (valeur x positive)                                                                                                                                                                  | 64       |
| image de tableau 4-par-4 (x positif x) mipmap                                                                                                                                                                  | 16       |
| image de tableau 2 par 2 (valeur x positive)                                                                                                                                                                  | 16       |
| image de tableau 1-par-1 (x positif x) mipmap                                                                                                                                                                  | 16       |
| répéter les 9 couches précédentes pour l’image d’entrée de tableau 1 (x) mipmap                                                                                                                                        | 87408    |
| répéter les 9 couches précédentes pour une image de tableau de l’entrée 2 (y positif y)                                                                                                                                        | 87408    |
| répéter les 9 couches précédentes pour l’entrée de tableau 3 (image mipmap négative y)                                                                                                                                        | 87408    |
| répéter les 9 couches précédentes pour l’image d’entrée de tableau 4 (z positif)                                                                                                                                        | 87408    |
| répéter les 9 couches précédentes pour une image de tableau de l’entrée 5 (z négatif)                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




