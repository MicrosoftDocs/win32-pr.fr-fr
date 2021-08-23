---
title: Décalage de profondeur
description: Les polygones en espace 3D peuvent être affichés comme s’ils n’étaient pas coplanés en ajoutant un biais (ou un biais de profondeur) à chacun d’eux.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f707a038a2da8ebe9c1adc21f6081c85f5a63fbbc1c360a4dfbbf5765d845d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990159"
---
# <a name="depth-bias"></a>Décalage de profondeur

Les polygones en espace 3D peuvent être affichés comme s’ils n’étaient pas coplanés en ajoutant un biais (ou un biais de profondeur) à chacun d’eux.

Il s’agit d’une technique couramment utilisée pour s’assurer que les ombres d’une scène s’affichent correctement. Par exemple, une ombre sur un mur aura probablement la même valeur de profondeur que le mur. Si une application affiche d’abord un mur, puis une ombre, l’ombre peut ne pas être visible ou les artefacts de profondeur peuvent être visibles.


Une application peut aider à s’assurer que les polygones sont rendus correctement en ajoutant le biais (à partir du membre **DepthBias** de [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) aux valeurs z que le système utilise lors du rendu des jeux de polygones coplanaires. Les polygones avec une plus grande valeur z sont dessinés devant les polygones avec une plus petite valeur z.

Il existe deux options pour calculer le décalage de profondeur.

1.  Si la mémoire tampon de profondeur actuellement liée à l’étape de fusion de sortie a un format **UNORM** ou qu’aucun tampon de profondeur n’est lié, la valeur d’écart est calculée comme suit :
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    où *r* est la valeur représentable minimale > 0 dans le format de mémoire tampon de profondeur converti en **float32**. Les valeurs **DepthBias** et **SlopeScaledDepthBias** sont des membres de structure [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) . La valeur de **MaxDepthSlope** est le maximum des pentes horizontales et verticales de la valeur de profondeur au pixel.
2.  Si une mémoire tampon de profondeur à virgule flottante est liée à l’étape de fusion de sortie, la valeur de décalage est calculée comme suit :
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    où *r* est le nombre de bits de mantisse dans la représentation à virgule flottante (à l’exclusion du bit masqué); par exemple, 23 pour **float32**.

La valeur de biais est ensuite ancrée comme suit :


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



La valeur de biais est ensuite utilisée pour calculer la profondeur de pixel.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



Les opérations de décalage de profondeur se produisent sur les sommets après le découpage. par conséquent, l’écart de profondeur n’a aucun effet sur le découpage géométrique. La valeur de biais est constante pour une primitive donnée et est ajoutée à la valeur z pour chaque vertex avant l’installation de l’interpolateur. Lorsque vous utilisez les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 et supérieurs, tous les calculs de biais sont effectués à l’aide de l’arithmétique à virgule flottante 32 bits. Le biais n’est appliqué à aucune primitive de point ou de ligne, à l’exception des lignes dessinées en mode filaire.

L’un des artefacts avec des ombres basées sur une mémoire tampon Shadow est l’acné Shadow, ou un ombrage de surface lui-même en raison de différences mineures entre le calcul de profondeur dans un nuanceur et la profondeur de la même surface dans le tampon d’ombre. Pour pallier cela, vous pouvez utiliser **DepthBias** et **SlopeScaledDepthBias** lors du rendu d’une mémoire tampon d’ombre. L’idée est de pousser des surfaces suffisamment en arrière lors du rendu d’un tampon d’ombre afin que le résultat de la comparaison (entre le tampon d’ombre z et le nuanceur z) soit cohérent sur l’aire de conception et éviter l’auto-ombrage local.

Toutefois, l’utilisation de **DepthBias** et de **SlopeScaledDepthBias** peut introduire de nouveaux problèmes de rendu lorsqu’un polygone affiché à un angle extrêmement aigu fait que l’équation de décalage génère une très grande valeur z. En effet, cela pousse le polygone extrêmement loin de la surface d’origine dans le mappage d’ombre. L’une des méthodes permettant d’atténuer ce problème consiste à utiliser **DepthBiasClamp**, qui fournit une limite supérieure (positive ou négative) sur la grandeur de l’écart z calculé.

> [!Note]  
> Pour les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** n’est pas pris en charge.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sortie-étape de fusion](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




