---
title: D2D_PS_ENTRY fonction (D2d1effecthelpers. h)
description: Macro qui définit un point d’entrée de nuanceur de pixels avec le nom de fonction donné.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- D2D_PS_ENTRY fonction Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540153"
---
# <a name="d2d_ps_entry-function"></a><span data-ttu-id="c8a01-104">Fonction d’entrée de la \_ PS D2D \_</span><span class="sxs-lookup"><span data-stu-id="c8a01-104">D2D\_PS\_ENTRY function</span></span>

<span data-ttu-id="c8a01-105">Macro qui définit un point d’entrée de nuanceur de pixels avec le nom de fonction donné.</span><span class="sxs-lookup"><span data-stu-id="c8a01-105">A macro that defines a pixel shader entry point with the given function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a01-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8a01-106">Syntax</span></span>

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a><span data-ttu-id="c8a01-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8a01-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a01-108">*Entryname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8a01-108">*Entryname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8a01-109">Nom du point d’entrée du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="c8a01-109">The pixel shader entry point name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a01-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c8a01-110">Return value</span></span>

<span data-ttu-id="c8a01-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c8a01-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8a01-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c8a01-112">Remarks</span></span>

<span data-ttu-id="c8a01-113">Utilisez cette macro au lieu de spécifier la signature d’entrée de point d’entrée de manière normale : tous les paramètres sont implicites et ajoutés par Direct2D pendant la compilation selon le type de cible de compilation (nuanceur complet ou fonction d’exportation).</span><span class="sxs-lookup"><span data-stu-id="c8a01-113">Use this macro instead of specifying the entry point s input signature in the normal manner: all parameters are implicit and added by Direct2D during compilation depending on the compilation target type (full shader or export function).</span></span>

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="c8a01-114">Dans cet exemple bref, Notez qu’aucun paramètre de fonction n’est déclaré, que le nombre d’entrées et le type de chaque entrée sont déclarés avant la fonction d’entrée, que l’entrée est récupérée en appelant [D2DGetInput](d2dgetinput.md), et que les directives de préprocesseur doivent être définies avant l’inclusion du fichier d’assistance.</span><span class="sxs-lookup"><span data-stu-id="c8a01-114">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="c8a01-115">Un nuanceur compatible avec la liaison doit fournir un nuanceur de pixels à passage unique standard et une fonction d’exportation de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c8a01-115">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="c8a01-116">La macro d’entrée de la \_ PS D2D \_ permet de générer chacune d’elles à partir du même code, quand elles sont utilisées conjointement avec le script de compilation du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c8a01-116">The D2D\_PS\_ENTRY macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="c8a01-117">Lors de la compilation d’un nuanceur complet, les macros sont développées dans le code suivant, qui a une signature d’entrée compatible avec les effets D2D.</span><span class="sxs-lookup"><span data-stu-id="c8a01-117">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="c8a01-118">Lors de la compilation d’une version de fonction d’exportation du même code, le code suivant est généré :</span><span class="sxs-lookup"><span data-stu-id="c8a01-118">When compiling an export function version of the same code, the following code is generated:</span></span>

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="c8a01-119">Notez que l’entrée de texture, normalement récupérée par l’échantillonnage d’un Texture2D, a été remplacée par un input0 d’entrée de fonction.</span><span class="sxs-lookup"><span data-stu-id="c8a01-119">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input input0.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a01-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8a01-120">Requirements</span></span>



| <span data-ttu-id="c8a01-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8a01-121">Requirement</span></span> | <span data-ttu-id="c8a01-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8a01-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a01-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8a01-123">Header</span></span><br/> | <dl> <span data-ttu-id="c8a01-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="c8a01-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="c8a01-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c8a01-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="c8a01-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8a01-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="c8a01-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8a01-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a01-128">Liaison de nuanceurs d’effet</span><span class="sxs-lookup"><span data-stu-id="c8a01-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="c8a01-129">Applications auxiliaires HLSL</span><span class="sxs-lookup"><span data-stu-id="c8a01-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





