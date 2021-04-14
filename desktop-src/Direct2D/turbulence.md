---
title: Effet turbulence
description: Utilisez l’effet turbulence pour générer une image bitmap basée sur la fonction de bruit perl.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- effet turbulence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104565102"
---
# <a name="turbulence-effect"></a>Effet turbulence

Utilisez l’effet turbulence pour générer une image bitmap basée sur la fonction de bruit perl.

L’effet turbulence n’a aucune image d’entrée.

Le CLSID de cet effet est CLSID \_ D2D1Turbulence.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de bruit](#noise-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

![exemple de capture d’écran montrant la sortie de l’effet turbulence.](images/32-turbulence.png)

L’effet turbulence calcule la somme d’une ou de plusieurs octaves de la fonction de bruit perl. Le bruit perl est une fonction Pseudo-aléatoire dont la valeur dépend de la valeur de la fréquence, de la position et de la valeur initiale. L’effet génère les valeurs RVBA à l’aide de l’une de ces équations.

Si vous sélectionnez le mode de bruit de la \_ \_ \_ somme fractale d2d1 turbulence bruit \_ , l’effet utilise cette équation.

![Capture d’écran montrant la fonction turbulence utilisée pour générer une image bitmap.](images/turbulence-equation1.png)

Si vous sélectionnez le \_ mode de turbulence du bruit d2d1 turbulence \_ \_ , l’effet utilise cette équation.

![fonction turbulence utilisée pour générer une image bitmap.](images/turbulence-equation2.png)

> [!Note]  
> La `PerlinNoise` fonction est comprise entre \[ -1 et 1 \] .

 

Cet effet génère des valeurs en pixels dans des valeurs alpha prémultipliées.

## <a name="effect-properties"></a>Propriétés d’effet



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom complet et énumération d’index</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offset<br/> D2D1_TURBULENCE_PROP_OFFSET<br/></td>
<td>Coordonnées où la sortie de turbulence est générée.<br/> L’algorithme utilisé pour générer le bruit perl est dépendant de la position, donc un décalage différent produit une sortie différente. Cette propriété n’est pas limitée et les unités sont spécifiées dans des DIP <br/>
<blockquote>
[!Note]<br />
Le décalage n’a pas le même effet qu’une translation, car la sortie de la fonction Noise est infinie et la fonction est encapsulée dans la vignette.
</blockquote>
<br/> Le type est D2D1_VECTOR_2F.<br/> La valeur par défaut est {0.0 f, 0.0 f}.<br/></td>
</tr>
<tr class="even">
<td>Taille<br/> D2D1_TURBULENCE_PROP_SIZE<br/></td>
<td>Taille de la sortie de turbulence.<br/> Cette propriété n’est pas limitée et les unités sont spécifiées dans des DIP <br/>
<br/> Le type est D2D1_VECTOR_2F.<br/> La valeur par défaut est {0.0 f, 0.0 f}.<br/></td>
</tr>
<tr class="odd">
<td>BaseFrequency<br/> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br/></td>
<td>Les fréquences de base dans les directions X et Y. Cette propriété est de type float et doit être supérieure à 0. Les unités sont spécifiées en 1/DIP. <br/> Une valeur de 1 (1/DIP) pour la fréquence de base se traduit par un bruit Perl qui termine un cycle entier entre deux pixels. L’interpolation d’accélération pour ces pixels entraîne des pixels complètement aléatoires, car il n’y a aucune corrélation entre les pixels.<br/> Une valeur de 0.1 (1/DIP) pour la fréquence de base, la fonction de bruit perl se répète toutes les 10 dip. Cela aboutit à une corrélation entre les pixels et l’effet de turbulence typique est visible.<br/> Le type est D2D1_VECTOR_2F.<br/> La valeur par défaut est {0,01 f, 0,01 f}.<br/></td>
</tr>
<tr class="even">
<td>NumOctaves<br/> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br/></td>
<td>Nombre d’octaves pour la fonction de bruit. Cette propriété est un UINT32 et doit être supérieure à 0.<br/> Le type est UINT32.<br/> La valeur par défaut est 1.<br/></td>
</tr>
<tr class="odd">
<td>Seed<br/> D2D1_TURBULENCE_PROP_SEED<br/></td>
<td>Valeur initiale pour le générateur Pseudo-aléatoire. Cette propriété n’est pas liée.<br/> Le type est UINT32.<br/> La valeur par défaut est 0.<br/></td>
</tr>
<tr class="even">
<td>Parasite<br/> D2D1_TURBULENCE_PROP_NOISE<br/></td>
<td>Mode de bruit de turbulence. Cette propriété peut être une <em>somme fractale</em> ou une <em>turbulence</em>. Indique s’il faut générer une image bitmap basée sur le bruit fractal ou la fonction turbulence. Pour plus d’informations, consultez <a href="#noise-modes">modes de bruit</a> . <br/> Le type est D2D1_TURBULENCE_NOISE.<br/> La valeur par défaut est D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br/></td>
</tr>
<tr class="odd">
<td>Agrafable<br/> D2D1_TURBULENCE_PROP_STITCHABLE<br/></td>
<td>Active ou désactive l’assemblage. La fréquence de base est ajustée afin que la bitmap de sortie puisse être retouchée. Cela est utile si vous souhaitez afficher en mosaïque plusieurs copies de la sortie de l’effet de turbulence.
<ul>
<li>True la bitmap de sortie peut être en mosaïque (à l’aide de l’effet de vignette) sans l’apparence des jointures. La fréquence de base est ajustée afin que la bitmap de sortie puisse être retouchée.</li>
<li>False la fréquence de base n’est pas ajustée. les coutures peuvent donc apparaître entre les vignettes si la bitmap est affichée en mosaïque.</li>
</ul>
<br/> Le type est BOOL.<br/> La valeur par défaut est FALSE.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a>Modes de bruit



| Énumération                           | Description                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| \_ \_ \_ Somme fractale du bruit de turbulence d2d1 \_ | Calcule la somme des octaves, en décalant la plage de sortie de \[ -1, 1 \] à \[ 0, 1 \] . |
| \_Turbulence du \_ bruit de turbulence d2d1 \_   | Calcule la somme de la valeur absolue de chaque octave.                                  |



 

> [!Note]  
> Aucun mode ne contient une pince explicite des valeurs de sortie.

 

## <a name="output-bitmap"></a>Bitmap de sortie

Cet effet génère une image bitmap de taille infinie logiquement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| Serveur minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

