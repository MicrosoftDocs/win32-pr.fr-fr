---
description: Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Plans et silhouettes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b5fcf26b3f3cbbe6e051e1a7d8517cc6d69044beb6eaed7f54baef3509a748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563409"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a>Plans et silhouettes (Direct3D 9)

Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.

Si votre application applique un masque de stencil à l’image d’une primitive qui est de la même forme mais légèrement inférieure, l’image résultante contient uniquement le contour de la primitive. L’application peut ensuite remplir la zone masquée du gabarit de l’image avec une couleur unie, ce qui donne à la primitive un aspect en relief.

Si la taille et la forme du masque du gabarit sont identiques à celles de la primitive que vous affichez, l’image résultante contient un trou où la primitive doit être. Votre application peut alors remplir le trou avec du noir pour produire une silhouette de la primitive.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques de tampon de stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



