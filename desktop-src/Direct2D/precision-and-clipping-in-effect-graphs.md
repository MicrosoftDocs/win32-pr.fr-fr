---
title: Précision et découpage numérique dans les graphiques d’effet
description: Les applications qui restituent des effets à l’aide de Direct2D doivent veiller à atteindre le niveau souhaité de qualité et de prévisibilité en ce qui concerne la précision numérique.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90628661ec8cd3f16ff6a6149aecbb7e8be3e5a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031696"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Précision et découpage numérique dans les graphiques d’effet

Les applications qui restituent des effets à l’aide de Direct2D doivent veiller à atteindre le niveau souhaité de qualité et de prévisibilité en ce qui concerne la précision numérique. Cette rubrique décrit les meilleures pratiques et les paramètres pertinents dans Direct2D qui sont utiles dans les cas suivants :

-   Votre graphique d’effet repose sur une précision ou des couleurs numériques élevées en dehors de la \[ plage 0, 1 \] et vous voulez vous assurer que celles-ci seront toujours disponibles
-   Ou votre graphique d’effet repose sur l’implémentation de rendu pour fixer les couleurs intermédiaires à la \[ plage 0, 1 \] et vous voulez vous assurer que ce verrouillage se produit toujours

Direct2D divise souvent un graphique d’effet en sections et restitue chaque section dans une étape distincte. La sortie de certaines étapes peut être stockée dans des textures Direct3D intermédiaires qui, par défaut, ont une plage numérique et une précision limitées. Direct2D n’apporte aucune garantie quant à l’utilisation ou l’emplacement de ces textures intermédiaires. Ce comportement peut varier en fonction des capacités du GPU, ainsi qu’entre les versions de Windows.

Dans Windows 10, Direct2D utilise moins de textures intermédiaires en raison de l’utilisation de la liaison de nuanceur. Direct2D peut donc produire des résultats différents avec les paramètres par défaut par rapport aux versions précédentes de Windows. Cela affecte principalement les scénarios où la liaison de nuanceur est possible dans un graphique d’effet, et ce graphique contient également des effets qui produisent des couleurs de sortie étendues.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Vue d’ensemble du rendu des effets et des intermédiaires

Pour afficher un graphique d’effet, Direct2D commence par Rechercher le graphique sous-jacent des « transformations », où une transformation est un nœud graphique utilisé dans un effet. Il existe différents types de transformations, notamment ceux qui fournissent des nuanceurs Direct3D à utiliser par Direct2D.

Par exemple, Direct2D peut afficher un graphique d’effet comme suit :

![graphique d’effet avec des textures intermédiaires](images/precision-and-clipping-1.png)

Direct2D recherche les opportunités de réduction du nombre de textures intermédiaires utilisées pour le rendu du graphique d’effet ; Cette logique est opaque pour les applications. Par exemple, le graphique suivant peut être rendu par Direct2D à l’aide d’un appel de dessin Direct3D et sans texture intermédiaire :

![graphique d’effet sans texture intermédiaire](images/precision-and-clipping-2.png)

Avant Windows 10, Direct2D utilise toujours des textures intermédiaires si plusieurs nuanceurs de pixels ont été utilisés dans le même graphique d’effet. La plupart des effets intégrés qui ajustent simplement les valeurs de couleur (par exemple, luminosité ou saturation) utilisent les nuanceurs de pixels.

Dans Windows 10, Direct2D peut désormais éviter d’utiliser des textures intermédiaires dans de tels cas. Pour ce faire, il lie en interne les nuanceurs de pixels adjacents. Par exemple :

![graphique des effets Windows 10 avec plusieurs nuanceurs de pixels et aucune texture intermédiaire](images/precision-and-clipping-3.png)

Notez que tous les nuanceurs de pixels adjacents dans un graphique ne peuvent pas être liés et, par conséquent, seuls certains graphiques produiront une sortie différente sur Windows 10. Pour obtenir des informations complètes, consultez [liaison de nuanceur Effect](effect-shader-linking.md). Les restrictions principales sont les suivantes :

