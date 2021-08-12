---
title: Syntaxe d’annotation (Direct3D 11)
description: Une annotation est une information définie par l’utilisateur, déclarée avec la syntaxe décrite dans cette section.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1109695f6239708e8f241b796b888b8d494acd7ab806b98c08352dbe3aeaee3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538563"
---
# <a name="annotation-syntax-direct3d-11"></a>Syntaxe d’annotation (Direct3D 11)

Une annotation est une information définie par l’utilisateur, déclarée avec la syntaxe décrite dans cette section.



| <Valeur du *nom* de *type de données*  =  ; *...* ; > |
|----------------------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                                   | Description                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Décimal*<br/> | \[dans \] le type de données, qui comprend tout type [HLSL scalaire](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , ainsi que le [type chaîne](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*<br/>                 | \[dans \] une chaîne ASCII, qui représente le nom de l’annotation.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Ajoutée*<br/>             | \[dans \] la valeur initiale de l’annotation.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[dans \] les annotations supplémentaires (paires nom-valeur).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Remarques

Vous pouvez ajouter plusieurs annotations entre crochets pointus, chacune d’elles étant séparées par un point-virgule. Les API d’infrastructure d’effet reconnaissent les annotations sur les variables globales ; toutes les autres annotations sont ignorées.

## <a name="example"></a>Exemple

Voici quelques exemples.


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format d’effet](d3d11-effect-format.md)
</dt> <dt>

[Syntaxe de la variable Effect](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

