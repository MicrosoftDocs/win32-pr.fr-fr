---
description: Compile un nuanceur à partir d’un effet qui contient une ou plusieurs fonctions.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'ID3DXEffectCompiler :: CompileShader, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522604"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="c3bf4-103">ID3DXEffectCompiler :: CompileShader, méthode</span><span class="sxs-lookup"><span data-stu-id="c3bf4-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="c3bf4-104">Compile un nuanceur à partir d’un effet qui contient une ou plusieurs fonctions.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3bf4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3bf4-105">Syntax</span></span>


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="c3bf4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3bf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3bf4-107">*hFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3bf4-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3bf4-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c3bf4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c3bf4-109">Identificateur unique de la fonction à compiler.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="c3bf4-110">Cette valeur ne doit pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-110">This value must not be **NULL**.</span></span> <span data-ttu-id="c3bf4-111">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c3bf4-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3bf4-112">*pTarget* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3bf4-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3bf4-113">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3bf4-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3bf4-114">Pointeur vers un profil de nuanceur qui détermine le jeu d’instructions du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="c3bf4-115">Pour obtenir la liste des profils disponibles, consultez [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="c3bf4-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="c3bf4-116">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c3bf4-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3bf4-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3bf4-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3bf4-118">Options de compilation identifiées par différents indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-118">Compile options identified by various flags.</span></span> <span data-ttu-id="c3bf4-119">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="c3bf4-120">Pour plus d’informations, consultez [indicateurs D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="c3bf4-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="c3bf4-121">*ppShader* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c3bf4-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c3bf4-122">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3bf4-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c3bf4-123">Mémoire tampon contenant le nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="c3bf4-124">Le nuanceur de compilateur est un tableau de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="c3bf4-125">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c3bf4-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3bf4-126">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c3bf4-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c3bf4-127">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3bf4-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c3bf4-128">Mémoire tampon contenant au moins le premier message d’erreur de compilation qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="c3bf4-129">Cela comprend les erreurs d’effet du compilateur et les erreurs de compilation du langage de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="c3bf4-130">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c3bf4-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3bf4-131">*ppConstantTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3bf4-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3bf4-132">Type : **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3bf4-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="c3bf4-133">Retourne une interface [**ID3DXConstantTable**](id3dxconstanttable.md) , qui peut être utilisée pour accéder aux constantes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="c3bf4-134">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-134">This value can be **NULL**.</span></span> <span data-ttu-id="c3bf4-135">Si vous compilez votre application en prenant en charge les adresses de grande taille (autrement dit, si vous utilisez l’option de l’éditeur de liens/LARGEADDRESSAWARE pour gérer les adresses supérieures à 2 Go), vous ne pouvez pas utiliser ce paramètre et devez lui affecter la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="c3bf4-136">Au lieu de cela, vous devez utiliser la fonction [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) pour récupérer la table de nuanceur-constante incorporée dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="c3bf4-137">Dans cet appel **D3DXGetShaderConstantTableEx** , vous devez passer l' **indicateur \_ LARGEADDRESSAWARE D3DXCONSTTABLE** au paramètre *Flags* pour spécifier l’accès à un espace d’adressage virtuel pouvant atteindre 4 Go.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3bf4-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3bf4-138">Return value</span></span>

<span data-ttu-id="c3bf4-139">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3bf4-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3bf4-140">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="c3bf4-141">Si les arguments ne sont pas valides, la méthode retourne D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="c3bf4-142">Si la méthode échoue, la valeur de retour est E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3bf4-143">Notes</span><span class="sxs-lookup"><span data-stu-id="c3bf4-143">Remarks</span></span>

<span data-ttu-id="c3bf4-144">Les cibles peuvent être spécifiées pour les nuanceurs de vertex, les nuanceurs de pixels et les fonctions de remplissage de texture.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c3bf4-145">Cibles de nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c3bf4-145">Vertex shader targets</span></span> | <span data-ttu-id="c3bf4-146">vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ SW, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c3bf4-146">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="c3bf4-147">Cibles de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c3bf4-147">Pixel shader targets</span></span>  | <span data-ttu-id="c3bf4-148">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c3bf4-148">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="c3bf4-149">Cibles de remplissage de texture</span><span class="sxs-lookup"><span data-stu-id="c3bf4-149">Texture fill targets</span></span>  | <span data-ttu-id="c3bf4-150">TX \_ 0, TX \_ 1</span><span class="sxs-lookup"><span data-stu-id="c3bf4-150">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="c3bf4-151">Cette méthode Compile un nuanceur à partir d’une fonction écrite dans un langage de type C.</span><span class="sxs-lookup"><span data-stu-id="c3bf4-151">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="c3bf4-152">Pour plus d’informations, consultez [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="c3bf4-152">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3bf4-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3bf4-153">Requirements</span></span>



| <span data-ttu-id="c3bf4-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3bf4-154">Requirement</span></span> | <span data-ttu-id="c3bf4-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3bf4-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3bf4-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3bf4-156">Header</span></span><br/>  | <dl> <span data-ttu-id="c3bf4-157"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3bf4-157"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c3bf4-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3bf4-158">Library</span></span><br/> | <dl> <span data-ttu-id="c3bf4-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3bf4-159"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c3bf4-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3bf4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3bf4-161">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="c3bf4-161">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="c3bf4-162">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="c3bf4-162">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
