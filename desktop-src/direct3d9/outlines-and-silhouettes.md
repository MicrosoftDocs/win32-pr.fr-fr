---
description: Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Plans et silhouettes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745533"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Plans et silhouettes (Direct3D 9)

Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.

Si votre application applique un masque de stencil à l’image d’une primitive qui est de la même forme mais légèrement inférieure, l’image résultante contient uniquement le contour de la primitive. L’application peut ensuite remplir la zone masquée du gabarit de l’image avec une couleur unie, ce qui donne à la primitive un aspect en relief.

Si la taille et la forme du masque du gabarit sont identiques à celles de la primitive que vous affichez, l’image résultante contient un trou où la primitive doit être. Votre application peut alors remplir le trou avec du noir pour produire une silhouette de la primitive.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques de tampon de stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



