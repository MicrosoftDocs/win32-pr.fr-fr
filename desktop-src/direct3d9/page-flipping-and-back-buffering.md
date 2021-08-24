---
description: Le retournement de page est essentiel dans les logiciels multimédia, d’animation et de jeu ; elle est analogue à la façon dont vous pouvez effectuer une animation avec un bloc de papier.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Mise en mémoire tampon de basculement et de page (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134f1797300a838e453abf6811ae35b8f576e46c89ca0e929d2326b43ffea274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746929"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Mise en mémoire tampon de basculement et de page (Direct3D 9)

Le retournement de page est essentiel dans les logiciels multimédia, d’animation et de jeu ; elle est analogue à la façon dont vous pouvez effectuer une animation avec un bloc de papier. Sur chaque page, l’artiste change légèrement la figure, de sorte que lorsque vous retournez rapidement entre les feuilles, le dessin apparaît animé.

Le basculement de page dans le logiciel est similaire à celui de ce processus. Direct3D implémente la fonctionnalité de retournement de page par le biais d’une chaîne de permutation, qui est une propriété de l’appareil. Initialement, vous configurez une série de mémoires tampons Direct3D qui s’affichent à l’écran de la façon dont le papier de l’artiste bascule sur la page suivante. La première mémoire tampon est appelée « mémoire tampon d’avant ». Les mémoires tampons sous-jacentes sont appelées mémoires tampons d’arrière-plan. Votre application écrit dans une mémoire tampon d’arrière-plan, puis retourne la mémoire tampon d’arrière-plan de la couleur afin que la mémoire tampon d’arrière-plan apparaisse à l’écran. Lorsque le système affiche l’image, votre logiciel écrit à nouveau dans une mémoire tampon d’arrière-plan. Le processus se poursuit aussi longtemps que vous animez, ce qui vous permet d’animer les images efficacement.

Direct3D facilite la configuration des schémas de retournement de page à partir d’un simple schéma à double mise en mémoire tampon (une mémoire tampon d’arrière-plan de couleur avec une seule mémoire tampon d’arrière-plan) vers des schémas plus sophistiqués avec des mémoires tampons d’arrière-plan supplémentaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Qu’est-ce qu’une chaîne de permutation ? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



