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
# <a name="return-statement"></a><span data-ttu-id="ae208-104">Instruction return</span><span class="sxs-lookup"><span data-stu-id="ae208-104">return Statement</span></span>

<span data-ttu-id="ae208-105">Une instruction return signale la fin d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="ae208-105">A return statement signals the end of a function.</span></span>



|                   |
|-------------------|
| <span data-ttu-id="ae208-106">valeur de retour \[ \] ;</span><span class="sxs-lookup"><span data-stu-id="ae208-106">return \[value\];</span></span> |



 

<span data-ttu-id="ae208-107">L’instruction return la plus simple retourne le contrôle de la fonction au programme appelant ; elle ne retourne aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="ae208-107">The simplest return statement returns control from the function to the calling program; it returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="ae208-108">Toutefois, une instruction return peut retourner une ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="ae208-108">However, a return statement can return one or more values.</span></span> <span data-ttu-id="ae208-109">Cet exemple retourne une valeur littérale :</span><span class="sxs-lookup"><span data-stu-id="ae208-109">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="ae208-110">Cet exemple retourne le résultat scalaire d’une expression.</span><span class="sxs-lookup"><span data-stu-id="ae208-110">This example returns the scalar result of an expression.</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="ae208-111">Cet exemple retourne un vecteur à quatre composants qui est construit à partir d’une variable locale et d’un littéral.</span><span class="sxs-lookup"><span data-stu-id="ae208-111">This example returns a four-component vector that is constructed from a local variable and a literal.</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="ae208-112">Cet exemple retourne un vecteur à quatre composants qui est construit à partir du résultat retourné par une fonction intrinsèque, ainsi que des valeurs littérales.</span><span class="sxs-lookup"><span data-stu-id="ae208-112">This example returns a four-component vector that is constructed from the result that is returned from an intrinsic function, together with literal values.</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="ae208-113">Cet exemple retourne une structure qui contient un ou plusieurs membres.</span><span class="sxs-lookup"><span data-stu-id="ae208-113">This example returns a structure that contains one or more members.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="ae208-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae208-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae208-115">Fonctions (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae208-115">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




