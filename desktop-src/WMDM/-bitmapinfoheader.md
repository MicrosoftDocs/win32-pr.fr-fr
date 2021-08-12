---
title: Structure _BITMAPINFOHEADER
description: La \_ structure BITMAPINFOHEADER définit le format d’une image vidéo.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Structure de _BITMAPINFOHEADER Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2d0da3d05fe050f32d5a35bbbe7de558e1c4962fa84a958855b2960e343942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586883"
---
# <a name="_bitmapinfoheader-structure"></a>\_BITMAPINFOHEADER, structure

La structure **\_ BITMAPINFOHEADER** définit le format d’une image vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**bisize**
</dt> <dd>

Spécifie le nombre d’octets requis par la structure.

</dd> <dt>

**bichasse**
</dt> <dd>

Spécifie la largeur de l’image bitmap, en pixels.

</dd> <dt>

**bihauteur**
</dt> <dd>

Spécifie la hauteur, en pixels, de la bitmap. Si la **bihauteur** est positive, le bitmap est un DIB ascendant et son origine est l’angle inférieur gauche. Si la valeur **bihauteur** est négative, l’image bitmap est un DIB descendant et son origine est l’angle supérieur gauche. Si la **bihauteur** est négative, ce qui indique un DIB de haut en haut, la **compression** doit être de type de bits \_ RVB bi ou bi \_ . Les DIB descendants ne peuvent pas être compressés.

</dd> <dt>

**biplans**
</dt> <dd>

Spécifie le nombre de plans pour l’appareil cible. Cette valeur doit être définie sur 1.

</dd> <dt>

**biBitCount**
</dt> <dd>

Spécifie le nombre de bits par pixel. Le membre **biBitCount** de la structure **BITMAPINFOHEADER** détermine le nombre de bits qui définissent chaque pixel et le nombre maximal de couleurs dans l’image bitmap. Ce membre doit avoir l’une des valeurs suivantes.



| Value | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | La bitmap est monochrome et le membre bmiColors contient deux entrées. Chaque bit du tableau de bitmaps représente un pixel. Si le bit est clair, le pixel est affiché avec la couleur de la première entrée dans la table bmiColors ; Si le bit est défini, le pixel a la couleur de la deuxième entrée dans la table.                                                                                                                                                                                                                                                                                                        |
| 2     | La bitmap possède quatre valeurs de couleur possibles.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | La bitmap a un maximum de 16 couleurs, et le membre bmiColors contient jusqu’à 16 entrées. Chaque pixel de la bitmap est représenté par un index 4 bits dans la table des couleurs. Par exemple, si le premier octet de la bitmap est 0x1F, l’octet représente deux pixels. Le premier pixel contient la couleur de la deuxième entrée de la table, tandis que le deuxième pixel contient la couleur dans le seizième entrée de la table.                                                                                                                                                                                                                 |
| 8     | La bitmap a un maximum de 256 couleurs et le membre bmiColors contient jusqu’à 256 entrées. Dans ce cas, chaque octet du tableau représente un pixel unique.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | La bitmap a un maximum de 2 ^ 16 couleurs. Si le membre de bicompression de l’BITMAPINFOHEADER est BI \_ RGB, le membre bmiColors est **null**. Chaque mot du tableau de bitmaps représente un pixel unique. Les inintensités relatives de rouge, de vert et de bleu sont représentées par 5 bits pour chaque composant de couleur. La valeur du bleu est comprise dans les 5 bits les moins significatifs, suivis de 5 bits chacun pour le vert et le rouge. Le bit le plus significatif n’est pas utilisé. La table de couleurs bmiColors est utilisée pour optimiser les couleurs utilisées sur les appareils basés sur une palette et doit contenir le nombre d’entrées spécifié par le membre biClrUsed. |
| 24    | La bitmap a un maximum de 2 ^ 24 couleurs et le membre bmiColors a la **valeur null**. Chaque triplet de 3 octets dans le tableau de bitmaps représente les indizaines relatives de bleu, vert et rouge, respectivement, pour un pixel. La table de couleurs bmiColors est utilisée pour optimiser les couleurs utilisées sur les appareils basés sur une palette et doit contenir le nombre d’entrées spécifié par le membre biClrUsed.                                                                                                                                                                                                                                     |
| 32    | La bitmap a un maximum de 2 ^ 32 couleurs. Si le membre de bicompression est BI \_ RGB, le membre bmiColors a la **valeur null**. Chaque DWORD dans le tableau de bitmaps représente les indizaines relatives de bleu, vert et rouge, respectivement, pour un pixel. L’octet de poids fort de chaque DWORD n’est pas utilisé. La table de couleurs bmiColors est utilisée pour optimiser les couleurs utilisées sur les appareils basés sur une palette et doit contenir le nombre d’entrées spécifié par le membre biClrUsed.                                                                                                                                                                 |



 

</dd> <dt>

**Compression**
</dt> <dd>

Spécifie le type de compression d’une image bitmap ascendante compressée (les DIB descendants ne peuvent pas être compressés). Ce membre peut être l’une des valeurs suivantes.



| Value         | Description                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RGB bi       | Format non compressé.                                                                                                                                                                                                                                                                                            |
| champs de \_ passe bi | Spécifie que l’image bitmap n’est pas compressée et que la table des couleurs est composée de trois masques de couleur DWORD qui spécifient respectivement les composants rouge, vert et bleu de chaque pixel. Cela est valide lorsqu’il est utilisé avec des bitmaps 16-bpp et 32-BPP. cette valeur est valide dans Microsoft Windows CE version 2,0 et versions ultérieures. |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

Spécifie la taille de l’image, en octets. Cette valeur peut être définie sur zéro pour les \_ bitmaps RGB bi.

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

Spécifie la résolution horizontale, en pixels par mètre, de l’appareil cible pour l’image bitmap. Une application peut utiliser cette valeur pour sélectionner une image bitmap d’un groupe de ressources qui correspond le mieux aux caractéristiques de l’appareil actuel.

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

Spécifie la résolution verticale, en pixels par mètre, de l’appareil cible pour l’image bitmap.

</dd> <dt>

**biClrUsed**
</dt> <dd>

Spécifie le nombre d’index de couleurs qui sont réellement utilisés par la bitmap dans la table des couleurs. Si cette valeur est égale à zéro, la bitmap utilise le nombre maximal de couleurs correspondant à la valeur du membre **biBitCount** pour le mode de compression spécifié par la **compression**.

</dd> <dt>

**biClrImportant**
</dt> <dd>

Spécifie le nombre d’index de couleurs requis pour l’affichage de la bitmap. Si cette valeur est égale à zéro, toutes les couleurs sont requises.

Si biClrUsed est différent de zéro et que le membre biBitCount est inférieur à 16, le membre biClrUsed spécifie le nombre réel de couleurs auxquelles le moteur graphique ou le pilote de périphérique accède. Si biBitCount a une valeur supérieure ou égale à 16, le membre biClrUsed spécifie la taille de la table de couleurs utilisée pour optimiser les performances des palettes de couleurs système. Si biBitCount est égal à 16 ou 32, la palette de couleurs optimale commence immédiatement après les trois masques DWORD.

Si la bitmap est un bitmap condensé (une image bitmap dans laquelle le tableau bitmap suit immédiatement la \_ structure BITMAPINFOHEADER et est référencé par un pointeur unique), le membre biClrUsed doit être égal à zéro ou à la taille réelle de la table de couleurs.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est contenue dans une structure **\_ VIDEOINFOHEADER** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





