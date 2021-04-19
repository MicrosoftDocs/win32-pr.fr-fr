---
description: Assembler un nuanceur.
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: D3DXAssembleShaderFromFile, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e355f6ce51158f72757f771114346899557c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523836"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="3b94c-103">D3DXAssembleShaderFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="3b94c-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="3b94c-104">Assembler un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3b94c-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b94c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b94c-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="3b94c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b94c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b94c-107">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b94c-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b94c-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b94c-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b94c-109">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3b94c-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="3b94c-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3b94c-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3b94c-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3b94c-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="3b94c-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3b94c-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3b94c-113">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b94c-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b94c-114">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3b94c-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3b94c-115">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif.</span><span class="sxs-lookup"><span data-stu-id="3b94c-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="3b94c-116">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="3b94c-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3b94c-117">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b94c-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b94c-118">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3b94c-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3b94c-119">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="3b94c-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3b94c-120">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="3b94c-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3b94c-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3b94c-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b94c-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b94c-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b94c-123">Options de compilation identifiées par différents indicateurs.</span><span class="sxs-lookup"><span data-stu-id="3b94c-123">Compile options identified by various flags.</span></span> <span data-ttu-id="3b94c-124">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3b94c-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="3b94c-125">Pour plus d’informations, consultez [indicateurs D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="3b94c-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="3b94c-126">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3b94c-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b94c-127">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b94c-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3b94c-128">Retourne une mémoire tampon contenant le nuanceur créé.</span><span class="sxs-lookup"><span data-stu-id="3b94c-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="3b94c-129">Cette mémoire tampon contient le code de nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="3b94c-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="3b94c-130">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3b94c-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b94c-131">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3b94c-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3b94c-132">Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="3b94c-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="3b94c-133">Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="3b94c-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="3b94c-134">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="3b94c-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b94c-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b94c-135">Return value</span></span>

<span data-ttu-id="3b94c-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b94c-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b94c-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3b94c-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3b94c-138">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3b94c-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b94c-139">Notes</span><span class="sxs-lookup"><span data-stu-id="3b94c-139">Remarks</span></span>

<span data-ttu-id="3b94c-140">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="3b94c-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3b94c-141">Si Unicode est défini, l’appel de fonction est résolu en D3DXAssembleShaderFromFileW.</span><span class="sxs-lookup"><span data-stu-id="3b94c-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="3b94c-142">Dans le cas contraire, l’appel de fonction est résolu en D3DXAssembleShaderFromFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="3b94c-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b94c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b94c-143">Requirements</span></span>



| <span data-ttu-id="3b94c-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b94c-144">Requirement</span></span> | <span data-ttu-id="3b94c-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b94c-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b94c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b94c-146">Header</span></span><br/>  | <dl> <span data-ttu-id="3b94c-147"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b94c-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3b94c-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b94c-148">Library</span></span><br/> | <dl> <span data-ttu-id="3b94c-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b94c-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3b94c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b94c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b94c-151">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3b94c-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="3b94c-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="3b94c-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="3b94c-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="3b94c-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
