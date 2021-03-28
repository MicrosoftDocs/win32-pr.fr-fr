---
title: Instruction do (ocidl. h)
description: Exécuter une série d’instructions en continu jusqu’à ce que l’expression conditionnelle échoue.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Instruction do HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211751"
---
# <a name="do-statement"></a>Instruction do

Exécuter une série d’instructions en continu jusqu’à ce que l’expression conditionnelle échoue.



|                                                                     |
|---------------------------------------------------------------------|
| \[*Attribut* \] { *bloc d’instructions*;} while ( *conditionnel* ); |



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.



| Attribut | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fastopt   | Réduit le temps de compilation, mais produit des optimisations moins agressives. Si vous utilisez cet attribut, le compilateur ne déroulera pas les boucles.<br/> Cet attribut affecte uniquement les cibles de modèle Shader qui prennent en charge les instructions [break](dx-graphics-hlsl-break.md) . Cet attribut est disponible dans le modèle de nuanceur [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) et le [nuanceur modèle 3](dx-graphics-hlsl-sm3.md) et versions ultérieures. Elle est particulièrement utile dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures lorsque le compilateur compile des boucles. Le compilateur simule par défaut des boucles pour déterminer s’il peut les dérouler. Si vous ne souhaitez pas que le compilateur dérouler les boucles, utilisez cet attribut pour réduire le temps de compilation.<br/> |



 

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*
</dt> <dd>

Une ou plusieurs [instructions](dx-graphics-hlsl-statement-blocks.md).

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*
</dt> <dd>

[Expression](dx-graphics-hlsl-expressions.md)conditionnelle. Le bloc d’instructions est exécuté avant l’évaluation de l’expression. La boucle est abandonnée lorsque l’expression prend la valeur false.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Ocidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de Flow](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





