---
description: D3DXAssembleShaderFromResource fonction-assembler un nuanceur.
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: D3DXAssembleShaderFromResource, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78df978201df37269b7d33058effc16eadc9d16f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116016"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="06733-103">D3DXAssembleShaderFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="06733-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="06733-104">Assembler un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="06733-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="06733-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06733-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="06733-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06733-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06733-107">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06733-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06733-108">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06733-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06733-109">Handle d’un module contenant la description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="06733-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="06733-110">Si ce paramètre a la **valeur null**, le module actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="06733-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="06733-111">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06733-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06733-112">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06733-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06733-113">Pointeur vers une chaîne qui spécifie le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="06733-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="06733-114">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="06733-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="06733-115">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="06733-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="06733-116">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="06733-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="06733-117">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06733-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06733-118">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="06733-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="06733-119">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif.</span><span class="sxs-lookup"><span data-stu-id="06733-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="06733-120">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="06733-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="06733-121">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06733-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06733-122">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="06733-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="06733-123">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="06733-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="06733-124">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="06733-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="06733-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="06733-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06733-126">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06733-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06733-127">Options de compilation identifiées par différents indicateurs.</span><span class="sxs-lookup"><span data-stu-id="06733-127">Compile options identified by various flags.</span></span> <span data-ttu-id="06733-128">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="06733-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="06733-129">Pour plus d’informations, consultez [indicateurs D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="06733-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="06733-130">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="06733-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06733-131">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="06733-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="06733-132">Retourne une mémoire tampon contenant le nuanceur créé.</span><span class="sxs-lookup"><span data-stu-id="06733-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="06733-133">Cette mémoire tampon contient le code de nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="06733-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="06733-134">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="06733-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06733-135">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="06733-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="06733-136">Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="06733-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="06733-137">Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="06733-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="06733-138">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="06733-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06733-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06733-139">Return value</span></span>

<span data-ttu-id="06733-140">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06733-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06733-141">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06733-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06733-142">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="06733-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="06733-143">Notes </span><span class="sxs-lookup"><span data-stu-id="06733-143">Remarks</span></span>

<span data-ttu-id="06733-144">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="06733-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="06733-145">Si Unicode est défini, l’appel de fonction est résolu en D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="06733-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="06733-146">Dans le cas contraire, l’appel de fonction est résolu en D3DXAssembleShaderFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="06733-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="06733-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06733-147">Requirements</span></span>



| <span data-ttu-id="06733-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06733-148">Requirement</span></span> | <span data-ttu-id="06733-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="06733-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06733-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="06733-150">Header</span></span><br/>  | <dl> <span data-ttu-id="06733-151"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="06733-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="06733-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06733-152">Library</span></span><br/> | <dl> <span data-ttu-id="06733-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06733-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="06733-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06733-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06733-155">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="06733-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="06733-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="06733-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="06733-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="06733-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
