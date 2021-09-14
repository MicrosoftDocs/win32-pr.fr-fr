---
title: Switch (SM4-ASM)
description: Transfère le contrôle à un autre bloc d’instructions dans le corps du commutateur en fonction de la valeur d’un sélecteur.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918191"
---
# <a name="switch-sm4---asm"></a>Switch (SM4-ASM)

Transfère le contrôle à un autre bloc d’instructions dans le corps du commutateur en fonction de la valeur d’un sélecteur.



| basculer le composant src0. Selected \_ |
|---------------------------------|



 



| Élément                                                            | Description                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[dans \] le sélecteur de l’instruction switch.<br/> |



 

## <a name="remarks"></a>Notes

Une  / construction [endswitch](endswitch--sm4---asm-.md) de commutateur se comporte exactement comme une construction de **commutateur** dans le langage C, avec l’exception suivante : pour [](case--sm4---asm-.md)les / instructions [par défaut](default--sm4---asm-.md) du cas d3d11 qui passent à la **casse** suivante / **par défaut** sans [saut](break--sm4---asm-.md) de code, il ne peut pas y avoir de code. Il est possible que plusieurs instructions **case** , y compris **default**, apparaissent séquentiellement, partageant le même bloc de code.

La condition doit être un composant de Registre 32 bits ou une quantité immédiate. La comparaison d’égalité est une opération au niveau du bit (Integer).

Comme pour toute instruction de nuanceur dans le D3D11, le matériel peut ou non implémenter directement la construction de **commutateur** .

Les instructions **switch** peuvent être imbriquées. Chaque bloc **switch** compte 1 niveau par rapport à la limite de profondeur d’imbrication de contrôle de flow de 64 par sous-routine et main, indépendamment du nombre d’instructions **case** . Le compilateur HLSL ne génère pas de sous-routines qui dépassent cette limite. Le comportement des instructions de workflow de contrôle au-delà de 64 niveaux de profondeur par sous-routine n’est pas défini.

L’exemple suivant montre comment utiliser cette instruction.

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





