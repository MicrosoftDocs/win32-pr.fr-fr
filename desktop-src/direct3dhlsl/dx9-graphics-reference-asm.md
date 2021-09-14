---
title: Référence du nuanceur asm
description: Les nuanceurs pilotent le pipeline graphique programmable.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922416"
---
# <a name="asm-shader-reference"></a>Référence du nuanceur asm

Les nuanceurs pilotent le pipeline graphique programmable.

## <a name="vertex-shader-reference"></a>Référence du nuanceur de sommets

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Différences entre vertex shader](dx9-graphics-reference-asm-vs-differences.md) résume les différences entre les versions de nuanceur de sommets.

## <a name="pixel-shader-reference"></a>Référence du nuanceur de pixels

-   [PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Différences de nuanceur de pixels](dx9-graphics-reference-asm-ps-differences.md) résume les différences entre les versions de nuanceur de pixels.

## <a name="shader-model-4-and-5-reference"></a>Référence du modèle de nuanceur 4 et 5

Les sections [Shader Model 4 assembly](dx-graphics-hlsl-sm4-asm.md) et [Shader Model 5 assembly](shader-model-5-assembly--directx-hlsl-.md) décrivent les instructions prises en charge par Shader Model 4 et 5.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Comportement des registres de constantes dans les nuanceurs d’assembly

Il existe deux façons de définir des registres constants dans un nuanceur d’assembly :

-   Déclarez une constante de nuanceur dans le code assembleur à l’aide de l’une des \* instructions Def.
-   Utilisez l’une des \* \* \* méthodes d' \* API Set ShaderConstant.

### <a name="direct3d-9-shader-constants"></a>Constantes de nuanceur Direct3D 9

Dans Direct3D 9, la durée de vie des constantes définies dans un nuanceur donné est limitée à l’exécution de ce nuanceur uniquement (et n’est pas remplaçable). Les constantes définies dans Direct3D 9 n’ont pas d’effets secondaires en dehors du nuanceur.

Voici un exemple utilisant Direct3D 9 :


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



Dans Direct3D 9, l’appel de l' \* \* \* opération obtenir ShaderConstant \* récupère uniquement les valeurs constantes définies via Set \* \* \* ShaderConstant \* .

### <a name="direct3d-8-shader-constants"></a>Constantes de nuanceur Direct3D 8

Ce comportement est différent dans Direct3D 8. x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



Dans Direct3D 8. x Set \* \* \* ShaderConstant prend effet immédiatement. Examinez le scénario suivant :


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



Le résultat indésirable est que l’ordre dans lequel les nuanceurs sont définis peut affecter le comportement observé des nuanceurs individuels.

## <a name="shader-driver-model-requirements"></a>Spécifications du modèle de pilote Shader

Les interfaces Direct3D 9 sont limitées aux pilotes d’interface de pilote de périphérique (DDI) qui sont au niveau de DirectX 7 et versions ultérieures. Pour vérifier le niveau DDI, exécutez l' [outil de diagnostic DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) et examinez le fichier texte enregistré.

Pour référence, les interfaces Direct3D 8 fonctionnent uniquement sur les pilotes DDI DirectX 6 et versions ultérieures.

## <a name="shader-binary-format"></a>Format binaire du nuanceur

La disposition au niveau du bit du flux d’instructions du nuanceur est définie dans D3d9types. h. Si vous souhaitez concevoir votre propre compilateur de nuanceur ou des outils de construction et que vous souhaitez obtenir plus d’informations sur le flux de jeton du nuanceur, consultez le kit de développement de pilotes (DDK) Direct3D 9.

## <a name="c-like-shader-language"></a>Langage de nuanceur de type C

Consultez [référence HLSL](dx-graphics-hlsl-reference.md) pour découvrir un langage de nuanceur de type C.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence pour le langage HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




