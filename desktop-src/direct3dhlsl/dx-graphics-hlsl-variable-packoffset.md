---
title: packoffset
description: Mot clé de compression de constante de nuanceur facultatif, qui utilise la syntaxe suivante
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- HLSL packoffset
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232422"
---
# <a name="packoffset"></a>packoffset

Mot clé de compression de constante de nuanceur facultatif, qui utilise la syntaxe suivante :

: packoffset (sous- \[ composant c \] \[ . composant \] )



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                                                                                                                 | Description                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Mot clé requis.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**secteur**<br/>                                                                                                                             | L’empaquetage s’applique uniquement aux registres constants (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Sous-composant \] \[ . composant\]**<br/> | Sous-composants et composants facultatifs. Un sous-composant est un numéro de Registre, qui est un entier. Un composant se présente sous la forme \[ . XYZW \] .<br/> |



 

## <a name="remarks"></a>Notes

Utilisez ce mot clé pour empaqueter manuellement une constante de nuanceur lors [de la déclaration d’un type de variable](dx-graphics-hlsl-variable-syntax.md).

Lorsque vous compressez une constante, vous ne pouvez pas mélanger des types de constantes.

Le compilateur se comporte de façon légèrement différente pour les constantes globales et les constantes uniformes :

-   Constante globale. Une variable globale est ajoutée en tant que constante globale à un *$Global* CBuffer par le compilateur. Les éléments empaquetés automatiquement (ceux déclarés sans packoffset) s’affichent après la dernière variable compressée manuellement. Vous pouvez combiner des types lors de l’empaquetage de constantes globales.
-   Constante uniforme. Un paramètre uniforme dans la liste de paramètres d’une fonction sera ajouté à une *$param* mémoire tampon constante par le compilateur lorsque le nuanceur est compilé en dehors de l’infrastructure des effets. En cas de compilation dans l’infrastructure Effect, une constante uniforme doit être résolue en une variable uniforme définie dans la portée globale. Une constante uniforme ne peut pas être décalée manuellement ; leur utilisation recommandée est uniquement destinée à la spécialisation des nuanceurs dans lesquels elles sont réaffectées aux données globales, et non à la transmission de données d’application dans le nuanceur.

Voici quelques exemples supplémentaires : les [constantes de compression à l’aide du Shader Model 4](dx-graphics-hlsl-packing-rules.md).

## <a name="examples"></a>Exemples

Voici plusieurs exemples de décompression manuelle des constantes de nuanceur.

Compresser les sous-composants des vecteurs et des scalaires dont la taille est suffisamment grande pour empêcher le franchissement des limites du Registre. Par exemple, ils sont tous valides :


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe des variables](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





