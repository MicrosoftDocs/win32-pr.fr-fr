---
title: Transitions d’images vidéo
description: Transitions d’images vidéo
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK, images vidéo transitions
- ASF (Advanced Systems Format), transitions d’images vidéo
- ASF (format des systèmes avancés), transitions d’images vidéo
- transitions d’images vidéo
- Windows Codec Media Video 9 image v2
- codecs, codec Windows Media Video 9 Image v2
- flux vidéo, codec Windows Media Video 9 Image v2
- flux vidéo, transitions d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404643"
---
# <a name="video-image-transitions"></a>Transitions d’images vidéo

le codec Windows Media Video 9 Image v2 anime une série d’images, générant ainsi un flux vidéo. Le codec peut manipuler deux images en même temps, en les fusionnant et en créant une transition de l’une à l’autre, en fonction de la configuration que vous fournissez. Cette section décrit les transitions prises en charge et les paramètres dont elles ont besoin.

Les transitions sont répertoriées dans le tableau suivant par leurs identificateurs globaux.



| Identificateur de la transition                                                                           | Description                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_liaison d' \_ étrave de transition VIDEOIMAGE \_ WMT \_**](wmt-videoimage-transition-bow-tie.md)              | Une nouvelle image est révélée dans un ensemble de triangles sur les côtés opposés du cadre.                                                                  |
| [**\_cercle de \_ transition \_ VIDEOIMAGE WMT**](wmt-videoimage-transition-circle.md)                 | La nouvelle image est révélée dans un cercle.                                                                                                           |
| [**\_ \_ fondu croisé de transition VIDEOIMAGE \_ WMT \_**](wmt-videoimage-transition-cross-fade.md)        | Aucune transition spéciale, les coefficients de fusion des deux images déterminent la fondu enchaîné (dissolution).                                         |
| [**\_transition de \_ transition VIDEOIMAGE en \_ diagonale**](wmt-videoimage-transition-diagonal.md)             | Une nouvelle image est révélée le long d’une ligne diagonale, en partant d’un coin du cadre.                                                          |
| [**\_transition VIDEOIMAGE WMT- \_ \_ losange**](wmt-videoimage-transition-diamond.md)               | La nouvelle image est révélée en losange.                                                                                                          |
| [**\_ \_ transition \_ en fondu VIDEOIMAGE WMT \_ vers la \_ couleur**](wmt-videoimage-transition-fade-to-color.md) | Se dissout de l’image à une image de couleur unie.                                                                                          |
| [**VIDEOIMAGE de transition à la \_ \_ transition WMT \_ \_**](wmt-videoimage-transition-filled-v.md)            | La nouvelle image est révélée dans un triangle provenant d’un côté du cadre.                                                                  |
| [**\_ \_ basculement de transition VIDEOIMAGE WMT \_**](wmt-videoimage-transition-flip.md)                     | L’ancienne image est pivotée sur un axe y à travers le centre du cadre. La nouvelle image est révélée à l’arrière de l’ancienne image.                    |
| [**inversion de \_ transition VIDEOIMAGE WMT \_ \_**](wmt-videoimage-transition-inset.md)                   | Une nouvelle image est révélée par un rectangle provenant d’un coin du cadre.                                                               |
| [**\_VIDEOIMAGE de \_ transition de BASCULement WMT \_**](wmt-videoimage-transition-iris.md)                     | La nouvelle image est révélée le long de l’axe x et de l’axe y.                                                                                          |
| [**\_rouleau de \_ page de transition VIDEOIMAGE \_ WMT \_**](wmt-videoimage-transition-page-roll.md)          | L’ancienne image est transformée en effet de basculement de page, révélant ainsi la nouvelle image sous-jacente.                                                      |
| [**\_rectangle de \_ transition \_ VIDEOIMAGE WMT**](wmt-videoimage-transition-rectangle.md)           | Une nouvelle image est révélée par un rectangle dans le cadre.                                                                                       |
| [**\_révélation de \_ transition \_ VIDEOIMAGE WMT**](wmt-videoimage-transition-reveal.md)                 | La nouvelle image est révélée le long d’une ligne droite provenant d’un côté du cadre.                                                          |
| [**\_diapositive de \_ transition \_ VIDEOIMAGE WMT**](wmt-videoimage-transition-slide.md)                   | L’ancienne image coulisse en dehors du cadre, en révélant la nouvelle image sous-jacente.                                                                       |
| [**\_ \_ fractionnement de transition VIDEOIMAGE WMT \_**](wmt-videoimage-transition-split.md)                   | Une nouvelle image est révélée par un fractionnement horizontal ou vertical dans l’ancienne image. Le fractionnement s’affiche sur une ligne droite à partir du cadre. |
| [**\_étoile de \_ transition \_ VIDEOIMAGE WMT**](wmt-videoimage-transition-star.md)                     | Une nouvelle image est révélée par une étoile à cinq branches dans le cadre.                                                                               |
| [**\_volant de \_ transition \_ VIDEOIMAGE WMT**](wmt-videoimage-transition-wheel.md)                   | La nouvelle image est révélée par quatre rayons pivotés avec un point pivot commun.                                                                     |



 

Chaque transition est entièrement décrite dans sa propre rubrique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> <dt>

[**\_VIDEOIMAGE WMT \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




