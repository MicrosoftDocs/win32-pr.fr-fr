---
title: Assembly modèle 4 du nuanceur
description: Assembly modèle 4 du nuanceur
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941135"
---
# <a name="shader-model-4-assembly"></a>Assembly modèle 4 du nuanceur

Le modèle de nuanceur 4 vous oblige à programmer des nuanceurs en HLSL. Toutefois, le compilateur du nuanceur compile le code HLSL dans un assembly qui s’exécute sur l’appareil. si vous utilisez PIX pour Windows pour déboguer vos nuanceurs, vous pouvez choisir d’afficher le code du nuanceur en HLSL ou en assembly. Cette section répertorie les instructions de l’assembly Shader Model 4 et Shader Model 4,1 que vous pouvez rencontrer lors du débogage d’un nuanceur.

<dl>

[Modificateurs d’instruction](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[pouvoir](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[réduis](cut--sm4---asm-.md)  
[\_constantBuffer DCL](dcl-constantbuffer.md)  
[DCL \_ globalFlags](dcl-globalflags.md)  
[\_immediateConstantBuffer DCL](dcl-immediateconstantbuffer.md)  
[\_indexableTemp DCL](dcl-indexabletemp.md)  
[\_indexRange DCL](dcl-indexrange.md)  
[\_entrée DCL](dcl-input.md)  
[\_SV d’entrée DCL \_](dcl-input-sv.md)  
[\_vPrim d’entrée DCL](dcl-input-vprim.md)  
[\_maxOutputVertexCount DCL](dcl-maxoutputvertexcount.md)  
[\_sortie DCL](dcl-output.md)  
[\_oDepth de sortie DCL \_](dcl-output-odepth.md)  
[copie DCL, \_ \_ SGV](dcl-output-sgv.md)  
[\_SIV de sortie DCL \_](dcl-output-siv.md)  
[\_outputTopology DCL](dcl-outputtopology.md)  
[\_ressource DCL](dcl-resource.md)  
[exemple de DCL \_](dcl-sampler.md)  
[temps de la DCL \_](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[Deriv \_ RTX](deriv-rtx--sm4---asm-.md)  
[Deriv \_ propriété](deriv-rty--sm4---asm-.md)  
[refuser](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[émettra](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[ENDLOOP](endloop--sm4---asm-.md)  
[endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[frc](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[IAdd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[ieq](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[IGE](ige--sm4---asm-.md)  
[ILT](ilt--sm4---asm-.md)  
[imad](imad--sm4---asm-.md)  
[imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[igne](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ishr](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[ld](ld--sm4---asm-.md)  
[Sign](log--sm4---asm-.md)  
[circuit](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[Mad](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[Moy](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[NOP](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[ResInfo](resinfo--sm4---asm-.md)  
[Av](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[\_arrondir ne](round-ne--sm4---asm-.md)  
[\_arrondir](round-ni--sm4---asm-.md)  
[arrondi \_ pi](round-pi--sm4---asm-.md)  
[rond \_ z](round-z--sm4---asm-.md)  
[rsq](rsq--sm4---asm-.md)  
[exemple](sample--sm4---asm-.md)  
[exemple \_ b](sample-b--sm4---asm-.md)  
[exemple \_ c](sample-c--sm4---asm-.md)  
[exemple \_ c \_ LZ](sample-c-lz--sm4---asm-.md)  
[exemple \_ d](sample-d--sm4---asm-.md)  
[exemple \_ l](sample-l--sm4---asm-.md)  
[SinCos,](sincos--sm4---asm-.md)  
[racine](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[UDIV](udiv--sm4---asm-.md)  
[uge](uge--sm4---asm-.md)  
[ULT](ult--sm4---asm-.md)  
[umad](umad--sm4---asm-.md)  
[UMAX](umax--sm4---asm-.md)  
[umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[XOR](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Assembly modèle de nuanceur 4,1

Le modèle de nuanceur 4,1 prend en charge toutes les instructions du Shader Model 4,0 et les instructions supplémentaires suivantes :

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[écart](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du nuanceur asm](dx9-graphics-reference-asm.md)
</dt> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




