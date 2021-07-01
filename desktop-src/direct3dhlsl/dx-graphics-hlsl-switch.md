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
ms.openlocfilehash: 4af131ca3a126cd6f1fd54160418bfbe70cc9cce
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119084"
---
# <a name="switch-statement"></a><span data-ttu-id="26386-104">Instruction switch</span><span class="sxs-lookup"><span data-stu-id="26386-104">switch Statement</span></span>

<span data-ttu-id="26386-105">Transférer le contrôle à un autre bloc d’instructions dans le corps du commutateur en fonction de la valeur d’un sélecteur.</span><span class="sxs-lookup"><span data-stu-id="26386-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>


<span data-ttu-id="26386-106">\[*Attribut* \] commutateur ( *Sélecteur* ) {case 0 : { *StatementBlock*;}   saut   cas 1 : { *StatementBlock*;}   saut   cas n : { *StatementBlock*;}   saut   valeur par défaut : { *StatementBlock*;}   saut</span><span class="sxs-lookup"><span data-stu-id="26386-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span>



 

## <a name="parameters"></a><span data-ttu-id="26386-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26386-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26386-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="26386-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="26386-109">Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.</span><span class="sxs-lookup"><span data-stu-id="26386-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="26386-110">Quand aucun attribut n’est spécifié, le compilateur peut utiliser un commutateur matériel ou émettre une série d’instructions **If** .</span><span class="sxs-lookup"><span data-stu-id="26386-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26386-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="26386-111">Attribute</span></span></th>
<th><span data-ttu-id="26386-112">Description</span><span class="sxs-lookup"><span data-stu-id="26386-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26386-113">aplatir</span><span class="sxs-lookup"><span data-stu-id="26386-113">flatten</span></span></td>
<td><span data-ttu-id="26386-114">Compilez l’instruction comme une série d’instructions <strong>If</strong> , chacune avec l’attribut <strong>Flatten</strong> .</span><span class="sxs-lookup"><span data-stu-id="26386-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26386-115">branche</span><span class="sxs-lookup"><span data-stu-id="26386-115">branch</span></span></td>
<td><span data-ttu-id="26386-116">Compilez l’instruction comme une série d’instructions <strong>If</strong> chacune avec l’attribut <strong>Branch</strong> .</span><span class="sxs-lookup"><span data-stu-id="26386-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="26386-117">Lorsque vous utilisez le modèle de <a href="dx-graphics-hlsl-sm2.md">nuanceur 2. x</a> ou le <a href="dx-graphics-hlsl-sm3.md">modèle de nuanceur 3,0</a>, chaque fois que vous utilisez la création de branche dynamique, vous consommez des ressources.</span><span class="sxs-lookup"><span data-stu-id="26386-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="26386-118">Ainsi, si vous utilisez la création de branche dynamique de façon excessive lorsque vous ciblez ces profils, vous pouvez recevoir des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="26386-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26386-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="26386-119">forcecase</span></span></td>
<td><span data-ttu-id="26386-120">Forcez une instruction switch dans le matériel.</span><span class="sxs-lookup"><span data-stu-id="26386-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="26386-121">Requiert un matériel 10_0 ou ultérieur de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">niveau de fonctionnalité</a> .</span><span class="sxs-lookup"><span data-stu-id="26386-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26386-122">appel</span><span class="sxs-lookup"><span data-stu-id="26386-122">call</span></span></td>
<td><span data-ttu-id="26386-123">Les corps des cas individuels dans le commutateur seront déplacés dans les sous-routines matérielles et le commutateur sera une série d’appels de sous-routine.</span><span class="sxs-lookup"><span data-stu-id="26386-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="26386-124">Requiert un matériel 10_0 ou ultérieur de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">niveau de fonctionnalité</a> .</span><span class="sxs-lookup"><span data-stu-id="26386-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="26386-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Sélection*</span><span class="sxs-lookup"><span data-stu-id="26386-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="26386-126">Variable.</span><span class="sxs-lookup"><span data-stu-id="26386-126">A variable.</span></span> <span data-ttu-id="26386-127">Les instructions case situées à l’intérieur des accolades vérifient chacune cette variable pour voir si le SwitchValue correspond à leur CaseValue particulier.</span><span class="sxs-lookup"><span data-stu-id="26386-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="26386-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="26386-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="26386-129">Une ou plusieurs [instructions](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="26386-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26386-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="26386-130">Remarks</span></span>


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



<span data-ttu-id="26386-131">Équivaut à :</span><span class="sxs-lookup"><span data-stu-id="26386-131">Is equivalent to:</span></span>


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



<span data-ttu-id="26386-132">Voici des exemples d’utilisation de forcecase et des attributs de contrôle de workflow d’appel :</span><span class="sxs-lookup"><span data-stu-id="26386-132">Here are example usages of forcecase and call flow control attributes:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="26386-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="26386-133">Requirements</span></span>



| <span data-ttu-id="26386-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26386-134">Requirement</span></span> | <span data-ttu-id="26386-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="26386-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26386-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="26386-136">Header</span></span><br/> | <dl> <span data-ttu-id="26386-137"><dt>Urlmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="26386-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26386-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26386-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26386-139">Contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="26386-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

