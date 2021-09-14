---
title: Rendu (Direct3D 12 Graphics)
description: Cette section contient des informations sur les fonctionnalités de rendu nouvelles dans Direct3D 12 (et Direct3D 11,3).
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ad70a054881e9472ff27a76a62dca62fdf3653
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012894"
---
# <a name="rendering-direct3d-12-graphics"></a>Rendu (Direct3D 12 Graphics)

Cette section contient des informations sur les fonctionnalités de rendu nouvelles dans Direct3D 12 (et Direct3D 11,3).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pixellisation conservatrice](conservative-rasterization.md)<br/>                             | La pixellisation conservatrice apporte une certaine certitude au rendu des pixels, ce qui est utile en particulier pour les algorithmes de détection des collisions.<br/>                                                                                                                                                                                                                                              |
| [Dessin indirect](indirect-drawing.md)<br/>                                                 | Le dessin indirect permet de déplacer le parcours de scène et l’élimination du processeur vers le GPU, ce qui peut améliorer les performances. La mémoire tampon de commande peut être générée par le processeur ou le GPU.<br/>                                                                                                                                                                                              |
| [Affichage ordonné du rastériseur](rasterizer-order-views.md)<br/>                                   | Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons UAV avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de la canalisation Graphics pour UAVs. Cela permet l’utilisation d’algorithmes OIT (commande Independent transparent), ce qui donne de meilleurs résultats de rendu lorsque plusieurs objets transparents sont alignés les uns avec les autres dans une vue. <br/> |
| [Valeur de référence du stencil spécifié par le nuanceur](shader-specified-stencil-reference-value.md)<br/> | L’activation des nuanceurs de pixels pour la sortie de la valeur de référence du stencil, plutôt que l’utilisation de l’API-spécifiée, permet un contrôle granulaire très précis des opérations du stencil.<br/>                                                                                                                                                                                                              |
| [Chaînes de permutation](swap-chains.md)<br/>                                                           | Les chaînes d’échange contrôlent la rotation de la mémoire tampon d’arrière-plan, formant ainsi la base de l’animation graphique.<br/>                                                                                                                                                                                                                                                                                            |



 

Les rubriques suivantes sont également nouvelles dans Direct3D 12 et Direct3D 11,3 :

-   [Mappage de texture par défaut](default-texture-mapping.md)
-   [Chargements de vues d’accès non ordonnées typées](typed-unordered-access-view-loads.md)
-   [Ressources en mosaïque de volume](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Plage dynamique élevée et gamme de couleurs étendue

Reportez-vous à la prise en charge de la plage dynamique élevée (plus grande différence entre les blancs les plus clairs et les noirs les plus foncés) et la gamme de couleurs larges (10 bits, plutôt que 8 bits, par couleur) décrite dans [DXGI 1,5 améliorations](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation de Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

