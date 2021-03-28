---
title: Changements de bytecode dans SM 5.1
description: SM 5.1 change la façon dont les registres de ressources sont déclarés et référencés dans les instructions.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311620"
---
# <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="0efc3-103">Changements de bytecode dans SM 5.1</span><span class="sxs-lookup"><span data-stu-id="0efc3-103">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="0efc3-104">SM 5.1 change la façon dont les registres de ressources sont déclarés et référencés dans les instructions.</span><span class="sxs-lookup"><span data-stu-id="0efc3-104">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span>

<span data-ttu-id="0efc3-105">Le SM 5.1 passe à la déclaration d’un registre « variable », de la même façon que pour les registres de mémoire partagée de groupe, illustrés dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="0efc3-105">SM5.1 moves towards declaring a register “variable”, similar to how it is done for group shared memory registers, illustrated by the following example:</span></span>

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

<span data-ttu-id="0efc3-106">Le code machine de cet exemple est le suivant :</span><span class="sxs-lookup"><span data-stu-id="0efc3-106">The disassembly of this example follows:</span></span>

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

<span data-ttu-id="0efc3-107">Chaque plage de ressources de nuanceur a maintenant un ID (nom) dans le bytecode du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0efc3-107">Each shader resource range now has an ID (a name) in the shader bytecode.</span></span> <span data-ttu-id="0efc3-108">Par exemple, le tableau de texture Tex1 devient « t 1 » dans le code d’octet du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0efc3-108">For example, tex1 texture array becomes ‘t1’ in the shader byte code.</span></span> <span data-ttu-id="0efc3-109">L’attribution d’ID uniques à chaque plage de ressources permet d’effectuer deux opérations :</span><span class="sxs-lookup"><span data-stu-id="0efc3-109">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="0efc3-110">Identifiez clairement la plage de ressources (voir la \_ ressource DCL \_ Texture2D) qui est indexée dans une instruction (voir exemple d’instruction).</span><span class="sxs-lookup"><span data-stu-id="0efc3-110">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="0efc3-111">Attachez un ensemble d’attributs à la déclaration, par exemple, le type d’élément, la taille de numérisation, le mode de fonctionnement raster, etc.</span><span class="sxs-lookup"><span data-stu-id="0efc3-111">Attach set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc..</span></span>

<span data-ttu-id="0efc3-112">Notez que l’ID de la plage n’est pas associé à la déclaration de la limite inférieure HLSL.</span><span class="sxs-lookup"><span data-stu-id="0efc3-112">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="0efc3-113">L’ordre des liaisons de ressources de réflexion et les instructions de déclaration de nuanceur sont les mêmes pour faciliter l’identification de la correspondance entre les variables HLSL et les ID de bytecode.</span><span class="sxs-lookup"><span data-stu-id="0efc3-113">The order of reflection resource bindings and shader declaration instructions is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="0efc3-114">Chaque instruction de déclaration dans le SM 5.1 utilise un opérande 3D pour définir : ID de plage, limites inférieure et supérieure.</span><span class="sxs-lookup"><span data-stu-id="0efc3-114">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="0efc3-115">Un jeton supplémentaire est émis pour spécifier l’espace de registre.</span><span class="sxs-lookup"><span data-stu-id="0efc3-115">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="0efc3-116">D’autres jetons peuvent être émis pour transmettre des propriétés supplémentaires de la plage, par exemple, CBuffer ou une instruction de déclaration de mémoire tampon structurée émet la taille de la structure ou du CBuffer.</span><span class="sxs-lookup"><span data-stu-id="0efc3-116">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="0efc3-117">Les détails exacts de l’encodage se trouvent dans d3d12TokenizedProgramFormat. h et D3D10ShaderBinary :: CShaderCodeParser.</span><span class="sxs-lookup"><span data-stu-id="0efc3-117">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and D3D10ShaderBinary::CShaderCodeParser.</span></span>

<span data-ttu-id="0efc3-118">Les instructions du SM 5.1 n’émettent pas d’informations d’opérande de ressource supplémentaires dans le cadre de l’instruction (comme dans le SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="0efc3-118">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="0efc3-119">Ces informations sont désormais déplacées vers les instructions de déclaration.</span><span class="sxs-lookup"><span data-stu-id="0efc3-119">This information is now moved to the declaration instructions.</span></span> <span data-ttu-id="0efc3-120">Dans SM 5.0, les instructions d’indexation des ressources nécessitant des attributs de ressource sont décrites dans les jetons d’opcode étendus, car l’indexation a obscurci l’Association à la déclaration.</span><span class="sxs-lookup"><span data-stu-id="0efc3-120">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="0efc3-121">Dans le SM 5.1, chaque ID (par exemple, « t 1 ») est associé de manière non ambiguë à une déclaration unique qui décrit les informations sur les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="0efc3-121">In SM5.1 each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="0efc3-122">Par conséquent, les jetons d’opcode étendus utilisés sur les instructions pour décrire les informations sur les ressources ne sont plus émis.</span><span class="sxs-lookup"><span data-stu-id="0efc3-122">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="0efc3-123">Dans les instructions de non-déclaration, un opérande de ressource pour les échantillonneurs, SRVs et UAVs est un opérande 2D.</span><span class="sxs-lookup"><span data-stu-id="0efc3-123">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="0efc3-124">Le premier index est une constante littérale qui spécifie l’ID de la plage.</span><span class="sxs-lookup"><span data-stu-id="0efc3-124">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="0efc3-125">Le deuxième index représente la valeur linéarisée de l’index.</span><span class="sxs-lookup"><span data-stu-id="0efc3-125">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="0efc3-126">La valeur est calculée par rapport au début de l’espace de Registre correspondant (et non par rapport au début de la plage logique) afin d’améliorer la corrélation avec la signature racine et réduire la charge de compilateur du pilote pour l’ajustement de l’index.</span><span class="sxs-lookup"><span data-stu-id="0efc3-126">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="0efc3-127">Un opérande de ressource pour CBVs est un opérande 3D : l’ID de littéral de la plage, l’index du CBuffer, le décalage dans l’instance particulière de CBuffer.</span><span class="sxs-lookup"><span data-stu-id="0efc3-127">A resource operand for CBVs is a 3D operand: literal ID of the range, index of the cbuffer, offset into the particular instance of cbuffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0efc3-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0efc3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0efc3-129">Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0efc3-129">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="0efc3-130">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="0efc3-130">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> </dl>

 

 




