---
title: Précis
description: Désactivation par instruction de la refactorisation arithmétique.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507707"
---
# <a name="precise"></a>Précis

Désactivation par instruction de la refactorisation arithmétique.



| précis (masque de composant) |
|--------------------------|



 

Ce modificateur requiert l’indicateur de nuanceur global « refactorisation \_ autorisée ». Lorsque la refactorisation \_ autorisée est présente, les résultats individuels des instructions individuelles peuvent être forcés à rester précis ou non à refactoriser par les compilateurs ou les pilotes. Si les composants d’une instruction [**Mad**](mad--sm4---asm-.md) sont marqués comme **précis**, le matériel doit exécuter une instruction **Mad** ou l’équivalent exact, et il ne peut pas le fractionner en une multiplication suivie d’un ajout. À l’inverse, une multiplication suivie d’un ajout, où les deux ou les deux sont marqués comme **précis**, ne peut pas être fusionnée dans un **Mad** fusionné.

Si la refactorisation \_ autorisée n’a pas été spécifiée, le modificateur **precise** n’est pas autorisé. Cela n’est pas nécessaire, car tout est précis. Le modificateur **precise** affecte toute opération, pas seulement l’arithmétique.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Ce modificateur est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs d’instruction du Shader Model 5](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




