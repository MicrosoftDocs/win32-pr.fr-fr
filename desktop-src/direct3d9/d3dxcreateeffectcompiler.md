---
description: 'Fonction D3DXCreateEffectCompiler : crée un compilateur d’effet à partir d’une description d’effet ASCII.'
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: D3DXCreateEffectCompiler, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 38ab58ed15609d468d25f4406353448e4fd6adb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115767"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="34531-103">D3DXCreateEffectCompiler fonction)</span><span class="sxs-lookup"><span data-stu-id="34531-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="34531-104">Crée un effet de compilateur à partir d’une description d’effet ASCII.</span><span class="sxs-lookup"><span data-stu-id="34531-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="34531-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34531-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="34531-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34531-107">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34531-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34531-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34531-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34531-109">Pointeur vers une mémoire tampon qui contient une description d’effet.</span><span class="sxs-lookup"><span data-stu-id="34531-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="34531-110">*SrcDataLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34531-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34531-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34531-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34531-112">Longueur, en octets, des données d’effet.</span><span class="sxs-lookup"><span data-stu-id="34531-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="34531-113">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34531-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34531-114">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="34531-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="34531-115">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="34531-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="34531-116">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="34531-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34531-117">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34531-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34531-118">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="34531-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="34531-119">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="34531-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="34531-120">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="34531-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="34531-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="34531-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34531-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34531-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34531-123">Options de compilation identifiées par différents indicateurs (consultez [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="34531-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="34531-124">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="34531-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="34531-125">Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="34531-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="34531-126">*ppEffectCompiler* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34531-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34531-127">Type : **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="34531-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="34531-128">Adresse d’un pointeur vers une interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) contenant le compilateur d’effet.</span><span class="sxs-lookup"><span data-stu-id="34531-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="34531-129">*ppParseErrors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34531-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34531-130">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="34531-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="34531-131">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) contenant tous les messages d’erreur qui se sont produits pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="34531-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="34531-132">Ce paramètre peut avoir la valeur **null** pour ignorer les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="34531-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34531-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="34531-133">Return value</span></span>

<span data-ttu-id="34531-134">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34531-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34531-135">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34531-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="34531-136">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="34531-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="34531-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34531-137">Requirements</span></span>



| <span data-ttu-id="34531-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34531-138">Requirement</span></span> | <span data-ttu-id="34531-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="34531-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34531-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="34531-140">Header</span></span><br/>  | <dl> <span data-ttu-id="34531-141"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="34531-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="34531-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34531-142">Library</span></span><br/> | <dl> <span data-ttu-id="34531-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34531-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="34531-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34531-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34531-145">Fonctions Effect</span><span class="sxs-lookup"><span data-stu-id="34531-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="34531-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="34531-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="34531-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="34531-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
