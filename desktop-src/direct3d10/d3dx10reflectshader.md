---
description: Cette fonction, qui crée un objet Shader-Reflection pour la récupération d’informations sur un nuanceur compilé, n’existe plus. Au lieu de cela, utilisez D3DReflect ou D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: D3DX10ReflectShader, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106544401"
---
# <a name="d3dx10reflectshader-function"></a><span data-ttu-id="3bd81-104">D3DX10ReflectShader fonction)</span><span class="sxs-lookup"><span data-stu-id="3bd81-104">D3DX10ReflectShader function</span></span>

<span data-ttu-id="3bd81-105">Cette fonction, qui crée un objet Shader-Reflection pour la récupération d’informations sur un nuanceur compilé, n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="3bd81-105">This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- no longer exists.</span></span> <span data-ttu-id="3bd81-106">Au lieu de cela, utilisez [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) ou [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span><span class="sxs-lookup"><span data-stu-id="3bd81-106">Instead, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) or [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd81-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bd81-107">Syntax</span></span>


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a><span data-ttu-id="3bd81-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bd81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd81-109">*pShaderBytecode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3bd81-109">*pShaderBytecode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd81-110">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="3bd81-110">Type: **const void\***</span></span>

<span data-ttu-id="3bd81-111">Pointeur vers le nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="3bd81-111">A pointer to the compiled shader.</span></span> <span data-ttu-id="3bd81-112">Pour obtenir ce pointeur, consultez [obtention d’un pointeur vers un nuanceur compilé](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="3bd81-112">To get this pointer see [Getting a Pointer to a Compiled Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bd81-113">*BytecodeLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3bd81-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd81-114">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bd81-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bd81-115">Longueur de pShaderBytecode.</span><span class="sxs-lookup"><span data-stu-id="3bd81-115">Length of pShaderBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="3bd81-116">*ppReflector* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3bd81-116">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd81-117">Type : **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span><span class="sxs-lookup"><span data-stu-id="3bd81-117">Type: **[**ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span></span>

<span data-ttu-id="3bd81-118">Adresse d’une interface de réflexion du nuanceur (voir [**interface ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span><span class="sxs-lookup"><span data-stu-id="3bd81-118">Address of a shader reflection interface (see [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd81-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bd81-119">Return value</span></span>

<span data-ttu-id="3bd81-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bd81-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bd81-121">Retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="3bd81-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd81-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3bd81-122">Remarks</span></span>

<span data-ttu-id="3bd81-123">Voici un exemple de création d’un objet Shader-Reflection.</span><span class="sxs-lookup"><span data-stu-id="3bd81-123">Here is an example of creating a shader-reflection object.</span></span> <span data-ttu-id="3bd81-124">L’exemple suppose que vous démarrez avec un nuanceur compilé (représenté sous la forme</span><span class="sxs-lookup"><span data-stu-id="3bd81-124">The example assumes you start with a compiled shader (shown as</span></span>


```
pVSBuf
```



<span data-ttu-id="3bd81-125">ce que vous pouvez voir dans l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="3bd81-125">which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a><span data-ttu-id="3bd81-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bd81-126">Requirements</span></span>



| <span data-ttu-id="3bd81-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bd81-127">Requirement</span></span> | <span data-ttu-id="3bd81-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bd81-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd81-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bd81-129">Header</span></span><br/> | <dl> <span data-ttu-id="3bd81-130"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd81-130"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bd81-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bd81-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd81-132">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="3bd81-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
