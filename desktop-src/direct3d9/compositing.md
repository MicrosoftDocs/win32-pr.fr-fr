---
description: Votre application peut utiliser la mémoire tampon de stencil pour les images 2D ou 3D composite sur une scène 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composition (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512906"
---
# <a name="compositing-direct3d-9"></a>Composition (Direct3D 9)

Votre application peut utiliser la mémoire tampon de stencil pour les images 2D ou 3D composite sur une scène 3D. Un masque dans le tampon de stencil est utilisé pour occultait une zone de la surface cible de rendu. Des informations 2D stockées, telles que du texte ou des bitmaps, peuvent ensuite être écrites dans la zone bloqués. Votre application peut également restituer des primitives 3D supplémentaires dans la région masquée du stencil de la surface cible de rendu. Il peut même rendre une scène entière.

Les jeux composent souvent plusieurs scènes 3D ensemble. Par exemple, la conduite des jeux affiche généralement un miroir en mode arrière. Le miroir contient la vue de la scène 3D derrière le pilote. Il s’agit essentiellement d’une deuxième scène 3D composite avec la vue d’avance du pilote.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques de tampon de stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