-   Un effet ne sera pas lié à des effets qui consomment sa sortie, si le premier effet est connecté en tant qu’entrée à plusieurs effets.
-   Un effet ne sera pas lié à un jeu d’effets comme entrée, si le premier effet échantillonne son entrée à une position logique différente de celle de sa sortie. Par exemple, un effet de matrice de couleurs peut être lié à son entrée, mais aucun effet de convolution n’est.

## <a name="built-in-effect-behavior"></a>Comportement d’effet intégré

De nombreux effets intégrés peuvent produire des couleurs en dehors de la \[ plage 0, 1 \] dans l’espace de couleurs unpremultiplied, même lorsque leurs couleurs d’entrée sont comprises dans cette plage. Dans ce cas, ces couleurs peuvent être sujettes à un découpage numérique. Notez qu’il est important de prendre en compte la plage de couleurs dans l’espace unpremultiplied, même si les effets intégrés produisent généralement des couleurs dans l’espace prémultiplié. Cela permet de s’assurer que les couleurs restent dans le même intervalle, même si d’autres effets les unpremultiply par la suite.

Certains des effets qui peuvent émettre ces couleurs hors limites offrent une propriété « ClampOutput ». Il s’agit, entre autres, des suivantes :

-   [Matrice de couleurs](color-matrix.md)
-   [Composite arithmétique](arithmetic-composite.md)
-   [Convolve](convolve-matrix.md)
-   [Effets de transfert](built-in-effects.md)

Si vous affectez la valeur TRUE à la propriété ClampOutput sur ces effets, vous obtiendrez un résultat cohérent, quels que soient les facteurs tels que la liaison de nuanceur. Notez que la fixation se produit dans l’espace unpremultiplied.

D’autres effets intégrés peuvent également produire des couleurs de sortie au-delà \[ de la plage de 0, 1 \] dans l’espace unpremultiplied, même lorsque leurs couleurs de couleur (et les propriétés de « couleur » le cas échéant) sont comprises dans cette plage. Il s’agit, entre autres, des suivantes :

-   [Effets de transformation et de mise à l’échelle](built-in-effects.md) (lorsque la propriété Mode d’interpolation est cubique ou de qualité supérieure)
-   [Effets d’éclairage](built-in-effects.md)
-   [Détection des bords](edge-detection-effect.md) (lorsque la propriété superposition des bords est vraie)
-   [Vulnérabilité](exposure-effect.md)
-   [Composite](composite.md) (lorsque la propriété mode est plus)
-   [Température et teinte](temperature-and-tint-effect.md)
-   [Sépia :](sepia-effect.md)
-   [Saturation](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Forçage du découpage numérique dans un graphique d’effet

Si vous utilisez des effets listés ci-dessus qui n’ont pas de propriété ClampOutput, les applications doivent envisager de forcer le verrouillage numérique. Cela peut être fait en insérant un effet supplémentaire dans le graphique qui fixe ses pixels. Un effet de matrice de couleurs peut être utilisé, avec sa propriété « ClampOutput » définie sur TRUE et en laissant la propriété « ColorMatrix » comme valeur par défaut (transfert direct).

Une deuxième option pour obtenir des résultats cohérents consiste à demander que Direct2D utilise des textures intermédiaires de plus grande précision. Cela est décrit ci-dessous.

## <a name="controlling-precision-of-intermediate-textures"></a>Contrôle de la précision des textures intermédiaires

Direct2D offre plusieurs moyens de contrôler la précision d’un graphique. Avant d’utiliser des formats de haute précision dans Direct2D, les applications doivent s’assurer qu’elles sont prises en charge de manière suffisante par le GPU. Pour vérifier cela, utilisez [**ID2D1DeviceContext :: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).

Les applications peuvent créer un appareil Direct3D à l’aide de WARP (émulation de logiciel) pour garantir que toutes les précisions de mémoire tampon sont prises en charge indépendamment du matériel de GPU réel sur l’appareil. Cela est recommandé dans les scénarios tels que l’application d’effets à une photo lors de l’enregistrement sur disque. Même si Direct2D prend en charge les formats de mémoire tampon de haute précision sur le GPU, l’utilisation de WARP est recommandée dans ce scénario sur les GPU de niveau de fonctionnalité 9. X, en raison de la précision limitée de l’arithmétique et de l’échantillonnage des nuanceurs sur des GPU mobiles de faible puissance.

Dans chaque cas ci-dessous, la précision demandée est en fait le Direct2D de précision minimal qui sera utilisé par. Une précision supérieure peut être utilisée si les intermédiaires ne sont pas requis. Direct2D peut également partager des textures intermédiaires pour différentes parties du même graphique ou des graphiques différents. Dans ce cas, Direct2D utilise la précision maximale demandée pour toutes les opérations impliquées.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Sélection de précision dans ID2D1DeviceContext :: SetRenderingControls

La façon la plus simple de contrôler la précision des textures intermédiaires Direct2d consiste à utiliser [**ID2D1DeviceContext :: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)). Cela contrôle la précision de toutes les textures intermédiaires, tant qu’une précision n’est pas également définie manuellement sur des effets ou des transformations directement.


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  // Get the current rendering controls
  D2D1_RENDERING_CONTROLS renderingControls = {};
  Context->GetRenderingControls(&renderingControls);

  // Switch the precision within the rendering controls and set it
  renderingControls.bufferPrecision = D2D1_BUFFER_PRECISION_32BPC_FLOAT;
  Context->SetRenderingControls(&renderingControls);
}
              
