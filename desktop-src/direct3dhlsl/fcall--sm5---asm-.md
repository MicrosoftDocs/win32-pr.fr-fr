---
title: FCALL (SM5-ASM)
description: Appel de fonction d’interface.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381221"
---
# <a name="fcall-sm5---asm"></a>FCALL (SM5-ASM)

Appel de fonction d’interface.



| FCALL FP \# \[ arrayIndex \] \[ callSite\] |
|--------------------------------------|



 



| Élément                                                                                                           | Description                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*ép\#*<br/>                                                  | \[dans \] le pointeur de fonction.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*<br/> | \[\]facultatif. Spécifie un décalage dans le tableau de pointeurs de fonction. Ce paramètre doit être un entier non signé littéral si FP \# n’a pas été déclaré comme indexable. Sinon, arrayIndex peut être de la forme littérale base + offset à partir d’un registre de nuanceur. Par exemple, FCALL FP1 \[ R1. w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*<br/>     | \[\]facultatif. Offset d’entier non signé littéral dans la table de fonctions sélectionnée, en sélectionnant un corps \# de fonction FB à exécuter. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Notes

*mode \# FP* \[  \] \[ arrayIndex \] correspond à une table de fonctions particulière, sélectionnée à partir de l’API en dehors du nuanceur, à partir des choix de la table de fonctions figurant dans la déclaration de *FP \#*.

La somme de \# en *FP \#* et *arrayIndex* sélectionne la table de fonctions. Par exemple, si une interface est déclarée en tant que FP4 \[ 4 \] \[ 3 \] (taille de tableau de 4), les **FCALL** s suivants sont équivalents : FCALL FP4 \[ 2 \] \[ 3 \] et FP5 \[ 1 \] \[ 3 \] , car 4 + 2 = 5 + 1.

### <a name="restrictions"></a>Restrictions

-   Si *arrayIndex* utilise l’indexation dynamique, le comportement n’est pas défini si *arrayIndex* divergent sur les appels de nuanceur adjacents, qui pourraient s’exécuter dans échelons. Le compilateur HLSL tentera d’interdire ce cas de figure.

    Les appels adjacents peuvent être inactifs en raison du contrôle de Flow, car il n’interrompt pas l’exécution de échelons.

-   Si *FP \#*  +  *arrayIndex* spécifie un index hors limites, le comportement n’est pas défini.
-   Pour les cas non définis décrits ici, cela signifie que le comportement de l’appareil D3D actuel devient non défini, y compris la possibilité de perte de l’appareil. Toutefois, aucune mémoire en dehors de l’appareil D3D actif n’est accessible ou exécutée en tant que code.

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette instruction est prise en charge dans les modèles de nuanceur suivants :



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | non        |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | non        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 5 du nuanceur (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





