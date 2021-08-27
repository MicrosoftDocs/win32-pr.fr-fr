---
title: Exemple de texture de volume DDS
description: Pour une texture de volume, utilisez la DDSCAPS \_ complexe, le \_ volume DDSCAPS2, la profondeur DDSD, les \_ indicateurs et le jeu et dwDepth. Une texture de volume est une extension d’une texture standard pour Direct3D 9 ; une texture de volume peut être définie avec ou sans des mipmaps.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79501ea3ffa6f4a660f4ab3b248fedbdc7df17bf8af94520cad5808c3c611fd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025739"
---
# <a name="dds-volume-texture-example"></a>Exemple de texture de volume DDS

Pour une texture de volume, utilisez la DDSCAPS \_ complexe, le \_ volume DDSCAPS2, la profondeur DDSD, les \_ indicateurs et le jeu et dwDepth. Une texture de volume est une extension d’une texture standard pour Direct3D 9 ; une texture de volume peut être définie avec ou sans des mipmaps.

Pour les volumes sans des mipmaps, chaque tranche de profondeur est écrite dans le fichier dans l’ordre. Si les des mipmaps sont inclus, toutes les tranches de profondeur pour un niveau de mipmap donné sont écrites ensemble, chaque niveau contenant un demi-nombre de secteurs comme niveau précédent, avec un minimum de 1.

Par exemple, une carte de volume 64 par 64-par-4 utilisant un format de pixel R8G8B8 (3 octets par pixel) avec tous les niveaux de mipmap contient les éléments suivants :



| Composants DDS                      | \# Bits    |
|-------------------------------------|-------------|
| en-tête                              | 128 octets   |
| 64-par-64 tranche 1 sur 4 image principale.   | 12288 octets |
| 64-par-64 tranche 2 sur 4 image principale.   | 12288 octets |
| 64-par-64 tranche 3 sur 4 image principale.   | 12288 octets |
| 64-par-64 tranche 4 sur 4 image principale.   | 12288 octets |
| 32-par-32 section 1 sur 2 image mipmap. | 3072 octets  |
| 32-par-32 section 2 sur 2 image mipmap. | 3072 octets  |
| 16 par 16, tranche 1 sur 1 image mipmap. | 768 octets   |
| 8 par 8, tranche 1 sur 1 image mipmap.   | 192 octets   |
| 4-par-4 section 1 sur 1 image mipmap.   | 48 octets    |
| 2-par-2 découpe 1 de 1 image mipmap.   | 12 octets    |
| 1-par-1 tranche 1 sur 1 image mipmap.   | 3 octets     |



 

Notez que le plus petit niveau de mipmap n’est que 3 octets, car bitCount est 24 et aucune compression n’est ajoutée à ce niveau.

La prise en charge des textures de volume a été ajoutée dans DirectX 8.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




