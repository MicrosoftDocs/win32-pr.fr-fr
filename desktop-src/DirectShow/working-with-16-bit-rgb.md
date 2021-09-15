---
description: Utilisation d’une couleur RVB 16 bits
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Utilisation d’une couleur RVB 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238782"
---
# <a name="working-with-16-bit-rgb"></a>Utilisation d’une couleur RVB 16 bits

Deux formats sont définis pour la couleur RVB non compressée 16 bits :

-   MEDIASUBTYPE \_ 555 utilise cinq bits pour chaque composant rouge, vert et bleu d’un pixel. Le bit le plus significatif dans le **mot** est ignoré.
-   MEDIASUBTYPE \_ 565 utilise cinq bits pour les composants rouge et bleu, et six bits pour le composant vert. Ce format reflète le fait que la vision humaine est la plus sensible aux parties vertes du spectre visible.

**RGB 565**

Pour extraire les composants de couleur d’une image RVB 565, traitez chaque pixel comme un type de **mot** et utilisez les masques de bits suivants :


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



Récupérez les composants de couleur d’un pixel comme suit :


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



N’oubliez pas que les canaux rouge et bleu sont 5 bits et que le canal vert est 6 bits. Pour convertir ces valeurs en composants 8 bits (pour les couleurs RVB 24 bits ou 32 bits), vous devez déplacer le nombre de bits approprié vers la gauche :


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



Inversez ce processus pour créer un pixel RVB 565. En supposant que les valeurs de couleur ont été tronquées avec le nombre correct de bits :


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



**RGB 555**

L’utilisation de RGB 555 est fondamentalement identique à la couleur RVB 565, sauf que les masques de bits et les opérations de décalage de bits sont différents. Pour récupérer les composants de couleur à partir d’un pixel RVB 555, procédez comme suit :


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



Pour empaqueter les valeurs de couleur rouge, vert et bleu dans un pixel RVB 555, procédez comme suit :


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sous-types de vidéos RVB non compressés](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



