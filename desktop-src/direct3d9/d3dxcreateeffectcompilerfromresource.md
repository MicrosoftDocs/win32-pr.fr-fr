---
description: Crée un ID3DXEffectCompiler à partir d’une description d’effet ASCII.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: D3DXCreateEffectCompilerFromResource, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211811"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a><span data-ttu-id="bbffe-103">D3DXCreateEffectCompilerFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="bbffe-103">D3DXCreateEffectCompilerFromResource function</span></span>

<span data-ttu-id="bbffe-104">Crée un [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) à partir d’une description d’effet ASCII.</span><span class="sxs-lookup"><span data-stu-id="bbffe-104">Creates an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbffe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbffe-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="bbffe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbffe-107">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bbffe-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbffe-108">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbffe-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbffe-109">Handle d’un module contenant la description de l’effet.</span><span class="sxs-lookup"><span data-stu-id="bbffe-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="bbffe-110">Si ce paramètre a la **valeur null**, le module actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bbffe-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="bbffe-111">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bbffe-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbffe-112">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbffe-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbffe-113">Pointeur vers la ressource.</span><span class="sxs-lookup"><span data-stu-id="bbffe-113">Pointer to the resource.</span></span> <span data-ttu-id="bbffe-114">Ce paramètre prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="bbffe-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="bbffe-115">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="bbffe-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="bbffe-116">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bbffe-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbffe-117">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="bbffe-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="bbffe-118">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="bbffe-118">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="bbffe-119">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="bbffe-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bbffe-120">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bbffe-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbffe-121">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="bbffe-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="bbffe-122">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="bbffe-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="bbffe-123">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="bbffe-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="bbffe-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bbffe-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbffe-125">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbffe-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbffe-126">Options de compilation identifiées par différents indicateurs (consultez [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="bbffe-126">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="bbffe-127">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bbffe-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="bbffe-128">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="bbffe-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="bbffe-129">*ppEffectCompiler* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bbffe-129">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbffe-130">Type : **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbffe-130">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="bbffe-131">Adresse d’un pointeur vers une interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , contenant le compilateur d’effet.</span><span class="sxs-lookup"><span data-stu-id="bbffe-131">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="bbffe-132">*ppParseErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bbffe-132">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbffe-133">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbffe-133">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bbffe-134">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , contenant tous les messages d’erreur qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="bbffe-134">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="bbffe-135">Ce paramètre peut avoir la valeur **null** pour ignorer les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bbffe-135">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbffe-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbffe-136">Return value</span></span>

<span data-ttu-id="bbffe-137">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bbffe-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bbffe-138">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bbffe-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bbffe-139">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bbffe-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbffe-140">Notes</span><span class="sxs-lookup"><span data-stu-id="bbffe-140">Remarks</span></span>

<span data-ttu-id="bbffe-141">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="bbffe-141">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="bbffe-142">Dans le cas contraire, le type de données LPCTSTR est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="bbffe-142">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="bbffe-143">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="bbffe-143">The compiler setting also determines the function version.</span></span> <span data-ttu-id="bbffe-144">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateEffectCompilerFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="bbffe-144">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromResourceW.</span></span> <span data-ttu-id="bbffe-145">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateEffectCompilerFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="bbffe-145">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbffe-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbffe-146">Requirements</span></span>



| <span data-ttu-id="bbffe-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbffe-147">Requirement</span></span> | <span data-ttu-id="bbffe-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbffe-148">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbffe-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbffe-149">Header</span></span><br/>  | <dl> <span data-ttu-id="bbffe-150"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbffe-150"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="bbffe-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bbffe-151">Library</span></span><br/> | <dl> <span data-ttu-id="bbffe-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbffe-152"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bbffe-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbffe-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbffe-154">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="bbffe-154">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="bbffe-155">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="bbffe-155">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="bbffe-156">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="bbffe-156">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
