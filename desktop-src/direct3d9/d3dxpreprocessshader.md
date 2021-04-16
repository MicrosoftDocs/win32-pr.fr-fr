---
description: Prétraite un nuanceur sans effectuer la compilation. Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.
ms.assetid: d91258ed-6206-487a-aa81-e7c2bcea21ea
title: D3DXPreprocessShader, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 042cebe4e678ac1715a37ec3425ec0f21561797c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530855"
---
# <a name="d3dxpreprocessshader-function"></a><span data-ttu-id="30a53-104">D3DXPreprocessShader fonction)</span><span class="sxs-lookup"><span data-stu-id="30a53-104">D3DXPreprocessShader function</span></span>

<span data-ttu-id="30a53-105">Prétraite un nuanceur sans effectuer la compilation.</span><span class="sxs-lookup"><span data-stu-id="30a53-105">Preprocesses a shader without performing compilation.</span></span> <span data-ttu-id="30a53-106">Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.</span><span class="sxs-lookup"><span data-stu-id="30a53-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="30a53-107">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="30a53-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="30a53-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30a53-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataSize,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="30a53-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30a53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a53-110">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30a53-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a53-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a53-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a53-112">Pointeur vers une chaîne qui contient le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="30a53-112">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="30a53-113">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30a53-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a53-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a53-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a53-115">Longueur des données en octets.</span><span class="sxs-lookup"><span data-stu-id="30a53-115">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="30a53-116">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30a53-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a53-117">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="30a53-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="30a53-118">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif.</span><span class="sxs-lookup"><span data-stu-id="30a53-118">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="30a53-119">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="30a53-119">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30a53-120">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30a53-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a53-121">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="30a53-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="30a53-122">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="30a53-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="30a53-123">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="30a53-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="30a53-124">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="30a53-124">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a53-125">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="30a53-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="30a53-126">Retourne une mémoire tampon contenant une seule grande chaîne qui représente le flux de jetons mis en forme résultant.</span><span class="sxs-lookup"><span data-stu-id="30a53-126">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="30a53-127">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="30a53-127">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a53-128">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="30a53-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="30a53-129">Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="30a53-129">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="30a53-130">Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="30a53-130">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="30a53-131">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="30a53-131">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a53-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30a53-132">Return value</span></span>

<span data-ttu-id="30a53-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30a53-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30a53-134">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30a53-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30a53-135">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="30a53-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a53-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30a53-136">Requirements</span></span>



| <span data-ttu-id="30a53-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30a53-137">Requirement</span></span> | <span data-ttu-id="30a53-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="30a53-138">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a53-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="30a53-139">Header</span></span><br/>  | <dl> <span data-ttu-id="30a53-140"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="30a53-140"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="30a53-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30a53-141">Library</span></span><br/> | <dl> <span data-ttu-id="30a53-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30a53-142"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="30a53-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30a53-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a53-144">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="30a53-144">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="30a53-145">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="30a53-145">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="30a53-146">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="30a53-146">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
