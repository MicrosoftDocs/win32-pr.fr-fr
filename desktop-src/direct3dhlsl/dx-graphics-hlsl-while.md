---
title: Instruction while
description: Exécute un bloc d’instructions jusqu’à ce que l’expression conditionnelle échoue.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while, instruction HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524597"
---
# <a name="while-statement"></a>Instruction while

Exécute un bloc d’instructions jusqu’à ce que l’expression conditionnelle échoue.

\[*Attribut* \] while ( *conditionnel* ) { *bloc d’instructions*;}



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.



| Attribut             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dérouler (x)             | Dérouler la boucle jusqu’à ce qu’elle cesse de s’exécuter. Si vous le souhaitez, vous pouvez spécifier le nombre maximal de fois que la boucle peut s’exécuter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| loop                  | Utilisez les instructions de contrôle de Flow dans le nuanceur compilé ; n’annulez pas la boucle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| fastopt               | Réduit le temps de compilation, mais produit des optimisations moins agressives. Si vous utilisez cet attribut, le compilateur ne déroulera pas les boucles.<br/> Cet attribut affecte uniquement les cibles de modèle Shader qui prennent en charge les instructions [break](dx-graphics-hlsl-break.md) . Cet attribut est disponible dans le modèle de nuanceur [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) et le [nuanceur modèle 3](dx-graphics-hlsl-sm3.md) et versions ultérieures. Elle est particulièrement utile dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures lorsque le compilateur compile des boucles. Le compilateur simule par défaut des boucles pour déterminer s’il peut les dérouler. Si vous ne souhaitez pas que le compilateur dérouler les boucles, utilisez cet attribut pour réduire le temps de compilation.<br/> |
| autoriser \_ la \_ condition UAV | Permet à une condition d’arrêt de boucle Compute Shader de se baser sur une lecture UAV. La boucle ne doit pas contenir d’intrinsèques de synchronisation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*
</dt> <dd>

[Expression](dx-graphics-hlsl-expressions.md)conditionnelle. Si l’expression prend la valeur true, le bloc d’instructions est exécuté. La boucle se termine lorsque l’expression prend la valeur false.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*
</dt> <dd>

Une ou plusieurs [instructions](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Flow Régulation](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





