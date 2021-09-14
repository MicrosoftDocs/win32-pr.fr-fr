---
description: Composants de filtre VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Composants de filtre VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238961"
---
# <a name="vmr-filter-components"></a>Composants de filtre VMR

VMR utilise une conception modulaire qui permet aux applications de les configurer pour de nombreux scénarios de rendu différents. En fonction de sa configuration, VMR contient de deux à cinq sous-composants (en plus de ses broches d’entrée).

![VMR en mode fenêtre avec plusieurs flux](images/vmr-multiple-streams.png)

**Mixer :** Le mélangeur est un objet COM chargé de mélanger plusieurs flux. La désentrelacement se produit également dans le mélangeur. Le mélangeur est chargé par le VMR lorsque plusieurs flux d’entrée sont détectés, ou lorsque la vidéo d’entrée est entrelacée. Le mélangeur collecte des informations sur chaque flux d’entrée et trie les flux dans l’ordre de plan correct. Il est chargé de déterminer à quel moment chaque broche d’entrée reçoit un échantillon et de demander au compositeur d’image de s’exécuter au bon moment pour effectuer la fusion réelle. Le mélangeur calcule également l’horodatage à appliquer à chaque image de sortie. Lorsque l’application fournit une image bitmap à afficher en haut de l’image composite, le mélangeur est chargé de s’assurer que la bitmap est affichée en haut, même si l’ordre de plan des flux d’entrée est modifié.

**Compositeur d’image :** Le compositeur d’image est un objet COM qui effectue la fusion réelle des flux d’entrée sur une surface DirectDraw ou Direct3D unique fournie par l’Allocator-presenter. VMR fournit un compositeur d’image par défaut qui permet aux applications d’effectuer des effets de fusion alpha 2D. Les applications peuvent fournir un compositeur d’image personnalisé pour permettre d’autres effets 2D et 3D, tels que l’application de textures à des portions de l’image, la fusion alpha par pixel, le mappage de l’image à des objets 3D stationnaires ou mobiles, et ainsi de suite.

**Allocator-présentateur :** L’Allocator-Presenter est un objet COM qui alloue l’objet DirectDraw ou Direct3D et gère la communication avec la carte graphique. Le dessin peut être exécuté comme un flip ou un blit. Vous pouvez brancher votre propre allocateur-présentateur pour créer et contrôler l’objet DirectDraw ou Direct3D, et/ou pour obtenir l’accès aux bits vidéo au moment de la présentation.

**Gestionnaire de fenêtres :** Le gestionnaire de fenêtres est utilisé uniquement en mode fenêtre. Le gestionnaire de fenêtres prend en charge les interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) et [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) héritées pour assurer la compatibilité descendante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du rendu de mixage vidéo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



