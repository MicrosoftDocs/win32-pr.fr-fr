---
title: Instruction for
description: Exécute itérativement une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- pour l’instruction HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100889"
---
# <a name="for-statement"></a>Instruction for

Exécute itérativement une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.



|                                                                                       |
|---------------------------------------------------------------------------------------|
| \[*Attribut* \] pour ( *initialiseur ; Conditionnel Iterator* ) { *bloc d’instructions*;} |



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Paramètre facultatif qui contrôle la façon dont l’instruction est compilée. Quand aucun attribut n’est spécifié, le compilateur tente d’abord d’émettre une version restaurée de la boucle, et en cas d’échec, ou si certaines opérations sont plus faciles si la boucle a été déroulée, revient à une version non terminée de la boucle.



| Attribut             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dérouler (x)             | Dérouler la boucle jusqu’à ce qu’elle cesse de s’exécuter. Peut éventuellement spécifier le nombre maximal de fois où la boucle doit s’exécuter. Non compatible avec l’attribut de **\[ boucle \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| loop                  | Générez du code qui utilise le contrôle de Flow pour exécuter chaque itération de la boucle. Non compatible avec l’attribut **\[ Unroll \]** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| fastopt               | Réduit le temps de compilation, mais produit des optimisations moins agressives. Si vous utilisez cet attribut, le compilateur ne déroulera pas les boucles.<br/> Cet attribut affecte uniquement les cibles de modèle Shader qui prennent en charge les instructions [break](dx-graphics-hlsl-break.md) . Cet attribut est disponible dans le modèle de nuanceur [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) et le [nuanceur modèle 3](dx-graphics-hlsl-sm3.md) et versions ultérieures. Elle est particulièrement utile dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures lorsque le compilateur compile des boucles. Le compilateur simule par défaut des boucles pour déterminer s’il peut les dérouler. Si vous ne souhaitez pas que le compilateur dérouler les boucles, utilisez cet attribut pour réduire le temps de compilation. <br/> |
| autoriser \_ la \_ condition UAV | Permet à une condition d’arrêt de boucle Compute Shader de se baser sur une lecture UAV. La boucle ne doit pas contenir d’intrinsèques de synchronisation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initialiseur*
</dt> <dd>

Valeur initiale du compteur de boucle.

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*
</dt> <dd>

[Expression](dx-graphics-hlsl-expressions.md)conditionnelle. Si l’expression conditionnelle prend la valeur true, le bloc d’instructions est exécuté. La boucle se termine lorsque l’expression prend la valeur false.

</dd> <dt>

<span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Répétiteur*
</dt> <dd>

Mettez à jour la valeur du compteur de boucle.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*
</dt> <dd>

Une ou plusieurs [instructions HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Les attributs de **\[ boucle \]** et de **\[ déroulabilité \]** s’excluent mutuellement et génèrent des erreurs de compilation lorsque les deux sont spécifiés.

Les attributs de **\[ \_ \_ condition \]** **\[ \] fastopt** et allow UAV sont ignorés si **\[ Unroll \]** est spécifié.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de Flow](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





