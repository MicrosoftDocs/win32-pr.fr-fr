---
title: if, instruction
description: Exécuter de manière conditionnelle une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Instruction if (HLSL)
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66c04a2ac9c995d3eafa0f93171483c784c72814
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473095"
---
# <a name="if-statement"></a>if, instruction

Exécuter de manière conditionnelle une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.

\[*Attribut* \] if ( *conditionnel* ) { *bloc d’instructions*;}



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.




| Attribut | Description | 
|-----------|-------------|
| branche | Évaluez un seul côté de l’instruction if en fonction de la condition donnée.<blockquote>[!Note]<br />Lorsque vous utilisez le modèle de <a href="dx-graphics-hlsl-sm2.md">nuanceur 2. x</a> ou le <a href="dx-graphics-hlsl-sm3.md">modèle de nuanceur 3,0</a>, chaque fois que vous utilisez la création de branche dynamique, vous consommez des ressources. Ainsi, si vous utilisez la création de branche dynamique de façon excessive lorsque vous ciblez ces profils, vous pouvez recevoir des erreurs de compilation.</blockquote><br /> | 
| aplatir | Évaluez les deux côtés de l’instruction if et choisissez entre les deux valeurs résultantes. | 




 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*
</dt> <dd>

[Expression](dx-graphics-hlsl-expressions.md)conditionnelle. L’expression est évaluée et, si la valeur est true, le bloc d’instructions est exécuté.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*
</dt> <dd>

Une ou plusieurs [instructions HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque le compilateur utilise la méthode Branch pour compiler une instruction if, il génère du code qui évalue un seul côté de l’instruction if en fonction de la condition donnée. Par exemple, dans l’instruction if :


```
[branch] if(x)
{
    x = sqrt(x);
}
```



L’instruction **If** a un bloc Else implicite, qui est équivalent à x = x. Étant donné que nous avons indiqué au compilateur d’utiliser la méthode Branch avec l’attribut Branch précédent, le code compilé évalue x et n’exécute que le côté qui doit être exécuté. Si x est égal à zéro, il exécute le côté **else** et, s’il n’est pas nul, il exécute le côté **Then** .

À l’inverse, si l’attribut **flattive** est utilisé, le code compilé évalue les deux côtés de l’instruction **If** et choisit entre les deux valeurs résultantes à l’aide de la valeur d’origine x. Voici un exemple d’utilisation de l’attribut Flatten :


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



Dans certains cas, l’utilisation des attributs Branch ou flattx peut générer une erreur de compilation. L’attribut Branch peut échouer si l’une des deux côtés de l’instruction if contient une fonction de dégradé, telle que [**tex2D**](dx-graphics-hlsl-tex2d.md). L’attribut aplati peut échouer si l’une des deux faces de l’instruction if contient une instruction Append de flux ou toute autre instruction qui a des effets secondaires.

Une instruction **If** peut également utiliser un bloc Else facultatif. Si l’expression **If** a la valeur true, le code du bloc d’instructions associé à l’instruction if est traité. Dans le cas contraire, le bloc d’instructions associé au bloc Else facultatif est traité.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Flow Régulation](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





