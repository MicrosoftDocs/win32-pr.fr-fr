---
description: Contient des données de jeu d’animations.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: CompressedAnimationSet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033748"
---
# <a name="compressedanimationset"></a>CompressedAnimationSet

Contient des données de jeu d’animations.

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

Où :

-   CompressedBlockSize : taille totale, en octets, des données compressées dans le tampon de données d’animation d’image clé compressée.
-   TicksPerSec : nombre de battements d’image clé d’animation qui se produisent par seconde.
-   PlaybackType : type de la boucle de lecture du jeu d’animations. Consultez [**\_ type D3DXPLAYBACK**](./d3dxplayback-type.md).
-   BufferLength : taille minimale de la mémoire tampon, en octets, nécessaire pour contenir les données d’animation d’image clé compressées. La valeur est égale à ((CompressedBlockSize + 3)/4).
-   CompressedData \[ BufferLength \] : tableau de valeurs de données compressées.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**XFILECOMPRESSEDANIMATIONSET**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
