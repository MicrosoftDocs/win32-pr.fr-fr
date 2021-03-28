---
title: Type de nuanceur
description: La syntaxe permettant de déclarer une variable de nuanceur dans un effet a changé de Direct3D 9 à Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Type de nuanceur HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971767"
---
# <a name="shader-type"></a><span data-ttu-id="ff3eb-104">Type de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ff3eb-104">Shader Type</span></span>

<span data-ttu-id="ff3eb-105">La syntaxe permettant de déclarer une variable de nuanceur dans un effet a changé de Direct3D 9 à Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-105">The syntax for declaring a shader variable in an effect changed from Direct3D 9 to Direct3D 10.</span></span>

## <a name="shader-type-for-direct3d-10"></a><span data-ttu-id="ff3eb-106">Type de nuanceur pour Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="ff3eb-106">Shader Type for Direct3D 10</span></span>

<span data-ttu-id="ff3eb-107">Déclarez une variable de nuanceur dans une passe d’effet (dans Direct3D 10) à l’aide de la syntaxe du type de nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ff3eb-107">Declare a shader variable within an effect pass (in Direct3D 10) using the shader type syntax:</span></span>



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3eb-108">**SetPixelShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile ( **ShaderTarget, ShaderFunction** );</span><span class="sxs-lookup"><span data-stu-id="ff3eb-108">**SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** );</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="ff3eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff3eb-109">Parameters</span></span>



| <span data-ttu-id="ff3eb-110">Élément</span><span class="sxs-lookup"><span data-stu-id="ff3eb-110">Item</span></span>                                                                                                                             | <span data-ttu-id="ff3eb-111">Description</span><span class="sxs-lookup"><span data-stu-id="ff3eb-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3eb-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span><span class="sxs-lookup"><span data-stu-id="ff3eb-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span></span><br/>         | <span data-ttu-id="ff3eb-113">Appel de l’API Direct3D qui crée l’objet Shader.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-113">The Direct3D API call that creates the shader object.</span></span> <span data-ttu-id="ff3eb-114">Peut avoir la valeur : **SetPixelShader** ou **SetGeometryShader** ou **SetVertexShader**.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-114">Can be either: **SetPixelShader** or **SetGeometryShader** or **SetVertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ff3eb-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="ff3eb-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>         | <span data-ttu-id="ff3eb-116">Modèle de nuanceur à compiler.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-116">The shader model to compile against.</span></span> <span data-ttu-id="ff3eb-117">Cela est valide pour toutes les cibles, y compris toutes les cibles Direct3D 9 et les cibles du [modèle de nuanceur 4](dx-graphics-hlsl-sm4.md) : vs \_ 4 \_ 0, GS \_ 4 \_ 0 et PS \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-117">This is valid for any target including all Direct3D 9 targets plus the [shader model 4](dx-graphics-hlsl-sm4.md) targets: vs\_4\_0, gs\_4\_0, and ps\_4\_0.</span></span><br/>                                                                                                                                                                                                                                          |
| <span data-ttu-id="ff3eb-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="ff3eb-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span></span><br/> | <span data-ttu-id="ff3eb-119">Chaîne ASCII qui contient le nom de la fonction de point d’entrée du nuanceur ; Il s’agit de la fonction qui commence l’exécution lorsque le nuanceur est appelé.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-119">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="ff3eb-120">Le (...) représente les arguments du nuanceur ; Ce sont les mêmes arguments que ceux passés à l’API de création de nuanceur : [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) ou [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) ou [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="ff3eb-120">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) or [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) or [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="ff3eb-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff3eb-121">Example</span></span>

<span data-ttu-id="ff3eb-122">Voici un exemple qui crée un nuanceur de sommets et un objet nuanceur de pixels, compilé pour un modèle de nuanceur particulier.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-122">Here is an example that creates a vertex shader and pixel shader object, compiled for a particular shader model.</span></span> <span data-ttu-id="ff3eb-123">Dans l’exemple Direct3D 10, il n’y a aucun nuanceur Geometry, donc le pointeur est défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-123">In the Direct3D 10 example, there is no geometry shader, so the pointer is set to **NULL**.</span></span>


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a><span data-ttu-id="ff3eb-124">Type de nuanceur pour Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="ff3eb-124">Shader Type for Direct3D 9</span></span>

<span data-ttu-id="ff3eb-125">Déclarez une variable de nuanceur dans une passe d’effet (pour Direct3D 9) à l’aide de la syntaxe du type de nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ff3eb-125">Declare a shader variable within an effect pass (for Direct3D 9) using the shader type syntax:</span></span>



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3eb-126">**PixelShader** = compile **ShaderTarget ShaderFunction (...); VertexShader** = compile **ShaderTarget ShaderFunction (...);**</span><span class="sxs-lookup"><span data-stu-id="ff3eb-126">**PixelShader** = compile **ShaderTarget ShaderFunction(...);VertexShader** = compile **ShaderTarget ShaderFunction(...);**</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="ff3eb-127">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff3eb-127">Parameters</span></span>



| <span data-ttu-id="ff3eb-128">Élément</span><span class="sxs-lookup"><span data-stu-id="ff3eb-128">Item</span></span>                                                                                                                                                 | <span data-ttu-id="ff3eb-129">Description</span><span class="sxs-lookup"><span data-stu-id="ff3eb-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3eb-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span><span class="sxs-lookup"><span data-stu-id="ff3eb-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span></span><br/>                                         | <span data-ttu-id="ff3eb-131">Variable de nuanceur, qui représente le nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-131">A shader variable, which represents the compiled shader.</span></span> <span data-ttu-id="ff3eb-132">Peut avoir la valeur : **PixelShader** ou **VertexShader**.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-132">Can be either: **PixelShader** or **VertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ff3eb-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="ff3eb-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>                             | <span data-ttu-id="ff3eb-134">[Modèle de nuanceur](dx-graphics-hlsl-models.md) à compiler ; dépend du type de variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-134">The [shader model](dx-graphics-hlsl-models.md) to compile against; depends on the type of shader variable.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ff3eb-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span><span class="sxs-lookup"><span data-stu-id="ff3eb-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span></span><br/> | <span data-ttu-id="ff3eb-136">Chaîne ASCII qui contient le nom de la fonction de point d’entrée du nuanceur ; Il s’agit de la fonction qui commence l’exécution lorsque le nuanceur est appelé.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-136">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="ff3eb-137">Le (...) représente les arguments du nuanceur ; Ce sont les mêmes arguments que ceux passés à l’API de création de nuanceur : [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) ou [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span><span class="sxs-lookup"><span data-stu-id="ff3eb-137">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) or [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="ff3eb-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff3eb-138">Example</span></span>

<span data-ttu-id="ff3eb-139">Voici un exemple d’objet Vertex Shader et de nuanceur de pixels, compilé pour un modèle de nuanceur particulier.</span><span class="sxs-lookup"><span data-stu-id="ff3eb-139">Here is an example of a vertex shader and pixel shader object, compiled for a particular shader model.</span></span>


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a><span data-ttu-id="ff3eb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff3eb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff3eb-141">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff3eb-141">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

