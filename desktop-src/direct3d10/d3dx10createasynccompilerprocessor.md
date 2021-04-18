---
description: Créer un processeur de données asynchrones pour un nuanceur.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: D3DX10CreateAsyncCompilerProcessor, fonction (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211723"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a><span data-ttu-id="20c5d-103">D3DX10CreateAsyncCompilerProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="20c5d-103">D3DX10CreateAsyncCompilerProcessor function</span></span>

<span data-ttu-id="20c5d-104">Créer un processeur de données asynchrones pour un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="20c5d-104">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20c5d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="20c5d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20c5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c5d-107">*pFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c5d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20c5d-109">Chaîne qui contient le nom de fichier du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="20c5d-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-110">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-111">Type : **\* macro de [**\_ nuanceur \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) const**</span><span class="sxs-lookup"><span data-stu-id="20c5d-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="20c5d-112">Tableau de macros de nuanceur se terminant par un caractère NULL (consultez la [**\_ \_ macro de nuanceur D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); définissez cette valeur sur **null** pour ne spécifier aucune macro.</span><span class="sxs-lookup"><span data-stu-id="20c5d-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-113">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-114">Type : **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="20c5d-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="20c5d-115">Pointeur vers une interface include (voir [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="20c5d-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="20c5d-116">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="20c5d-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-117">*pFunctionName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-117">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-118">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c5d-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20c5d-119">Nom de la fonction de point d’entrée du nuanceur où commence l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="20c5d-119">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="20c5d-120">Quand vous compilez un effet, **D3DX10CreateAsyncCompilerProcessor** ignore *pFunctionName*; Nous vous recommandons de définir *pFunctionName* sur **null** , car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="20c5d-120">When you compile an effect, **D3DX10CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-121">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-121">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-122">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c5d-122">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20c5d-123">Chaîne qui spécifie le [profil de nuanceur](../direct3dhlsl/dx-graphics-hlsl-models.md) ou le modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="20c5d-123">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-124">*Flags1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-124">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-125">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c5d-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20c5d-126">[Indicateurs de compilation du nuanceur](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="20c5d-126">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-127">*Flags2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-127">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-128">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20c5d-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20c5d-129">[Indicateurs de compilation Effect](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="20c5d-129">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="20c5d-130">Quand vous compilez un nuanceur et non un fichier Effect, **D3DX10CreateAsyncCompilerProcessor** ignore *flags2*; Nous vous recommandons de définir *flags2* sur zéro, car il s’agit d’une bonne pratique de programmation qui consiste à définir un paramètre de pointeur sur la **valeur null** si la fonction appelée ne l’utilise pas.</span><span class="sxs-lookup"><span data-stu-id="20c5d-130">When you compile a shader and not an effect file, **D3DX10CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-131">*ppCompiledShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-131">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-132">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="20c5d-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="20c5d-133">Adresse d’un pointeur vers l’effet compilé (consultez [**ID3D10Blob interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="20c5d-133">Address of a pointer to the compiled effect (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-134">*ppErrorBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-134">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-135">Type : **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="20c5d-135">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="20c5d-136">Adresse d’un pointeur vers des erreurs de compilation (voir [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="20c5d-136">Address of a pointer to compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="20c5d-137">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20c5d-137">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20c5d-138">Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="20c5d-138">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="20c5d-139">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="20c5d-139">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c5d-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20c5d-140">Return value</span></span>

<span data-ttu-id="20c5d-141">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20c5d-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20c5d-142">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="20c5d-142">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20c5d-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20c5d-143">Requirements</span></span>



| <span data-ttu-id="20c5d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20c5d-144">Requirement</span></span> | <span data-ttu-id="20c5d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="20c5d-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c5d-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="20c5d-146">Header</span></span><br/> | <dl> <span data-ttu-id="20c5d-147"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="20c5d-147"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20c5d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20c5d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c5d-149">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="20c5d-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
