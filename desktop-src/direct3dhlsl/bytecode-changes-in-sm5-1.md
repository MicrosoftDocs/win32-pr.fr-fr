---
title: Changements de bytecode dans SM 5.1
description: SM 5.1 change la façon dont les registres de ressources sont déclarés et référencés dans les instructions.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93d7d8533bac3750e743166a9d64b687fc06f0fbf21931d44e7d83d462cf15a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794557"
---
# <a name="bytecode-changes-in-sm51"></a>Changements de bytecode dans SM 5.1

SM 5.1 change la façon dont les registres de ressources sont déclarés et référencés dans les instructions.

Le SM 5.1 passe à la déclaration d’un registre « variable », de la même façon que pour les registres de mémoire partagée de groupe, illustrés dans l’exemple suivant :

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

Le code machine de cet exemple est le suivant :

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots used
```

Chaque plage de ressources de nuanceur a maintenant un ID (nom) dans le bytecode du nuanceur. Par exemple, le tableau de texture Tex1 devient « t 1 » dans le code d’octet du nuanceur. L’attribution d’ID uniques à chaque plage de ressources permet d’effectuer deux opérations :

-   Identifiez clairement la plage de ressources (voir la \_ ressource DCL \_ Texture2D) qui est indexée dans une instruction (voir exemple d’instruction).
-   Attachez un ensemble d’attributs à la déclaration, par exemple, le type d’élément, la taille de numérisation, le mode de fonctionnement raster, etc.

Notez que l’ID de la plage n’est pas associé à la déclaration de la limite inférieure HLSL.

L’ordre des liaisons de ressources de réflexion et les instructions de déclaration de nuanceur sont les mêmes pour faciliter l’identification de la correspondance entre les variables HLSL et les ID de bytecode.

Chaque instruction de déclaration dans le SM 5.1 utilise un opérande 3D pour définir : ID de plage, limites inférieure et supérieure. Un jeton supplémentaire est émis pour spécifier l’espace de registre. D’autres jetons peuvent être émis pour transmettre des propriétés supplémentaires de la plage, par exemple, CBuffer ou une instruction de déclaration de mémoire tampon structurée émet la taille de la structure ou du CBuffer. Les détails exacts de l’encodage se trouvent dans d3d12TokenizedProgramFormat. h et D3D10ShaderBinary :: CShaderCodeParser.

Les instructions du SM 5.1 n’émettent pas d’informations d’opérande de ressource supplémentaires dans le cadre de l’instruction (comme dans le SM 5.0). Ces informations sont désormais déplacées vers les instructions de déclaration. Dans SM 5.0, les instructions d’indexation des ressources nécessitant des attributs de ressource sont décrites dans les jetons d’opcode étendus, car l’indexation a obscurci l’Association à la déclaration. Dans le SM 5.1, chaque ID (par exemple, « t 1 ») est associé de manière non ambiguë à une déclaration unique qui décrit les informations sur les ressources requises. Par conséquent, les jetons d’opcode étendus utilisés sur les instructions pour décrire les informations sur les ressources ne sont plus émis.

Dans les instructions de non-déclaration, un opérande de ressource pour les échantillonneurs, SRVs et UAVs est un opérande 2D. Le premier index est une constante littérale qui spécifie l’ID de la plage. Le deuxième index représente la valeur linéarisée de l’index. La valeur est calculée par rapport au début de l’espace de Registre correspondant (et non par rapport au début de la plage logique) afin d’améliorer la corrélation avec la signature racine et réduire la charge de compilateur du pilote pour l’ajustement de l’index.

Un opérande de ressource pour CBVs est un opérande 3D : l’ID de littéral de la plage, l’index du CBuffer, le décalage dans l’instance particulière de CBuffer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Modèle de nuanceur 5,1](shader-model-5-1.md)
</dt> </dl>

 

 




