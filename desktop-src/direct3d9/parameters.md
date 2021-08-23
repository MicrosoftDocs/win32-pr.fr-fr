---
description: Les paramètres sont des variables d’effet.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Paramètres (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc28d1410180aac54daf306fe586694cfa1b7f4123403efc606a77385d088326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606679"
---
# <a name="parameters-direct3d-9"></a>Paramètres (Direct3D 9)

Les paramètres sont des variables d’effet.

## <a name="syntax"></a>Syntaxe

*ID du type d’utilisation* \[ : expression *sémantique* \] \[ < *(s) d’annotation* > \] \[ =   \] ;

Les paramètres peuvent être lus et écrits par l’application avec [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).

Les paramètres peuvent être référencés dans des fonctions et dans des techniques (plus précisément, dans la partie droite des affectations d’État).



| Élément                                                                                 | Description                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*syntaxe*<br/>                   | Étendue du paramètre. Consultez [utilisations et littéraux (Direct3D 9)](usages-and-literals.md).<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*entrer*<br/>                      | Toute [référence valide pour](../direct3dhlsl/dx-graphics-hlsl-reference.md) le type HLSL.<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*IDENTIFI*<br/>                            | Nom unique.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*équivalent*<br/>          | Étiquette qui suit les règles d’identificateur qui indiquent généralement l’utilisation du paramètre. Doit être un type particulier.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*<br/> | Zéro, un ou plusieurs éléments d’informations spécifiques à l’utilisateur. Peut être de n’importe quel type. Consultez [Ajouter des informations pour appliquer des paramètres avec des annotations](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*formule*<br/>    | Initialise la valeur du paramètre. Consultez [expressions (Direct3D 9)](expressions.md).<br/>                                                                  |



 

Les paramètres peuvent être initialisés à toute [référence valide pour](../direct3dhlsl/dx-graphics-hlsl-reference.md) l’expression HLSL qui réduit à une valeur littérale.

Les valeurs de paramètre ne sont pas modifiées par l’exécution d’une assignation d’État ou d’appels de fonction.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
