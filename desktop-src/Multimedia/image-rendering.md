---
title: Rendu d’image
description: Rendu d’image
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, rendu d’image
- DrawDib, dessin de DIB
- DrawDibDraw fonction)
- DrawDibGetBuffer fonction)
- DrawDibUpdate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195232"
---
# <a name="image-rendering"></a>Rendu d’image

Après avoir appelé [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) pour créer un contrôleur de périphérique DrawDib (voir [opérations DrawDib](drawdib-operations.md)), vous pouvez dessiner un DIB à l’écran à l’aide de la fonction [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) . **DrawDibDraw** détrame les bitmaps de couleur vraies lors de leur affichage avec des adaptateurs d’affichage 8 bits.

[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) prend également en charge les compresseurs vidéo de manière transparente lors de l’affichage des images bitmap compressées. Vous pouvez accéder à la mémoire tampon qui contient l’image décompressée à l’aide de la fonction [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) . **DrawDibGetBuffer** retourne la **valeur null** lors du dessin d’une bitmap non compressée. Vous devez préparer votre application pour gérer les bitmaps compressées et non compressées.

Vous pouvez actualiser une image ou une partie d’une image affichée par votre application à l’aide de la macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des fonctions DrawDib](about-the-drawdib-functions.md)
</dt> </dl>

 

 




