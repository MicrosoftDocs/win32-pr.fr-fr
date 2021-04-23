---
description: Les sous-types suivants définissent des formats RGB non compressés sans canal alpha.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Sous-types de vidéos RVB non compressés (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894034c01b42f58cbc6a1e5a5c7fe6d77f50befd
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909527"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Sous-types de vidéos RVB non compressés

Les sous-types suivants définissent des formats RGB non compressés sans canal alpha.



| Constante                                                                                                                                                                        | Description                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**MEDIASUBTYPE \_ RGB1**</dt> </dl>       | RVB, 1 bit par pixel (BPP), en palette<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**MEDIASUBTYPE \_ RGB4**</dt> </dl>       | RVB, 4 BPP, en palette<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**MEDIASUBTYPE \_ RGB8**</dt> </dl>       | RVB, 8 BPP, en palette<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**MEDIASUBTYPE \_ RGB555**</dt> </dl> | RGB 555, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**MEDIASUBTYPE \_ RGB565**</dt> </dl> | RGB 565, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**MEDIASUBTYPE \_ Rgb24**</dt> </dl>    | RVB, 24 BPP<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**MEDIASUBTYPE \_ RGB32**</dt> </dl>    | RGB, 32 BPP<br/>                            |



Les sous-types suivants définissent les formats RVB non compressés avec le canal alpha.



| Constante                                                                                                                                                                                       | Description                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB1555**</dt> </dl>          | RGB 555 avec canal alpha<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB32**</dt> </dl>                | RGB 32 avec canal alpha<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB4444**</dt> </dl>          | RGB 16 bits avec canal alpha ; 4 bits par canal<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**MEDIASUBTYPE \_ A2R10G10B10**</dt> </dl> | RGB 32 bits avec canal alpha 10 bits par canal RVB plus 2 bits pour alpha.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**MEDIASUBTYPE \_ A2B10G10R10**</dt> </dl> | 32 bits BGR avec canal alpha 10 bits par canal BGR plus 2 bits pour alpha.<br/> |



## <a name="remarks"></a>Remarques

Pour les formats en palette, la couleur de chaque pixel est spécifiée en tant qu’index dans une palette. La palette doit être incluse dans le bloc de format, à la suite de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Pour les formats non-en palette, la couleur de chaque pixel est spécifiée directement ; la disposition de la mémoire dépend de la profondeur de bits :

-   RGB 555 utilise la disposition mémoire suivante :
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   RGB 565 utilise la disposition mémoire suivante :
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   Pour RVB 24, chaque pixel est un [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple). Chaque couleur est un octet, avec une valeur comprise entre 0 et 255 inclus. La disposition de la mémoire est : 

| Étiquette | Valeur |
    |-------|------|-------|-----|
    | Byte  | 0    | 1     | 2   |
    | Valeur | Bleu | Vert | Rouge |

    

     

-   Pour RGB 32, chaque pixel est un **RGBQUAD**. Chaque couleur est un octet, avec une valeur comprise entre 0 et 255 inclus. La disposition de la mémoire est : 

| Étiquette | Valeur |
    |-------|------|-------|-----|---------------------|
    | Byte  | 0    | 1     | 2   | 3                   |
    | Valeur | Bleu | Vert | Rouge | Alpha ou ne vous inquiétez pas |

    

     

    If the subtype is MEDIASUBTYPE\_ARGB32, byte 3 contains a value for the alpha channel. If the subtype is MEDIASUBTYPE\_RGB32, byte 3 should be ignored.

-   A2R10G10B10 utilise la disposition suivante : 

| Étiquette | Valeur |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | Valeur | Bleu  | Vert   | Rouge     | Alpha   |

    

     

-   A2B10G10R10 utilise la disposition suivante : 

| Étiquette | Valeur |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | Valeur | Rouge   | Vert   | Bleu    | Alpha   |

    

     

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sous-types de vidéos](video-subtypes.md)
</dt> <dt>

[Utilisation des images vidéo](working-with-video-frames.md)
</dt> </dl>

 

 
