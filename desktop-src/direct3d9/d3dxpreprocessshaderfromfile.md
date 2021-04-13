---
description: Prétraite un fichier de nuanceur sans effectuer la compilation. Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: D3DXPreprocessShaderFromFile, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322889"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a><span data-ttu-id="be0d3-104">D3DXPreprocessShaderFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="be0d3-104">D3DXPreprocessShaderFromFile function</span></span>

<span data-ttu-id="be0d3-105">Prétraite un fichier de nuanceur sans effectuer la compilation.</span><span class="sxs-lookup"><span data-stu-id="be0d3-105">Preprocesses a shader file without performing compilation.</span></span> <span data-ttu-id="be0d3-106">Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.</span><span class="sxs-lookup"><span data-stu-id="be0d3-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="be0d3-107">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="be0d3-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="be0d3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be0d3-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="be0d3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be0d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be0d3-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be0d3-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be0d3-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be0d3-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be0d3-112">Pointeur vers une chaîne qui spécifie le nom de fichier du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="be0d3-112">Pointer to a string that specifies the filename of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="be0d3-113">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be0d3-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be0d3-114">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="be0d3-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="be0d3-115">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif.</span><span class="sxs-lookup"><span data-stu-id="be0d3-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="be0d3-116">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="be0d3-117">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be0d3-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be0d3-118">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="be0d3-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="be0d3-119">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="be0d3-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="be0d3-120">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="be0d3-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="be0d3-121">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="be0d3-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be0d3-122">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="be0d3-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="be0d3-123">Retourne une mémoire tampon contenant une seule grande chaîne qui représente le flux de jetons mis en forme résultant.</span><span class="sxs-lookup"><span data-stu-id="be0d3-123">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="be0d3-124">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="be0d3-124">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be0d3-125">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="be0d3-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="be0d3-126">Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="be0d3-126">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="be0d3-127">Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="be0d3-127">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="be0d3-128">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="be0d3-128">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be0d3-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be0d3-129">Return value</span></span>

<span data-ttu-id="be0d3-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be0d3-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be0d3-131">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be0d3-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="be0d3-132">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="be0d3-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="be0d3-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be0d3-133">Requirements</span></span>



| <span data-ttu-id="be0d3-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be0d3-134">Requirement</span></span> | <span data-ttu-id="be0d3-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="be0d3-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be0d3-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="be0d3-136">Header</span></span><br/>  | <dl> <span data-ttu-id="be0d3-137"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="be0d3-137"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="be0d3-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be0d3-138">Library</span></span><br/> | <dl> <span data-ttu-id="be0d3-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be0d3-139"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="be0d3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be0d3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0d3-141">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="be0d3-141">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="be0d3-142">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="be0d3-142">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> <dt>

[<span data-ttu-id="be0d3-143">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="be0d3-143">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
