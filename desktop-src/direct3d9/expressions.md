---
description: Les expressions sont des instructions mathématiques ou logiques qui sont utilisées sur le côté droit d’un signe égal. Il existe de nombreux types d’expressions.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expressions (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daeffeb09a2c2f496f73d492581cb2b51ac2e518e176bbbc848889bef5716b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985699"
---
# <a name="expressions-direct3d-9"></a>Expressions (Direct3D 9)

Les expressions sont des instructions mathématiques ou logiques qui sont utilisées sur le côté droit d’un signe égal. Il existe de nombreux types d’expressions.

## <a name="expressions"></a>Expressions

1.  Référence de variable
    ```
    ( variable ) or<variable >
    ```

    

2.  Scalaire numérique
    ```
    scalar 
    ```

    

3.  Expression numérique

    ```
    ( numeric expression )
    ```

    

    Toutes les expressions HLL numériques standard sont prises en charge ici.

4.  Constructeur
    ```
    type ( constructor arguments )
    ```

    

5.  Liste des initialiseurs

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    Les valeurs scalaires doivent être des valeurs scalaires littérales.

    Le nombre d’initialiseurs doit être compatible avec la variable (State) sur le côté gauche du signe égal.

6.  OU expression

    ```
    token [ | token ... ]
    ```

    

    Les jetons doivent être compatibles avec la variable (État) sur le côté gauche du signe égal.

    Les jetons ne respectent pas la casse.

7.  NULL

    ```
    NULL
    ```

    

    La valeur NULL ne peut être assignée qu’à un nuanceur, un échantillonneur ou un objet texture.

8.  Bloc d’assembly

    ```
    asm { code }
    ```

    

    Les blocs d’assembly PS doivent être affectés à l’État PIXELSHADER.

    Les blocs d’assembly VS doivent être affectés à l’État VERTEXSHADER.

9.  Bloc d’état de l’échantillonneur

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    Les blocs d’état de l’échantillonneur sont des séquences d’état d’une étape d’échantillonnage non indexée ou d’affectations de texture.

    Les blocs d’état de l’échantillonneur doivent être affectés à l’état de l’effet d’échantillonnage.

10. Bloc d’état de l’état d’effet

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    Les blocs d’État sont des séquences d’état général. Les blocs d’État peuvent être imbriqués, mais ne peuvent pas contenir de références circulaires.

    Les blocs d’État doivent être affectés à l’état de l’effet STATEBLOCK.

11. Compilation HLSL

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    Le nuanceur vertex et la \_ \_ cible m n indiquent la \_ version du nuanceur de sommets de la version D3DVS (m, n). La cible de nuanceur de pixels PS \_ m \_ n indique la \_ version de nuanceur de pixels de la version D3DPS (m, n).

    Les expressions de compilation du langage de niveau supérieur du nuanceur de sommets ne peuvent être assignées qu’à l’état de l’effet VERTEXSHADER. Les expressions de compilation du langage de haut niveau de nuanceur de pixels ne peuvent être assignées qu’à l’état d’effet PIXELSHADER.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



