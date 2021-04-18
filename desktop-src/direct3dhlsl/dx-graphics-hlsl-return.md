---
title: Instruction return
description: Une instruction return signale la fin d’une fonction.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Instruction return HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104971470"
---
# <a name="return-statement"></a>Instruction return

Une instruction return signale la fin d’une fonction.



|                   |
|-------------------|
| valeur de retour \[ \] ; |



 

L’instruction return la plus simple retourne le contrôle de la fonction au programme appelant ; elle ne retourne aucune valeur.


```
void main()
{
    return ;
}
```



Toutefois, une instruction return peut retourner une ou plusieurs valeurs. Cet exemple retourne une valeur littérale :


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



Cet exemple retourne le résultat scalaire d’une expression.


```
return  light.enabled = true ;
```



Cet exemple retourne un vecteur à quatre composants qui est construit à partir d’une variable locale et d’un littéral.


```
return  float4(color.rgb, 1) ;
```



Cet exemple retourne un vecteur à quatre composants qui est construit à partir du résultat retourné par une fonction intrinsèque, ainsi que des valeurs littérales.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Cet exemple retourne une structure qui contient un ou plusieurs membres.


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




