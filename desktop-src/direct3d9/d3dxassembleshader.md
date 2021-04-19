---
description: Assembler un nuanceur.
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: D3DXAssembleShader, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7268d394021c7dc1be665f8ed8781a827d1fcdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537261"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="bc98a-103">D3DXAssembleShader fonction)</span><span class="sxs-lookup"><span data-stu-id="bc98a-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="bc98a-104">Assembler un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bc98a-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc98a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc98a-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="bc98a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc98a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc98a-107">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc98a-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc98a-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc98a-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc98a-109">Pointeur vers une mémoire tampon qui contient les données du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bc98a-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="bc98a-110">*SrcDataLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc98a-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc98a-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc98a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc98a-112">Longueur des données d’effet, en octets.</span><span class="sxs-lookup"><span data-stu-id="bc98a-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bc98a-113">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc98a-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc98a-114">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc98a-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="bc98a-115">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif.</span><span class="sxs-lookup"><span data-stu-id="bc98a-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="bc98a-116">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="bc98a-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc98a-117">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc98a-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc98a-118">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="bc98a-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="bc98a-119">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="bc98a-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="bc98a-120">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="bc98a-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="bc98a-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bc98a-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc98a-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc98a-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc98a-123">Options de compilation identifiées par différents indicateurs.</span><span class="sxs-lookup"><span data-stu-id="bc98a-123">Compile options identified by various flags.</span></span> <span data-ttu-id="bc98a-124">Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bc98a-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="bc98a-125">Pour plus d’informations, consultez [indicateurs D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="bc98a-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="bc98a-126">*ppShader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc98a-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc98a-127">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc98a-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bc98a-128">Retourne une mémoire tampon contenant le nuanceur créé.</span><span class="sxs-lookup"><span data-stu-id="bc98a-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="bc98a-129">Cette mémoire tampon contient le code de nuanceur compilé, ainsi que toutes les informations de débogage et de table de symboles incorporées.</span><span class="sxs-lookup"><span data-stu-id="bc98a-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="bc98a-130">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc98a-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc98a-131">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc98a-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bc98a-132">Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="bc98a-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="bc98a-133">Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="bc98a-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="bc98a-134">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="bc98a-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc98a-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc98a-135">Return value</span></span>

<span data-ttu-id="bc98a-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc98a-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc98a-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc98a-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bc98a-138">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bc98a-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc98a-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc98a-139">Requirements</span></span>



| <span data-ttu-id="bc98a-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc98a-140">Requirement</span></span> | <span data-ttu-id="bc98a-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc98a-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc98a-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc98a-142">Header</span></span><br/>  | <dl> <span data-ttu-id="bc98a-143"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc98a-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bc98a-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc98a-144">Library</span></span><br/> | <dl> <span data-ttu-id="bc98a-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc98a-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bc98a-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc98a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc98a-147">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="bc98a-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="bc98a-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="bc98a-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="bc98a-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="bc98a-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
