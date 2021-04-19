---
description: Crée un effet de compilateur à partir d’une description d’effet ASCII.
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: D3DXCreateEffectCompilerFromFile, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fe27683078f77d7d444bd3a763fc326e749f7517
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531551"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="066b6-103">D3DXCreateEffectCompilerFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="066b6-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="066b6-104">Crée un effet de compilateur à partir d’une description d’effet ASCII.</span><span class="sxs-lookup"><span data-stu-id="066b6-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="066b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="066b6-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="066b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="066b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="066b6-107">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="066b6-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066b6-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="066b6-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="066b6-109">Pointeur vers le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="066b6-109">Pointer to the filename.</span></span> <span data-ttu-id="066b6-110">Ce paramètre prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="066b6-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="066b6-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="066b6-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="066b6-112">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="066b6-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066b6-113">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="066b6-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="066b6-114">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="066b6-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="066b6-115">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="066b6-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="066b6-116">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="066b6-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066b6-117">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="066b6-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="066b6-118">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="066b6-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="066b6-119">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="066b6-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="066b6-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="066b6-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066b6-121">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="066b6-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="066b6-122">Options de compilation identifiées par différents indicateurs (consultez [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="066b6-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="066b6-123">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="066b6-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="066b6-124">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="066b6-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="066b6-125">*ppEffectCompiler* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="066b6-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="066b6-126">Type : **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="066b6-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="066b6-127">Adresse d’un pointeur vers une interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , contenant le compilateur d’effet.</span><span class="sxs-lookup"><span data-stu-id="066b6-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="066b6-128">*ppParseErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="066b6-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="066b6-129">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="066b6-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="066b6-130">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) , contenant tous les messages d’erreur qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="066b6-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="066b6-131">Ce paramètre peut avoir la valeur **null** pour ignorer les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="066b6-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="066b6-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="066b6-132">Return value</span></span>

<span data-ttu-id="066b6-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="066b6-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="066b6-134">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="066b6-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="066b6-135">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="066b6-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="066b6-136">Notes</span><span class="sxs-lookup"><span data-stu-id="066b6-136">Remarks</span></span>

<span data-ttu-id="066b6-137">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="066b6-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="066b6-138">Dans le cas contraire, le type de données LPCTSTR est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="066b6-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="066b6-139">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="066b6-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="066b6-140">Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="066b6-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="066b6-141">Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateEffectCompilerFromFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="066b6-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="066b6-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="066b6-142">Requirements</span></span>



| <span data-ttu-id="066b6-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="066b6-143">Requirement</span></span> | <span data-ttu-id="066b6-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="066b6-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="066b6-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="066b6-145">Header</span></span><br/>  | <dl> <span data-ttu-id="066b6-146"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="066b6-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="066b6-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="066b6-147">Library</span></span><br/> | <dl> <span data-ttu-id="066b6-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="066b6-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="066b6-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="066b6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066b6-150">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="066b6-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="066b6-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="066b6-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="066b6-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="066b6-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
