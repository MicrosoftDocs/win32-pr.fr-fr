---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: L’assembleur de nuanceur de pixels est constitué d’un ensemble d’instructions qui fonctionnent sur les données de pixels contenues dans les registres.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190722"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4

L’assembleur de nuanceur de pixels est constitué d’un ensemble d’instructions qui fonctionnent sur les données de pixels contenues dans les registres. Les opérations sont exprimées en tant qu’instructions composées d’un opérateur et d’un ou plusieurs opérandes. Les instructions utilisent des registres pour transférer des données vers et depuis le nuanceur de pixels ALU. Les registres peuvent également être utilisés par certaines instructions pour conserver les résultats temporaires.

> [!Note]  
> La prise en charge de HLSL pour le nuanceur de pixels 1. x est déconseillée.

 

## <a name="instructions"></a>Instructions

Il existe deux catégories principales d’instructions de nuanceur de pixels : instructions arithmétiques et instructions d’adressage de texture. Les instructions arithmétiques modifient les données de couleur. Les opérations d’adressage de texture traitent les données de coordonnée de texture et, dans la plupart des cas, échantillonnent une texture. Les instructions de nuanceur de pixels sont exécutées sur une base par pixel. autrement dit, ils n’ont aucune connaissance d’autres pixels dans le pipeline.

Les instructions d’adressage de texture consomment chacune un emplacement, mais les instructions arithmétiques peuvent être associées pour activer les composants de couleur (RVB) et une instruction de composant alpha dans un seul emplacement.

les instructions PS 1 [ \_ \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiennent une liste des instructions disponibles.

Lorsque l’échantillonnage multiple est activé, les nuanceurs de pixels ne sont exécutés qu’une seule fois par pixel, et non une fois pour chaque sous-pixel. L’échantillonnage multiple augmente uniquement la résolution des arêtes de polygones, ainsi que des tests de profondeur et de stencil. Par exemple, si l’échantillonnage multiple 3 x 3 est activé et qu’un triangle en cours de pixellisation est trouvé pour couvrir cinq des neuf sous-pixels pour un pixel particulier, le nuanceur de pixels est exécuté une fois et le même résultat de couleur est appliqué aux cinq sous-pixels.

## <a name="registers"></a>Registres

[les \_ registres PS 1 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ 3 PS 1 \_ \_ \_ \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) répertorient les différents registres utilisés par le nuanceur alu.

## <a name="modifiers"></a>Modificateurs

Les [modificateurs pour PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) peuvent être utilisés pour modifier les fonctionnalités d’une instruction, ou les données lues ou écrites dans un registre.

Direct3D 9 requiert des calculs intermédiaires pour maintenir une précision d’au moins 8 bits pour tous les formats de surface. Il est recommandé d’avoir à la fois une plus grande précision (12 bits) pour les mathématiques en cours et une saturation de 8 bits entre les différentes étapes de texture. Aucun mode d’arrondi ou exception modifiable n’est pris en charge. La multiplication doit être prise en charge avec une précision d’arrondi à la valeur la plus proche pour limiter la perte de précision à un minimum.

## <a name="sampler-count"></a>Nombre d’échantillonneurs

Le nombre d’échantillonneurs de texture disponibles est le suivant :

-   Pour PS \_ 1 \_ 0-PS \_ 1 \_ 3, la valeur maximale est 4.
-   Pour PS \_ 1 \_ 4, la valeur maximale est 6.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceurs de pixels](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