```



### <a name="precision-selection-from-inputs-and-render-targets"></a>Sélection de la précision à partir des entrées et des cibles de rendu

Les applications peuvent également reposer sur la précision des entrées sur un graphique d’effet pour contrôler la précision des textures intermédiaires. Cela est vrai tant qu’une précision de mémoire tampon n’est pas spécifiée à l’aide de [**ID2D1DeviceContext :: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))et n’est pas définie manuellement sur Effects et Transform directement.

Les précisions des entrées pour les effets sont propagées par le biais du graphique pour sélectionner la précision des intermédiaires en aval. Là où les différentes branches dans le graphique d’effet rencontrent, la plus grande précision d’une entrée est utilisée.

La précision sélectionnée en fonction d’une bitmap Direct2D est déterminée à partir de son format de pixel. La précision sélectionnée pour un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) est déterminée à partir du format de pixel WIC du IWICBitmapSource sous-jacent utilisé pour créer le **ID2D1ImageSource**. Notez que Direct2D n’autorise pas la création de sources d’images avec des sources WIC utilisant des précisions non prises en charge par Direct2D et le GPU.

Il est possible que Direct2D ne puisse pas assigner un effet à une précision en fonction de ses entrées. Cela se produit lorsqu’un effet n’a pas d’entrée, ou lorsqu’un [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) est utilisé, ce qui n’a pas de précision spécifique. Dans ce cas, la précision des textures intermédiaires est déterminée à partir de l’image bitmap définie en tant que cible de rendu actuelle du contexte.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Sélection de la précision directement sur l’effet et les transformations

La précision minimale pour les textures intermédiaires peut également être définie à des emplacements explicites dans un graphique d’effet. Cela est recommandé uniquement pour les scénarios avancés.

La précision minimale peut être définie à l’aide d’une propriété sur un effet comme suit :


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



Dans une implémentation Effect, la précision minimale peut être définie à l’aide de ID2D1RenderInfo :: SetOutputPrecision, comme suit :


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Notez que la précision définie sur un effet se propage aux effets en aval dans le même graphique d’effet, sauf si une précision différente est définie sur ces effets en aval. La précision définie sur une transformation à l’intérieur d’un effet n’affecte pas la précision des nœuds de transformation en aval.

Voici la logique récursive complète utilisée pour déterminer la précision minimale pour une mémoire tampon intermédiaire qui stocke la sortie d’un nœud de transformation donné :

![Logique de précision minimale de la mémoire tampon intermédiaire](images/precision-and-clipping-4.png)

 

 