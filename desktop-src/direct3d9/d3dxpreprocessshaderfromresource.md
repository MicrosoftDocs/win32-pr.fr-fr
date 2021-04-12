---
description: Prétraite une ressource de nuanceur sans effectuer la compilation. Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: D3DXPreprocessShaderFromResource, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322838"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a><span data-ttu-id="00669-104">D3DXPreprocessShaderFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="00669-104">D3DXPreprocessShaderFromResource function</span></span>

<span data-ttu-id="00669-105">Prétraite une ressource de nuanceur sans effectuer la compilation.</span><span class="sxs-lookup"><span data-stu-id="00669-105">Preprocesses a shader resource without performing compilation.</span></span> <span data-ttu-id="00669-106">Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.</span><span class="sxs-lookup"><span data-stu-id="00669-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="00669-107">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="00669-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="00669-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00669-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="00669-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00669-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00669-110">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00669-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00669-111">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00669-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00669-112">Handle du module qui contient la ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="00669-112">Handle to the module that holds the shader resource.</span></span> <span data-ttu-id="00669-113">Si cette valeur est **null**, le module en cours sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="00669-113">If this value is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="00669-114">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00669-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00669-115">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00669-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00669-116">Chaîne qui représente le nom de la ressource dans le module.</span><span class="sxs-lookup"><span data-stu-id="00669-116">String that represents the name of the resource in the module.</span></span>

</dd> <dt>

<span data-ttu-id="00669-117">*pDefines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00669-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00669-118">Type : **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="00669-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="00669-119">Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif.</span><span class="sxs-lookup"><span data-stu-id="00669-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="00669-120">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="00669-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="00669-121">*pInclude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00669-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00669-122">Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="00669-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="00669-123">Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include.</span><span class="sxs-lookup"><span data-stu-id="00669-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="00669-124">Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.</span><span class="sxs-lookup"><span data-stu-id="00669-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="00669-125">*ppShaderText* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="00669-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00669-126">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="00669-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="00669-127">Retourne une mémoire tampon contenant une seule grande chaîne qui représente le flux de jetons mis en forme résultant.</span><span class="sxs-lookup"><span data-stu-id="00669-127">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="00669-128">*ppErrorMsgs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="00669-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00669-129">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="00669-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="00669-130">Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="00669-130">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="00669-131">Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="00669-131">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="00669-132">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="00669-132">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00669-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00669-133">Return value</span></span>

<span data-ttu-id="00669-134">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00669-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00669-135">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="00669-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="00669-136">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="00669-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="00669-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00669-137">Requirements</span></span>



| <span data-ttu-id="00669-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00669-138">Requirement</span></span> | <span data-ttu-id="00669-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="00669-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00669-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="00669-140">Header</span></span><br/>  | <dl> <span data-ttu-id="00669-141"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="00669-141"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="00669-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00669-142">Library</span></span><br/> | <dl> <span data-ttu-id="00669-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00669-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="00669-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00669-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00669-145">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="00669-145">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="00669-146">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="00669-146">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="00669-147">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="00669-147">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> </dl>

 

 
