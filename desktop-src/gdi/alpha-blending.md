---
description: La fusion alpha est utilisée pour afficher une bitmap alpha, qui est une bitmap qui a des pixels transparents ou semi-transparents.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Fusion alpha (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972786"
---
# <a name="alpha-blending-windows-gdi"></a>Fusion alpha (Windows GDI)

La *fusion alpha* est utilisée pour afficher une bitmap alpha, qui est une bitmap qui a des pixels transparents ou semi-transparents. Outre un canal de couleur rouge, vert et bleu, chaque pixel d’une bitmap Alpha possède un composant de transparence appelé « *canal alpha*». Le canal alpha contient généralement autant de bits qu’un canal de couleurs. Par exemple, un canal alpha 8 bits peut représenter 256 niveaux de transparence, à partir de 0 (la bitmap entière est transparente) à 255 (la bitmap entière est opaque).

Les mécanismes de fusion alpha sont appelés en appelant [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), qui fait référence à la structure [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .

Les valeurs alpha par pixel sont prises en charge uniquement pour la fonction RVB 32-BPP BI \_ . Cette formule est définie comme suit :


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



Cela est représenté dans la mémoire, comme indiqué dans le tableau suivant.



|       |       |       |       |
|-------|-------|-------|-------|
| 31:24 | 23:16 | 15:08 | 07:00 |
| Alpha | Rouge   | Vert | Blue  |



 

Les bitmaps peuvent également être affichées avec un facteur de transparence appliqué à la bitmap entière. Tout format bitmap peut être affiché avec une valeur alpha constante globale en définissant **SourceConstantAlpha** dans la structure [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) . La valeur alpha constante globale a 256 niveaux de transparence, à partir de 0 (la totalité de la bitmap est complètement transparente) à 255 (la bitmap entière est entièrement opaque). La valeur alpha constante globale est associée à la valeur alpha par pixel.

Pour obtenir un exemple, consultez [alpha blending a bitmap](alpha-blending-a-bitmap.md).

 

 



