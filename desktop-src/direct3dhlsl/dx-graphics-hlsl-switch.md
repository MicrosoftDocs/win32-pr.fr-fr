---
title: Switch, instruction (urlmon. h)
description: Transférer le contrôle à un autre bloc d’instructions dans le corps du commutateur en fonction de la valeur d’un sélecteur.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Switch, instruction HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c65049acce4265dd2abdf849119aad5902db9e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761923"
---
# <a name="switch-statement"></a>Instruction switch

Transférer le contrôle à un autre bloc d’instructions dans le corps du commutateur en fonction de la valeur d’un sélecteur.



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Attribut* \] commutateur ( *Sélecteur* ) {case 0 : { *StatementBlock*;}   saut   cas 1 : { *StatementBlock*;}   saut   cas n : { *StatementBlock*;}   saut   valeur par défaut : { *StatementBlock*;}   saut |



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*
</dt> <dd>

Paramètre facultatif qui contrôle la façon dont l’instruction est compilée. Quand aucun attribut n’est spécifié, le compilateur peut utiliser un commutateur matériel ou émettre une série d’instructions **If** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>aplatir</td>
<td>Compilez l’instruction comme une série d’instructions <strong>If</strong> , chacune avec l’attribut <strong>Flatten</strong> .</td>
</tr>
<tr class="even">
<td>branche</td>
<td>Compilez l’instruction comme une série d’instructions <strong>If</strong> chacune avec l’attribut <strong>Branch</strong> .
<blockquote>
[!Note]<br />
Lorsque vous utilisez le modèle de <a href="dx-graphics-hlsl-sm2.md">nuanceur 2. x</a> ou le <a href="dx-graphics-hlsl-sm3.md">modèle de nuanceur 3,0</a>, chaque fois que vous utilisez la création de branche dynamique, vous consommez des ressources. Ainsi, si vous utilisez la création de branche dynamique de façon excessive lorsque vous ciblez ces profils, vous pouvez recevoir des erreurs de compilation.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>forcecase</td>
<td>Forcez une instruction switch dans le matériel.
<blockquote>
[!Note]<br />
Requiert un matériel 10_0 ou ultérieur de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">niveau de fonctionnalité</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>appel</td>
<td>Les corps des cas individuels dans le commutateur seront déplacés dans les sous-routines matérielles et le commutateur sera une série d’appels de sous-routine.
<blockquote>
[!Note]<br />
Requiert un matériel 10_0 ou ultérieur de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">niveau de fonctionnalité</a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Sélection*
</dt> <dd>

Variable. Les instructions case situées à l’intérieur des accolades vérifient chacune cette variable pour voir si le SwitchValue correspond à leur CaseValue particulier.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Une ou plusieurs [instructions](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Notes


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



Équivaut à :


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



Voici des exemples d’utilisation de forcecase et des attributs de contrôle de workflow d’appel :


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Urlmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle de Flow](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

