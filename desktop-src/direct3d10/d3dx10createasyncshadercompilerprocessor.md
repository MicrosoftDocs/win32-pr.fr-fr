---
description: Compilez un nuanceur et créez un processeur de données de façon asynchrone.
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: D3DX10CreateAsyncShaderCompilerProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2a1cd663827cc32b868c9c6c9b74fbc3c21b8ee6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394095"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a><span data-ttu-id="566c0-103">D3DX10CreateAsyncShaderCompilerProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="566c0-103">D3DX10CreateAsyncShaderCompilerProcessor function</span></span>

<span data-ttu-id="566c0-104">Compilez un nuanceur et créez un processeur de données de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="566c0-104">Compile a shader and create a data processor asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="566c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="566c0-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="566c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="566c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="566c0-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566c0-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="566c0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="566c0-109">Chaîne qui contient le nom de fichier du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="566c0-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="566c0-110">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566c0-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-111">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="566c0-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="566c0-112">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="566c0-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="566c0-113">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566c0-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-114">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="566c0-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="566c0-115">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Affectez-lui la valeur **null** pour spécifier qu’il n’y a aucun fichier include.</span><span class="sxs-lookup"><span data-stu-id="566c0-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="566c0-116">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566c0-116">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-117">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="566c0-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="566c0-118">Nom de la fonction de point d’entrée pour le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="566c0-118">Name of the entry point function for the shader.</span></span>

</dd> <dt>

<span data-ttu-id="566c0-119">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="566c0-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-120">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="566c0-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="566c0-121">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md) ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="566c0-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="566c0-122">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="566c0-122">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="566c0-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="566c0-124">Options de compilation HLSL (voir [indicateurs de nuanceur](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="566c0-124">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="566c0-125">*ppCompiledShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="566c0-125">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-126">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="566c0-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="566c0-127">Adresse d’un pointeur vers le nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="566c0-127">Address of a pointer to the compiled shader.</span></span> <span data-ttu-id="566c0-128">Voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="566c0-128">See [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="566c0-129">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="566c0-129">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-130">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="566c0-130">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="566c0-131">Adresse d’un pointeur vers une mémoire tampon qui contient des erreurs de compilation (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="566c0-131">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="566c0-132">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="566c0-132">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="566c0-133">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="566c0-133">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="566c0-134">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="566c0-134">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="566c0-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="566c0-135">Return value</span></span>

<span data-ttu-id="566c0-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="566c0-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="566c0-137">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="566c0-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="566c0-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="566c0-138">Requirements</span></span>



| <span data-ttu-id="566c0-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="566c0-139">Requirement</span></span> | <span data-ttu-id="566c0-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="566c0-140">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="566c0-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="566c0-141">Header</span></span><br/> | <dl> <span data-ttu-id="566c0-142"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="566c0-142"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="566c0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="566c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="566c0-144">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="566c0-144">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
