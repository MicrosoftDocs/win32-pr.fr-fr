---
description: Les indicateurs suivants sont utilisés pour spécifier les canaux à utiliser dans une texture.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481305"
---
# <a name="d3dx_filter"></a>\_Filtre D3DX

Les indicateurs suivants sont utilisés pour spécifier les canaux à utiliser dans une texture.



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#définition                | Description                                                                                                                                                                                                 |
| Filtre D3DX, \_ \_ aucun      | Aucune mise à l’échelle ou aucun filtrage n’aura lieu. Les pixels en dehors des limites de l’image source sont supposés être en noir transparent.                                                                                 |
| \_Point de filtre D3DX \_     | Chaque pixel de destination est calculé en échantillonnant le pixel le plus proche de l’image source.                                                                                                                     |
| D3DX- \_ filtre \_ linéaire    | Chaque pixel de destination est calculé en échantillonnant les quatre pixels les plus proches de l’image source. Ce filtre fonctionne mieux lorsque la mise à l’échelle sur les deux axes est inférieure à deux.                                          |
| \_Triangle de filtre D3DX \_  | Chaque pixel de l’image source contribue de manière égale à l’image de destination. Il s’agit de la plus lente des filtres.                                                                                           |
| \_Zone de filtre D3DX \_       | Chaque pixel est calculé en calculant la moyenne d’une zone de pixels 2x2 (x2) à partir de l’image source. Ce filtre fonctionne uniquement lorsque les dimensions de la destination sont la moitié de la source, comme c’est le cas avec des mipmaps. |
| D3DX \_ Filtrer \_ en miroir \_ U | Les pixels du bord de la texture sur l’axe u doivent être mis en miroir, et non encapsulés.                                                                                                                           |
| Filtre D3DX- \_ \_ miroir \_ V | Les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.                                                                                                                           |
| \_ \_ Mise en miroir du filtre D3DX \_ W | Les pixels du bord de la texture sur l’axe des w doivent être mis en miroir, et non encapsulés.                                                                                                                           |
| \_ \_ Mise en miroir du filtre D3DX    | La spécification de cet indicateur revient à spécifier les \_ indicateurs de filtre D3DX en miroir \_ \_ U, D3DX \_ Filter \_ miroir \_ V et D3DX \_ Filter- \_ MIRROR \_ W.                                                                     |
| Filtre D3DX, \_ \_ trame    | L’image résultante doit être tramée à l’aide d’un algorithme de trame trié 4x4.                                                                                                                                  |
| \_Filtre \_ de D3DX sRVB \_ dans  | Les données d’entrée se trouvent dans l’espace de couleurs sRGB (gamma 2,2).                                                                                                                                                              |
| Filtre de D3DX en \_ \_ \_ sortie | Les données de sortie se trouvent dans l’espace de couleurs sRGB (gamma 2,2).                                                                                                                                                         |
| Filtre de D3DX \_ \_ sRVB      | Identique à la spécification \_ de la fonction de filtre D3DX \_ sRVB \_ dans le \| \_ filtre D3DX \_ \_ out.                                                                                                                                       |



 

Chaque filtre valide doit contenir exactement l’un des indicateurs suivants : D3DX \_ filtre \_ None, D3DX \_ Filter \_ point, D3DX \_ Filter \_ Linear, D3DX \_ Filter \_ triangle ou D3DX \_ Filter \_ Box. En outre, vous pouvez utiliser l’opérateur OR pour spécifier zéro, un ou plusieurs des indicateurs facultatifs suivants avec un filtre valide : D3DX \_ Filter \_ miroir \_ U, D3DX \_ Filter \_ MIRROR \_ V, D3DX \_ filtre \_ MIRROR \_ avec, D3DX Filter \_ \_ miroir, D3DX \_ Filter \_ juxtaposition, D3DX \_ Filter \_ sRVB \_ in, D3DX \_ Filter sRVB \_ \_ out ou D3DX \_ Filter \_ sRGB.

La spécification de \_ la valeur D3DX par défaut pour ce paramètre est généralement l’équivalent de la spécification de la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ . Toutefois, D3DX \_ default peut avoir différentes significations, en fonction de la méthode qui utilise le filtre. Par exemple :

-   Quand vous utilisez [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), la \_ valeur par défaut de D3DX est mappée au triangle de filtre D3DX de filtre \_ \_ \| \_ \_ .
-   Quand vous utilisez [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ la valeur par défaut de D3DX est mappée à \_ la zone de filtre D3DX \_ si la taille de la texture est une puissance de deux et le filtre de la zone de filtre D3DX dans le \_ \_ \| \_ \_ cas contraire.

Référencez chaque méthode pour rechercher des informations sur la façon dont le \_ filtre par défaut D3DX est mappé.

## <a name="constant-information"></a>Informations constantes



|                          |            |
|--------------------------|------------|
| En-tête                   | d3dx9tex. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



